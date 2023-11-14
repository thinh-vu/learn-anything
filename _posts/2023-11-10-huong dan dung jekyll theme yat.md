---
layout: post
title: Hướng dẫn cấu hình jekyll theme yat
subtitle: Bài viết thử đầu tiên
author: Thinh Vu
top: 1
categories: jekyll
tags: [guide]
banner:
  image: /assets/images/banners/home.jpeg
---

## Cài đặt Jekyll

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
	- Kiểm tra phiên bản
	
	```shell
	  C:\Users\mrthi>jekyll -v
	jekyll 4.3.2
	```

## YAT theme

URL: https://jeffreytse.github.io/jekyll-theme-yat/about.html
### Thiết lập
- File `Gemfile` chứa thông tin thiết lập về theme được sử dụng, các gói phụ thuộc cần được chỉ rõ. Trong hướng dẫn ban đầu tác giả nêu không đầy đủ do đó khi sử dụng sẽ gặp lỗi khi thiết lập và người dùng không có kinh nghiệm sẽ loay hoay.
- File `_config.yml` chứa tất cả các cài đặt cho site. Uncomment và thay thế các giá trị mặc định để cập nhật.
- Sau khi thay đổi các thông số trên, cần chạy lệnh `bundle` từ thư mục dự án trong terminal để build và phản ánh các thay đổi. Khi chạy server local host, các thay đổi trong bài viết có thể được phản ánh trên browser nhưng các thiết lập trang không tự động thay đổi, ngoại trừ chạy lệnh `bundle`
- Có thể cần chạy `bundle install` để cài đặt các gói phụ thuộc
- Cuối cùng, chạy lệnh `bundle exec jekyll serve` để chạy local server
- Để build (generate site) tại môi trường local, chạy lệnh `bundle exec jekyll build` từ thư mục dự án. Khi chạy lệnh buid, các thay đổi tự động được gán cho nhánh `gh-` 
### Build local hay github action và github page?
- Nên sử dụng local mặc dù mất công thiết lập môi trường (1 lần), về sau chạy lệnh build nhanh chóng và cho phép preview trang để dễ dàng debug. Sau khi thành công hãy push vào 1 nhánh riêng và đẩy lên github page branch để hiển thị.
- Github page chạy mất thời gian, không thể preview, lỗi thì khó debug hơn hoặc reverse lại phiên bản cũ.

## Tính năng
### Viết bài
- Diagram: Có thể sử dụng [PlantUML](https://plantuml.com/guide) hoặc Mermaid
- Table: Hỗ trợ nhiều cài đặt như gộp ô, headless
### Giao diện
- Đặt properties `sidebar: []` để ẩn TOC bên phải
- Cấu hình sidebar tại file `article_menu` tại đường dẫn `jekyll-theme-yat\_includes\sidebar`
- Thay đổi tên `Dark/Light` thành `Tối/Sáng` tại file `jekyll-theme-yat/_includes/extensions/theme-toggle.html`
### Phân tích
- Sửa đổi đoạn mã theo dõi GA thành GTM (nếu cần) tại file `jekyll-theme-yat/_includes/extensions/google-analytics.html`