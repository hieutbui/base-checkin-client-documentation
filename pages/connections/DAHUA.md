---
title: Dahua
parent: Các loại kết nối
nav_order: 14
---

# Dahua

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

- Các máy chấm công Dahua sẽ sử dụng phần mềm quản lý riêng dưới dạng web-based.
- Base Checkin Client có khả năng kết nối đến phần mềm này và đọc dữ liệu chấm công thông qua Dahua API do Dahua cung cấp. Các dữ liệu chấm công sẽ được phân biệt dựa trên `UserID`.

## Hướng dẫn cài đặt

- Truy cập vào trang quản lý `Dahua Web Service`, đảm bảo các thông tin `Username` và `Password` là chính xác.
- ⚠️ Vui lòng liên hệ Dahua nếu không tìm được các thông tin này.

<img src="{{site.baseurl}}/assets/images/dahua_web_service_login.png" alt="Dahua Web Service">

- Chọn loại thiết bị Dahua và điền đầy đủ các thông tin bắt buộc.

<img src="{{site.baseurl}}/assets/images/select_dahua.png" alt="Select Dahua">