---
tags: [moc, area, analytics, traffic]
created: 2026-07-07
up:
  - "[[_MOC Analytics & Reporting]]"
---

# MOC — Hiệu Quả Traffic Mạng Xã Hội

> Đo **off-platform**: mạng xã hội kéo được bao nhiêu người **click ra website/landing**, chất lượng traffic đó ra sao, có chuyển đổi không.
> Khác với [[_MOC Tương Tác Mạng Xã Hội]] (đo **on-platform**: reach, like, comment, share, follower — người ở lại trên nền tảng).

## Đo cái gì
- Lượt click ra web (link click) theo kênh
- Session từ social (GA4: `source/medium` = facebook/tiktok/zalo…)
- Chất lượng: tỉ lệ thoát (bounce), thời gian trên trang, số trang/phiên
- Chuyển đổi: lead / đơn / booking đến từ traffic social
- Bài/kênh nào kéo traffic ra web tốt nhất → link về [[_MOC Brand & Content]]

## Files
```dataview
list
from "03. Areas/Analytics & Reporting/Hiệu Quả Traffic Mạng Xã Hội"
where file.name != this.file.name
sort file.name desc
```

## Liên kết
- [[_MOC Tương Tác Mạng Xã Hội]] — tương tác on-platform
- [[Tracking Plan]] — cách gắn UTM & GA4 để đo được traffic này
- [[_MOC Marketing Channels]]
