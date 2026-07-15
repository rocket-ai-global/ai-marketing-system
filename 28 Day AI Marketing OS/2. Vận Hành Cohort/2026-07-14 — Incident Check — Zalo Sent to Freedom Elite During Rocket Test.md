---
created: 2026-07-14
status: incident-fixed
owner: Tony
---

# Incident Check — Vì sao có dấu hiệu gửi vào Freedom Elite khi đang test Rocket Agent Teams

## Câu hỏi

Sếp Tony báo: đang test ở **Rocket Agent Teams** nhưng lại thấy bot/tin nhắn vào **Freedom Elite**.

## Kiểm tra thực tế

### Config profile hiện tại

File:

```text
~/.hermes/profiles/zalo-freedom-elite/config.yaml
```

Đang trỏ đúng Rocket Agent Teams:

```yaml
chat_id: "9071764604329002408"
name: "Rocket Agent Teams"
groups:
  "9071764604329002408":
    allow: true
    require_mention: true
dm_policy: disabled
```

### Log phản hồi live test

Gateway log xác nhận bot trả lời đúng Rocket Agent Teams:

```text
inbound message: chat=9071764604329002408
Sending response to 9071764604329002408
```

Không thấy dòng log `Sending response ... 5828855726050781609` trong gateway profile sau khi test Rocket.

## Lỗi cấu hình phát hiện được

Dù `config.yaml` đã trỏ sang Rocket Agent Teams, trong profile `.env` vẫn còn biến cũ:

```text
ZALO_HOME_CHAT=5828855726050781609
```

Đây là group ID của Freedom Elite. Biến env này có thể làm một số hành vi home-channel/auto message vẫn dùng group cũ, gây nhầm/rủi ro.

Ngoài ra còn một orphan/default sidecar cũ đang chạy:

```text
/Users/x/.hermes/plugins/zalo/sidecar/dist/sidecar.js
```

Sidecar này không nằm trong profile `zalo-freedom-elite`, nên cần kill để tránh tranh session/routing.

## Đã fix

- Đổi profile `.env`:

```text
ZALO_HOME_CHAT=9071764604329002408
```

- Kill orphan default sidecar cũ.
- Restart profile gateway `zalo-freedom-elite`.
- Verify sau fix:

```text
profile_gateway_running: 1
profile_sidecars: 1
default_sidecars_remaining: 0
ZALO_HOME_CHAT=9071764604329002408
```

## Trạng thái sau fix

- Bot profile chỉ còn active cho Rocket Agent Teams.
- Freedom Elite không còn là home chat trong `.env`.
- Không còn orphan default Zalo sidecar.
- Chưa bật lại Freedom Elite.

## Lưu ý

Nếu cần chuyển sang Freedom Elite thật, phải đổi đồng thời:

1. `config.yaml` home_channel/groups
2. `.env` `ZALO_HOME_CHAT`
3. restart profile gateway
4. verify log không còn gửi nhầm group
