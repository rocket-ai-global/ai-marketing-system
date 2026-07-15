---
created: 2026-07-15
status: replaced-and-verified
platform: Facebook Page
page: Tony Trieu AI
page_id: "112793447211604"
reason: "Old scheduled SVG visuals looked too basic/template-like; Tony approved replacement with GPT image/image2 premium style."
image_model: openai-codex/gpt-image-2-medium
timezone: Asia/Ho_Chi_Minh
posting_time: "07:00"
tags: [facebook, rocketai, content-queue, premium-visuals, image2, aios]
---

# Replaced Facebook Queue — Premium GPT Image2 Visuals

## Summary

Tony reported the 07:00 post image looked bad/basic. Root cause: deterministic SVG layout was text-safe but not visually premium enough for public Facebook content.

Action completed:

1. Generated 7 new premium GPT image2 visuals using `openai-codex/gpt-image-2-medium`.
2. Vision-reviewed the visuals for large text/artifact/fake-claim risks.
3. Uploaded all images to direct image URLs and verified `image/png` MIME.
4. Deleted the old low-quality live post and 6 scheduled posts.
5. Re-created today's post immediately with premium visual.
6. Re-scheduled the remaining 6 posts at 07:00 Asia/Ho_Chi_Minh.
7. Verified D1 live and D2-D7 scheduled/unpublished via Facebook API.

## Deleted old post IDs

- `112793447211604_1493744432765873` — old D1 live post
- `112793447211604_1493744379432545` — old D2 scheduled
- `112793447211604_1493744399432543` — old D3 scheduled
- `112793447211604_1493744479432535` — old D4 scheduled
- `112793447211604_1493744569432526` — old D5 scheduled
- `112793447211604_1493744599432523` — old D6 scheduled
- `112793447211604_1493744586099191` — old D7 scheduled

## New live/scheduled queue

| Day | Date | Status | Facebook Post ID | Photo ID | Image URL |
|---|---|---|---|---|---|
| D1 | 2026-07-15 | live | `112793447211604_1494002336073416` | `1494002306073419` | https://files.catbox.moe/gjbthi.png |
| D2 | 2026-07-16 07:00 | scheduled / unpublished | `112793447211604_1494002326073417` | `1494002326073417` | https://files.catbox.moe/vccwr6.png |
| D3 | 2026-07-17 07:00 | scheduled / unpublished | `112793447211604_1494002386073411` | `1494002386073411` | https://files.catbox.moe/82j1ai.png |
| D4 | 2026-07-18 07:00 | scheduled / unpublished | `112793447211604_1494002376073412` | `1494002376073412` | https://files.catbox.moe/kyahnv.png |
| D5 | 2026-07-19 07:00 | scheduled / unpublished | `112793447211604_1494002472740069` | `1494002472740069` | https://files.catbox.moe/qydcny.png |
| D6 | 2026-07-20 07:00 | scheduled / unpublished | `112793447211604_1494002512740065` | `1494002512740065` | https://files.catbox.moe/ja7xg4.png |
| D7 | 2026-07-21 07:00 | scheduled / unpublished | `112793447211604_1494002486073401` | `1494002486073401` | https://files.catbox.moe/kd7rpr.png |

## Verified live link

- D1 live permalink: https://www.facebook.com/1493715246102125/posts/1494002336073416
- D1 photo link: https://www.facebook.com/photo.php?fbid=1494002306073419&set=a.464395962367397&type=3

## Local image assets

- D1: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_071007_11d9e2d3.png`
- D2: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_071810_d3969d46.png`
- D3: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_071913_7c76b891.png`
- D4: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_072018_91862416.png`
- D5: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_072329_fdb8676f.png`
- D6: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_072434_40f77ea3.png`
- D7: `/Users/x/.hermes/cache/images/openai_codex_gpt-image-2-medium_20260715_072539_89e7fa0e.png`

## Rule update for future posts

For public Facebook posts:

- Avoid plain SVG template visuals unless explicitly approved.
- Use GPT image/image2 premium visual style for brand perception.
- Keep image text short and mostly English/simple labels to reduce rendering errors.
- Vision review every image before posting/scheduling.
- If image contains critical Vietnamese text, use deterministic overlay or manual design review.
