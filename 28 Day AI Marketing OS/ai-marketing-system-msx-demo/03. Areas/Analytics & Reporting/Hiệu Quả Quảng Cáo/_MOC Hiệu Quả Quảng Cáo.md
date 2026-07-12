---
tags: [moc, area, analytics, ads, paid]
created: 2026-07-07
up:
  - "[[_MOC Analytics & Reporting]]"
---

# MOC — Hiệu Quả Quảng Cáo (Paid)

> Đo **tiền quảng cáo bỏ ra đổi lại được gì**: Facebook/Instagram Ads, Google Ads, TikTok Ads, Zalo Ads. 1 file / 1 chiến dịch (hoặc 1 kỳ theo tháng), so được creative/nhóm QC nào tốt.

## Chỉ số theo phễu
| Tầng | Chỉ số chính |
|---|---|
| Hiển thị | Impressions, Reach, Frequency, CPM |
| Thu hút | CTR, CPC, Link click |
| Lead | Số lead, **CPL** (chi phí/lead), tỉ lệ lead chất lượng |
| Chốt | Số đơn, **CPA** (chi phí/đơn), Doanh thu, **ROAS** (doanh thu/chi phí) |

> ROAS < 1 = lỗ. Ngưỡng hoà vốn = 1 / biên lợi nhuận gộp (vd biên 40% → cần ROAS ≥ 2.5).

## Files
```dataview
table period as "Kỳ", channel as "Kênh"
from "03. Areas/Analytics & Reporting/Hiệu Quả Quảng Cáo"
where file.name != this.file.name
sort file.name desc
```

## Liên kết
- [[Tracking Plan]] — pixel/GA4/conversion để đo CPL, CPA, ROAS
- [[_MOC Hiệu Suất Content]] — creative nào (hook/format) đang chạy
- [[_MOC Sales Pipeline & CRM]] — đối chiếu lead ads → deal thật
- [[_MOC Decisions]] — quyết định scale/tắt ngân sách
