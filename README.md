# INT3105_2 (tuần 1)
***
##### Họ và tên: Lê Minh Đức
##### MSV: 23021532
### 1. Docker, Docker-compose là gì?
- **Docker** là một nền tảng mã nguồn mở giúp ta đóng gói (package), phân phối, và chạy ứng dụng trong các container.
- **Docker** Compose là một công cụ đi kèm Docker giúp ta định nghĩa và quản lý nhiều container cùng lúc thông qua một file cấu hình (thường là docker-compose.yml).
### 2. Linux vs Unix vs BSD hay *Nix, macOS thuộc loại nào?
#### `Linux`
- Linux (1991, Linus Torvalds) là kernel mã nguồn mở, sau này + GNU tools thành hệ điều hành "GNU/Linux".

- Linux không phải Unix gốc, nhưng được thiết kế theo chuẩn Unix-like (giống Unix).

- Các bản phổ biến: Ubuntu, Debian, Fedora, Arch, RedHat, SUSE…

- Linux không được chứng nhận Unix, nhưng gần như ai cũng xếp nó vào Unix-like.
#### `Unix`
- Unix là một hệ điều hành gốc, ra đời từ thập niên 1970 tại Bell Labs (AT&T).

- Nó đặt nền móng cho hầu hết hệ điều hành hiện đại (triết lý "mọi thứ là file", công cụ nhỏ ghép lại được…).

- Các bản Unix "chuẩn" (chính thống) được gọi là Unix-certified (chuẩn POSIX, The Open Group chứng nhận).
### `BSD` 
- BSD (Berkeley Software Distribution) là nhánh hệ điều hành phát triển từ Unix gốc (Unix V6 từ AT&T).

- Do đó BSD là hậu duệ trực tiếp của Unix.

- Có nhiều biến thể: FreeBSD, OpenBSD, NetBSD, DragonFlyBSD.

- Một số hệ điều hành khác dựa trên BSD:

    - macOS, iOS, iPadOS, tvOS, watchOS (Apple dùng Darwin kernel, vốn dựa trên BSD + Mach).

    - PlayStation OS cũng dùng FreeBSD
### `Nix`
- "*nix" là cách viết tắt (wildcard) để chỉ chung các hệ điều hành "giống Unix" (Unix hoặc không phải Unix nhưng theo chuẩn POSIX).

- Bao gồm:

    - Unix thương mại (Solaris, AIX, HP-UX).

    - BSD và hậu duệ của nó.

    - Linux (dù không phải con cháu trực tiếp).

- Tóm lại: *tất cả Unix-like được gọi chung là nix
### `macOS` thuộc loại nào?
- macOS dựa trên Darwin, kết hợp giữa Mach kernel và nhiều thành phần BSD.

- macOS là Unix chính thống (Unix-certified).

- Nó cũng được xem là BSD-based Unix.
### 3. Alpine vs Ubuntu
#### `Ubuntu`
- Nguồn gốc: Dựa trên Debian.

- Kích thước image Docker: ~70–80 MB (minimal) → khá lớn so với Alpine.

- Package manager: apt (Advanced Package Tool).

- **Ưu điểm**:

    - Dễ dùng, nhiều tài liệu, cộng đồng lớn.

    - Nhiều package sẵn, ít phải build thủ công.

    - Hỗ trợ tốt cho development, CI/CD, production.

- **Nhược điểm**:

    - Image nặng hơn (tốn dung lượng, thời gian pull).

    - Bảo mật ổn nhưng bề mặt tấn công rộng hơn (nhiều package hơn).
#### `Alpine`
- Nguồn gốc: Độc lập, không dựa trên Debian/Ubuntu.

- Kích thước image Docker: ~5 MB (!) → cực nhẹ.

- Package manager: apk (Alpine Package Keeper).

- **Ưu điểm**:

    - Nhỏ gọn → image Docker siêu nhẹ, tải nhanh.

    - Bảo mật cao (ít package mặc định).

    - Thích hợp cho microservices, container hóa.

- **Nhược điểm**:

    - Thiếu nhiều thư viện, đôi khi phải build từ source.

    - Dùng musl libc thay vì glibc, đôi khi gây lỗi tương thích (một số app C/C++ không chạy ổn).

    - Debug khó hơn vì thiếu công cụ
### 4. `VNC`
VNC, hay Virtual Network Computing, là một hệ thống cho phép người dùng tương tác với một máy tính từ xa thông qua một kết nối mạng. Nó truyền tải sự kiện chuột và bàn phím từ máy khách (client) đến máy chủ (server) và trả lại các cập nhật màn hình.

VNC được sử dụng rộng rãi trong việc hỗ trợ kỹ thuật từ xa, quản lý máy chủ, giáo dục và nhiều ứng dụng khác. Nó hoạt động trên nhiều hệ điều hành, bao gồm Windows, macOS, Linux và nhiều hệ điều hành di động.

#### Điểm mạnh:

- **Độc lập với nền tảng**: VNC hoạt động trên nhiều hệ điều hành, bao gồm Windows, macOS, Linux và nhiều hệ điều hành di động.

- **Đơn giản và dễ sử dụng**: VNC dễ cài đặt và sử dụng, ngay cả với những người không có nhiều kinh nghiệm về công nghệ.

- **Cho phép truy cập từ xa**: VNC cho phép người dùng tương tác với máy tính từ xa, giúp hỗ trợ kỹ thuật, quản lý máy chủ, giáo dục và nhiều ứng dụng khác.

#### Điểm hạn chế:

- **Hiệu suất**: VNC có thể chậm hơn so với một số giải pháp truy cập từ xa khác, đặc biệt là khi mạng chậm hoặc không ổn định.

- **Bảo mật**: Mặc dù VNC có thể được cấu hình để sử dụng mã hóa, nhưng nó không được bật theo mặc định, có thể tạo ra các vấn đề bảo mật.