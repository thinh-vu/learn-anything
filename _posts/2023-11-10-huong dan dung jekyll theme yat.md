---
layout: post
title: Hướng dẫn cấu hình Jekyll theme YAT cho Blog
subtitle: Cách thiết lập Jekyll blog như trang hiện tại
author: Thinh Vu
top: 2
categories: jamstack
tags: [guide, jekyll]
banner:
  image: https://images.unsplash.com/photo-1502945015378-0e284ca1a5be?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---
## Cài đặt Jekyll

> Tùy chọn cài đặt Jekyll nếu bạn muốn preview trang trên máy tính cục bộ (localhost), nếu không cài trên máy sẽ khó và mất thời gian hơn chút khi tùy biến trang web. Tuy nhiên, nếu không cài m đẩy mã nguồn lên Github page vẫn có thể hiển thị website bình thường.

- Hướng dẫn: [tại đây](https://jekyllrb.com/docs/installation/windows/)
- Chi tiết:
	- Tải [Ruby Installer](https://rubyinstaller.org/downloads/) cho Windows
	- Mặc định chọn `ridk install` ở bước cài đặt cuối cùng của Wizard
	- Trong terminal/command prompt chạy sau khi kết thúc Wizard, nhập `3` cho tùy chọn tương ứng `MSYS2 and MINGW development tool chain`
	 ![demo](/assets/images/Pasted image 20231110213146.png)
	- Mở cửa sổ mới cho Terminal/command prompt, chạy lệnh `gem install jekyll bundler`
	  ![](/assets/images/Pasted image 20231110213006.png)
	- Cập nhật phiên bản mới theo hướng dẫn nếu cần. Ví dụ `gem update --system 3.4.22`
	  ![](/assets/images/Pasted image 20231110213041.png)
	- Kiểm tra phiên bản `jekyll -v`

## YAT theme

> Để sao chép giao diện đang hiển thị của trang web này, bạn có thể clone mã nguồn github [tại đây](https://github.com/thinh-vu/learn-anything)

Bạn cũng có thể truy cập trang dự án của giao diện nguyên bản trên Github: [yekyll theme yat](https://jeffreytse.github.io/jekyll-theme-yat/about.html)

### Thiết lập
- File `Gemfile` chứa thông tin thiết lập về theme được sử dụng, các gói phụ thuộc cần được chỉ rõ. Trong hướng dẫn ban đầu tác giả nêu không đầy đủ do đó khi sử dụng sẽ gặp lỗi khi thiết lập và người dùng không có kinh nghiệm sẽ loay hoay.
- File `_config.yml` chứa tất cả các cài đặt cho site. Uncomment và thay thế các giá trị mặc định để cập nhật.
- Có thể cần chạy `bundle install` để cài đặt các gói phụ thuộc
- Cuối cùng, chạy lệnh `bundle exec jekyll serve` để chạy local server và xem trước nội dung để có thể tùy biến trang web.
- Để build (generate site) tại môi trường local, chạy lệnh `bundle exec jekyll build` từ thư mục dự án. Khi chạy lệnh buid, các thay đổi tự động được gán cho nhánh `gh-` 
### Build local hay github action và github page?
- Nên sử dụng local mặc dù mất công thiết lập môi trường (1 lần), về sau chạy lệnh build nhanh chóng và cho phép preview trang để dễ dàng debug. Sau khi thành công hãy push vào 1 nhánh riêng và đẩy lên github page branch để hiển thị.
- Github page chạy mất thời gian, không thể preview, lỗi thì khó debug hơn hoặc reverse lại phiên bản cũ.

## Tính năng
### Viết bài
- Diagram: Có thể sử dụng [PlantUML](https://plantuml.com/guide) hoặc Mermaid
- Table: Hỗ trợ nhiều cài đặt như gộp ô, headless
- Hỗ trợ đa dạng các cú pháp markdown cơ bản lẫn nâng cao.


### Giao diện
- Đặt properties `sidebar: []` để ẩn TOC bên phải
- Cấu hình sidebar tại file `article_menu` tại đường dẫn `jekyll-theme-yat\_includes\sidebar`
- Thay đổi tên `Dark/Light` thành `Tối/Sáng` tại file `jekyll-theme-yat/_includes/extensions/theme-toggle.html`
- Thay đổi màu sắc chủ đạo cho theme trong `_config.yml`

### Phân tích
- Sửa đổi đoạn mã theo dõi GA thành GTM (nếu cần) tại file `jekyll-theme-yat/_includes/extensions/google-analytics.html`