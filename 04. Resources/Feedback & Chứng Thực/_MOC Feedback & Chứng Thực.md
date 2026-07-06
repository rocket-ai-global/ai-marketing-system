---
tags: [moc, resource, feedback]
created: 2026-07-07
---

# MOC — Feedback & Chứng Thực Khách Hàng

> Thư viện **dùng chung** mọi phản hồi từ khách: lời khen (testimonial), đánh giá (review), câu chuyện thành công (case study), và góp ý/khiếu nại. Là **bằng chứng xã hội** để Marketing viết content, Sale xử lý từ chối, Offer chứng minh giá trị (Value Equation) — đồng thời là **tín hiệu cải thiện** cho sản phẩm & chăm sóc khách.
>
> Đặt ở `04. Resources/` vì tái sử dụng nhiều nơi. Mỗi feedback link về [[People]]/[[Companies]] (ai nói) + sản phẩm liên quan trong [[_MOC Sản Phẩm & Dịch Vụ]].

## Phân loại bằng frontmatter `type`
| `type` | Là gì | Dùng để |
|---|---|---|
| `testimonial` | Lời khen ngắn, trích dẫn được | Landing, ads, social proof |
| `review` | Đánh giá công khai (Google/Fanpage/Shopee) | Uy tín, phản hồi công khai |
| `case-study` | Câu chuyện chi tiết before→after có số | Bán high-ticket, content chiều sâu |
| `gop-y` | Góp ý cải thiện | Nâng cấp sản phẩm/dịch vụ |
| `khieu-nai` | Khiếu nại/phàn nàn | Xử lý & phòng churn |

Mỗi note thêm: `rating` (1–5 nếu có), `product` (link sản phẩm), `nguon` (kênh/nơi khách nói), `xin_phep_dung` (đã xin phép dùng công khai chưa: yes/no).

## Testimonial & Case study (bằng chứng tốt — dùng cho marketing)
```dataview
table type as "Loại", rating as "Sao", product as "Sản phẩm", xin_phep_dung as "Được dùng?"
from "04. Resources/Feedback & Chứng Thực"
where type = "testimonial" or type = "review" or type = "case-study"
sort rating desc
```

## Góp ý & Khiếu nại (tín hiệu cải thiện)
```dataview
table type as "Loại", product as "Sản phẩm", nguon as "Nguồn"
from "04. Resources/Feedback & Chứng Thực"
where type = "gop-y" or type = "khieu-nai"
sort file.ctime desc
```

## Liên kết
- Hình/video review, testimonial quay clip → `Media/` trong thư mục này
- Sản phẩm được khen/chê: [[_MOC Sản Phẩm & Dịch Vụ]]
- Góp ý/khiếu nại → hành động chăm sóc: [[_MOC Customer Success & Retention]]
- Chấm điểm offer bằng chứng thực: [[thiet-ke-offer]] · so với đối thủ [[_MOC Đối Thủ]]
- Lý do inbox/khiếu nại từ chat: [[_MOC Chăm Sóc Khách Hàng (Chat)]]
