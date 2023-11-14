---
title: "Lựa chọn nền tảng tạo Digital Garden cho kho tri thức cá nhân"
date: 14-11-2023
category: jamstack
tags: [jekyll, gatsby, digital garden, blog, docs]
banner:
  image: https://images.unsplash.com/photo-1516414447565-b14be0adf13e?q=80&w=1973&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
top: 1
---

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

```mermaid!
graph TD
A[Christmas] -->|Get money| B(Go shopping)
  B --> C{Let me think}
  C -->|One| D[Laptop]
  C -->|Two| E[iPhone]
  C -->|Three| F[fa:fa-car Car]
```

## Quy trình lựa chọn
- Kiến trúc hệ thống: 

```mermaid!
graph TD  

subgraph ChooseStaticSiteGenerator

  A[Define Requirements] -->|Ease of Use, Features| B

  B[Research Options] -->|Jekyll, Gatsby, Hugo, etc.| C

  C[Evaluate Features] -->|Templates, Plugins, Customization| D

  D[Choose Generator] -->|Based on Evaluation| E

end

  

subgraph ChooseHostingPlatform

  F[Select Hosting Platform] -->|GitHub Pages, Netlify, Vercel| G

  G[Configure Deployment] -->|Link Repository, Set Build Commands| H

end

  

subgraph ChooseTheme

  I[Explore Free Themes] -->|Jekyll Themes, Gatsby Starters, etc.| J

  J[Preview Themes] -->|Demo, Customization Options| K

  K[Choose Theme] -->|Based on Preferences| L

end

  

subgraph PublishContent

  M[Create Content] -->|Markdown Files| N

  N[Add Content to Repository] -->|Commit and Push| O

  O[Trigger Build] -->|GitHub/GitLab Actions, Netlify Build| P

  P[View Published Site] -->|Check Deployment URL| Q

end

  

subgraph Iterate

  R[Iterate and Refine] -->|Feedback, Analytics| S

  S[Update Content and Themes] -->|Regular Maintenance| T

end

  

A -->|Personal Blog or Digital Garden?| F

E -->|Specify Theme Preferences| I

L -->|Content Structure| M

Q -->|Satisfied?| R

T -->|Repeat Process| A
```