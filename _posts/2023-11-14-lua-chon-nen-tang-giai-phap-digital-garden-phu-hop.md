---
title: "Lựa chọn nền tảng tạo Digital Garden cho kho tri thức cá nhân"
date: 14-11-2023
layout: post
category: jamstack
tags: [jekyll, gatsby, digital garden, blog, docs, mermaid]
banner:
  image: https://images.unsplash.com/photo-1516414447565-b14be0adf13e?q=80&w=1973&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
top: 1
---

## Tại sao cần chia sẻ?
- **Cho những ý tưởng có cơ hội được chia sẻ:** Viết là quá trình tư duy để giải quyết những vấn đề/câu hỏi cụ thể. Viết thì cần chia sẻ như hít vào cần thở ra vậy.
- **Rèn luyện tư duy logic:** Khi viết ta có thời gian suy nghĩ nhiều hơn về cấu trúc, thông điệp và nhiều yếu tố khác để giúp nội dung truyền đạt tốt nhất đến người xem. Quá trình lặp đi lặp lại này giúp bạn hình thành một kỹ năng và phong cách trình bày nội dung mạch lạc.
## Phong cách

### Giao diện
- Digital Garden: ghi chú không chuyên nghiệp, tập trung vào ý tưởng và liên kết. Thúc đẩy hình thành thói quen viết, không cầu toàn về hoàn thiện.
- Blog: Chỉn chu, chuyên nghiệp về nội dung và hình thức. Tối ưu cho máy tìm kiếm để có traffic về blog.
- Trang tài liệu: trình bày các tài liệu kỹ thuật, hướng dẫn sử dụng sản phẩm. Giao diện thường đơn giản, tập trung vào nội dung chính về hướng dẫ

### Trình bày nội dung
- Thuần ghi chú cơ bản văn xuôi với markdown, chèn ảnh và media
- Ghi chú khoa học với công thức toán học, cần dùng Latex, code

## Tính năng cân nhắc

- Tìm kiếm
- Markdown
- Wikilink, Tag
- Graph View
- Blog Style

## Quy trình lựa chọn
- Kiến trúc hệ thống: 

```mermaid!
graph TD

subgraph Basics
  A[Define Requirements] -->|Ease of Use, Features| B
  B[Choose Static Site Generator] -->|Jekyll, Gatsby, Hugo, etc.| C
  C[Select Hosting Platform] -->|GitHub Pages, Netlify, Vercel| D
end

subgraph ThemesAndContent
  D[Explore Free Themes] -->|Jekyll, Gatsby, etc.| E
  E[Choose Theme] -->|Based on Preferences| F
  F[Create Content] -->|Markdown Files| G
end

subgraph Publish
  G[Add Content to Repository] -->|Commit and Push| H
  H[Configure Deployment] -->|Link Repository, Set Build Commands| I
  I[Trigger Build] -->|GitHub/GitLab Actions, Netlify Build| J
  J[View Published Site] -->|Check Deployment URL| K
end

subgraph Iterate
  K[Iterate and Refine] -->|Feedback, Analytics| L
  L[Update Content and Themes] -->|Regular Maintenance| M
end

A -->|Personal Blog or Digital Garden?| C
F -->|Content Structure| G
K -->|Satisfied?| A
M -->|Repeat Process| A
```