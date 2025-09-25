---
title: Kiểm tra máy có thể kết nối với Base Check-in Client
nav_order: 5
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

# Kiểm tra máy có thể kết nối với Check-in Client

## Access Directly/Zk 5xxx

- Không chắc chắn có thể kết nối được.
- Phải thử `Thêm thiết bị` để biết Base Check-in Client có kết nối được với máy chấm công hay không.
- Một số dòng máy đã được team kiểm tra và có thể kết nối được: [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
- Tất cả các model máy không có trong danh sách → KHÔNG thể chắc chắn về khả năng kết nối.

## SQL Server

- Đảm bảo có thể truy cập vào SQL Database.
- Đảm bảo dữ liệu chấm công được lưu vào đúng Database.

## Sunbeam/MyTime Cloud

- Đảm bảo phần mềm SunBeam và MyTime đã kết nối thành công, có thể lấy là lưu được dữ liệu chấm công.
- Đảm bảo thông tin đăng nhập là chính xác
- Đảm bảo phần mềm không bị lỗi HPA.

## Các loại kết nối còn lại

- Đảm bảo có thể truy cập được trang quản lý máy chấm công.
- Đảm bảo thông tin đăng nhập là chính xác.

***Thông tin chi tiết về các loại kết nối, tham khảo tại: [Các loại kết nối](../../pages/connections/CONNECTIONS_OVERVIEW.md).***