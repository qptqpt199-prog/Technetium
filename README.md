# Technetium

Technetium là bộ công cụ tiện ích hệ thống dành cho Windows, được xây dựng bằng C++ và Qt Widgets. Ứng dụng tập hợp nhiều chức năng thường dùng trong một giao diện duy nhất, nhẹ, chạy portable (không cần cài đặt), hỗ trợ song song tiếng Việt và tiếng Anh (cùng một số ngôn ngữ khác ở mức hỗ trợ cơ bản).

---

## Mục lục

- [Đổi tên hàng loạt](#đổi-tên-hàng-loạt)
- [Lịch sử đổi tên và Hoàn tác](#lịch-sử-đổi-tên-và-hoàn-tác)
- [Hiệu năng hệ thống](#hiệu-năng-hệ-thống)
- [Dọn dẹp hệ thống](#dọn-dẹp-hệ-thống)
- [Lịch dọn dẹp tự động](#lịch-dọn-dẹp-tự-động)
- [Chuyển đổi định dạng ảnh](#chuyển-đổi-định-dạng-ảnh)
- [Đa ngôn ngữ](#đa-ngôn-ngữ)
- [Tải về và cài đặt](#tải-về-và-cài-đặt)
- [Công nghệ sử dụng](#công-nghệ-sử-dụng)
- [Giới hạn đã biết](#giới-hạn-đã-biết)
- [Đóng góp](#đóng-góp)
- [Giấy phép](#giấy-phép)

---

## Đổi tên hàng loạt

Cho phép chọn nhiều file cùng lúc và đổi tên theo quy tắc chung, thay vì phải sửa thủ công từng file một.

- Thêm tiền tố, hậu tố vào tên file hàng loạt.
- Đánh số thứ tự tự động, có thể chọn số bắt đầu.
- Tìm và thay thế một đoạn ký tự trong tên file.
- Xem trước kết quả tên file mới trước khi áp dụng thật.
- Hoạt động trên nhiều định dạng file bất kỳ, không giới hạn loại file.

[Về đầu mục lục](#mục-lục)

---

## Lịch sử đổi tên và Hoàn tác

Mọi thao tác đổi tên hàng loạt đều được ghi lại, tránh tình trạng đổi nhầm mà không thể quay lại.

- Lưu lại tối đa 25 lần đổi tên gần nhất, lưu vĩnh viễn giữa các lần mở ứng dụng.
- Xem chi tiết từng lần đổi tên: file nào đã đổi từ tên gì sang tên gì.
- Hoàn tác (Undo) từng lần thao tác một cách độc lập.
- Tự động bỏ qua trong lúc hoàn tác nếu file đã bị xóa, di chuyển hoặc đang bị khóa bởi chương trình khác, không làm gián đoạn toàn bộ quá trình.

[Về đầu mục lục](#mục-lục)

---

## Hiệu năng hệ thống

Theo dõi tình trạng sử dụng tài nguyên máy tính theo thời gian thực.

- Biểu đồ mức sử dụng CPU theo thời gian thực.
- Biểu đồ mức sử dụng RAM theo thời gian thực.
- Cập nhật liên tục, không cần làm mới thủ công.

[Về đầu mục lục](#mục-lục)

---

## Dọn dẹp hệ thống

Quét và dọn dẹp các loại dữ liệu rác phổ biến trên Windows, giúp giải phóng dung lượng ổ đĩa.

Các nhóm dữ liệu được hỗ trợ:

- Tệp tin tạm (Temporary files)
- Thùng rác (Recycle Bin)
- Bộ nhớ đệm trình duyệt (Browser cache)
- Bộ nhớ đệm Windows Update
- Bộ nhớ đệm hình thu nhỏ (Thumbnail cache)
- Dữ liệu Prefetch
- Tệp kết xuất sự cố bộ nhớ (Memory dump files)
- Bộ nhớ đệm shader (Shader cache)
- Tệp tối ưu hóa phân phối (Delivery Optimization)
- Báo cáo lỗi hệ thống (Windows Error Reporting)
- Tệp còn sót lại sau khi gỡ driver

Người dùng xem trước dung lượng từng nhóm trước khi quyết định xóa, có thể chọn xóa riêng từng nhóm hoặc nhiều nhóm cùng lúc.

[Về đầu mục lục](#mục-lục)

---

## Lịch dọn dẹp tự động

Thiết lập lịch để Technetium tự động quét và dọn dẹp định kỳ mà không cần mở ứng dụng thủ công mỗi lần.

- Hỗ trợ 2 kiểu lịch: lặp lại đơn giản theo số ngày cố định, hoặc lịch nâng cao (hàng ngày, hàng tuần theo thứ cụ thể, hàng tháng theo ngày cụ thể).
- Chọn riêng những nhóm dữ liệu muốn dọn tự động, độc lập với lựa chọn ở phần dọn dẹp thủ công.
- Khi đến giờ hẹn, ứng dụng quét trước, hiển thị thông báo, chờ 60 giây để người dùng có thể hủy nếu muốn, sau đó mới tự động chuyển dữ liệu vào Thùng rác.
- Lịch dọn dẹp tự động không bao giờ xóa vĩnh viễn dữ liệu, chỉ chuyển vào Thùng rác, đảm bảo luôn có thể khôi phục nếu cần.
- Khi bật tính năng này, ứng dụng sẽ ẩn xuống khay hệ thống (system tray) thay vì đóng hẳn khi bấm nút đóng cửa sổ, để lịch có thể tiếp tục hoạt động ở chế độ nền.
- Nếu tắt tính năng này, ứng dụng hoạt động và đóng như một chương trình thông thường.

[Về đầu mục lục](#mục-lục)

---

## Chuyển đổi định dạng ảnh

Chuyển đổi hàng loạt file ảnh trong một thư mục sang định dạng khác.

- Tự động quét toàn bộ ảnh hợp lệ trong thư mục, bất kể đuôi file gốc là gì, tự bỏ qua các file không phải ảnh.
- Hỗ trợ chuyển đổi sang PNG, JPG, BMP, ICO.
- Khi chuyển sang ICO, có thể chọn độ phân giải đích cố định (16, 32, 48, 64, 128, 256 pixel).
- Có thể chọn thư mục lưu riêng, hoặc lưu lại ngay trong thư mục nguồn.
- Tự động xử lý trùng tên: nếu kết quả chuyển đổi trùng tên với một file khác, tự động thêm hậu tố để tránh ghi đè ngoài ý muốn.
- Tùy chọn xóa file ảnh gốc ngay sau khi chuyển đổi thành công, dành cho trường hợp muốn thay thế hẳn định dạng cũ.

[Về đầu mục lục](#mục-lục)

---

## Đa ngôn ngữ

Giao diện hỗ trợ nhiều ngôn ngữ, chuyển đổi ngay lập tức không cần khởi động lại ứng dụng.

- Tiếng Việt và tiếng Anh được dịch đầy đủ toàn bộ giao diện.
- Hỗ trợ thêm tiếng Trung, tiếng Pháp, tiếng Tây Ban Nha, tiếng Ả Rập, tiếng Nga, tiếng Hindi ở mức cơ bản. Những câu chưa có bản dịch sẽ tự động hiển thị bằng tiếng Anh thay vì để trống.
- Rất hoan nghênh đóng góp bản dịch đầy đủ hơn cho các ngôn ngữ này từ cộng đồng (xem phần Đóng góp bên dưới).

[Về đầu mục lục](#mục-lục)

---

## Tải về và cài đặt

Technetium được phát hành dưới dạng bản portable, không cần cài đặt.

1. Tải file nén bản phát hành mới nhất từ mục Releases.
2. Giải nén ra một thư mục bất kỳ.
3. Chạy trực tiếp file `Technetium.exe`.

Lưu ý: nếu di chuyển hoặc đổi tên thư mục chứa ứng dụng sau khi đã tạo shortcut, cần mở lại file `Technetium.exe` thật một lần để ứng dụng tự cập nhật lại đường dẫn shortcut.

[Về đầu mục lục](#mục-lục)

---

## Công nghệ sử dụng

- Ngôn ngữ: C++
- Giao diện: Qt Widgets (Qt 6)
- Hệ thống build: CMake
- Trình biên dịch: MinGW 64-bit
- Nền tảng hỗ trợ: Windows

[Về đầu mục lục](#mục-lục)

---

## Giới hạn đã biết

- Lịch dọn dẹp tự động không thể hoạt động nếu máy tính đang trong trạng thái tắt hẳn (shutdown). Khi mở lại ứng dụng, Technetium sẽ tự kiểm tra và chạy bù nếu đã quá hạn lịch hẹn.
- Để lịch dọn dẹp hoạt động sau khi khởi động lại máy, cần tự bật quyền khởi động cùng Windows trong phần cài đặt hệ thống (ứng dụng sẽ hướng dẫn cụ thể trong lúc thiết lập).
- Khi chuyển đổi ảnh sang định dạng ICO, mỗi file chỉ chứa đúng một độ phân giải được chọn, không tự gộp nhiều kích thước vào cùng một file như một số công cụ chuyên dụng khác.

[Về đầu mục lục](#mục-lục)

---

## Đóng góp

Mọi đóng góp đều được hoan nghênh, đặc biệt là:

- Bổ sung bản dịch cho các ngôn ngữ đang hỗ trợ ở mức cơ bản (Trung, Pháp, Tây Ban Nha, Ả Rập, Nga, Hindi).
- Báo lỗi hoặc đề xuất tính năng thông qua mục Issues.

[Về đầu mục lục](#mục-lục)

---

## Giấy phép

Thông tin giấy phép sẽ được bổ sung.

[Về đầu mục lục](#mục-lục)
