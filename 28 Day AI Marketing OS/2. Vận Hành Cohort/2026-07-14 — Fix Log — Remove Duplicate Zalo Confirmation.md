---
created: 2026-07-14
status: fixed
tags: [zalo, tony-ai, duplicate-response, rocket-agent-teams]
owner: Tony
---

# Fix Log — Bỏ câu “Đã trả lời trong nhóm rồi ạ.”

## Hiện tượng

Trong nhóm **Rocket Agent Teams**, Tony AI trả lời thêm câu:

```text
Đã trả lời trong nhóm rồi ạ.
```

Điều này gây khó chịu vì bot đã trả lời trong group rồi, không cần xác nhận lại.

## Nguyên nhân kỹ thuật

Trong phiên Zalo group `20260714_203911_7b5d05e4`, model đã dùng **tool Zalo** để gửi câu trả lời thật vào nhóm trước, sau đó gateway tiếp tục gửi **final answer** của agent vào nhóm. Final answer bị model viết thành:

```text
Đã trả lời trong nhóm rồi ạ.
```

Nói ngắn gọn: bot có quyền dùng tool `zalo`, nên nó tự gửi bằng tool rồi lại để gateway gửi thêm một câu xác nhận.

## Đã sửa

### 1. Tắt Zalo toolset khỏi agent

Đã chạy:

```text
zalo-freedom-elite tools disable zalo
```

Verify:

```text
Plugin toolsets:
  ✗ disabled  zalo
```

Nghĩa là agent không còn được tự gọi tool Zalo để gửi message nữa. Gateway sẽ là nơi duy nhất gửi final response.

### 2. Patch SOUL.md

Thêm luật rõ ràng:

- Không tự gửi câu trả lời bằng tool Zalo.
- Không được nói “Đã trả lời trong nhóm rồi ạ.”
- Nếu câu hỏi từng được trả lời, vẫn tóm tắt lại câu trả lời ngắn gọn.

### 3. Xóa session group cũ

Đã xóa session:

```text
20260714_203911_7b5d05e4
```

Và xóa routing mirror cho group để lần @mention tiếp theo tạo session sạch.

### 4. Restart profile gateway

Sau restart:

```text
profile_gateway_running: yes
profile_sidecar_running: yes
default_sidecars: 0
```

## Test sau sửa

Test local bằng profile, không gửi vào Zalo group:

Input:

```text
@Tony Ai tuần này học gì vậy
```

Output sau sửa là câu trả lời nội dung thật về Tuần 1 / AIOS Business Foundation, không còn câu:

```text
Đã trả lời trong nhóm rồi ạ.
```

## Lưu ý

Các tin đã gửi trong nhóm trước đó không có `msgId` trong gateway log nên chưa recall được tự động an toàn. Nếu cần xóa thủ công, có thể bấm giữ tin nhắn trong Zalo và chọn Thu hồi/Xóa. Từ sau fix này bot sẽ không tự sinh câu đó nữa.
