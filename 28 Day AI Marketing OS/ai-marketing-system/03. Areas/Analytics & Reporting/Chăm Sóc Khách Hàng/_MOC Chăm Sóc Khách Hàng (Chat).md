---
tags: [moc, area, analytics, cskh, chat]
created: 2026-07-07
up:
  - "[[_MOC Analytics & Reporting]]"
---

# MOC — Chăm Sóc Khách Hàng (Chat)

> Đo hiệu quả **hộp thoại 1-1** — nơi phần lớn SME Việt thực sự chốt đơn: Messenger, Zalo OA/cá nhân, Instagram DM, inbox TikTok, comment→inbox. Đây là đáy phễu: inbox nhiều mà chốt ít = mất tiền quảng cáo đã bỏ ra để tạo inbox.

## Đo cái gì
- **Khối lượng:** số hội thoại mới / tổng, theo kênh, theo khung giờ
- **Tốc độ:** thời gian phản hồi lần đầu (First Response Time) — TB & % rep trong 5 phút; tỉ lệ bỏ sót (inbox không ai rep)
- **Phễu chat:** Inbox → Có nhu cầu (lead) → Báo giá/Hẹn → **Chốt**; tỉ lệ chat-to-close
- **Chất lượng:** CSAT/mức hài lòng (nếu có), lý do inbox top, lý do mất khách
- **Kịch bản:** câu hỏi lặp lại → đưa vào [[04. Resources/Playbooks/]] hoặc chatbot/tin nhắn mẫu

## Files
```dataview
list
from "03. Areas/Analytics & Reporting/Chăm Sóc Khách Hàng"
where file.name != this.file.name
sort file.name desc
```

## Liên kết
- [[_MOC Sales Pipeline & CRM]] — chat ra lead thì tạo hồ sơ [[People]] + đẩy vào pipeline
- [[_MOC Customer Success & Retention]] — chăm sóc sau chốt
- [[_MOC Hiệu Quả Quảng Cáo]] — inbox đến từ ads: nối CPL với tỉ lệ chốt chat
- [[04. Resources/Playbooks/]] — kịch bản xử lý từ chối, trả lời mẫu
