---
title: SQL Server
parent: Các loại kết nối
nav_order: 8
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# SQL Server

## Mô tả

- Phần lớn các phần mềm quản lý máy chấm công như RonalJackPro, SunBeam, MyTime, MitaPro, WiseEye, etc. khi hoạt động sẽ tạo cơ sở dữ liệu sử dụng SQL Server hoặc Microsoft Access.
- Base Check-in Client hỗ trợ kết nối và lấy dữ liệu trực tiếp từ cơ sở dữ liệu sử dụng SQL Server.
- Lúc này, phần mềm quản lý máy chấm công của hãng sẽ chịu trách nhiệm lấy dữ liệu về máy tính và lưu vào cơ sở dữ liệu → Base Check-in Client sẽ đọc dữ liệu được lưu và đẩy lên HRM.

## Hướng dẫn kết nối

- Đảm bảo phần mềm quản lý sử dụng SQL Server.
- Mỗi Database Engine sẽ có cách đăng nhập khác nhau, tuỳ thuộc vào cài đặt của người dùng hoặc thiết lập trong phần mềm của nhà sản xuất.
- Nếu sử dụng Windows Authentication, có thể kiểm tra tên đăng nhập như sau: Mở Terminal/CMD trên window và gõ lệnh `hostname`:

<img src="{{site.baseurl}}/assets/images/cmd_hostname.png" alt="Check Hostname">

- Vậy username sẽ là “DESKTOP-T8MIU7U”. Mật khẩu cho tài khoản này sẽ là `0`.
- Dưới đây là dữ liệu kết nối mẫu đến SQL Server của phần mềm MitaPro:

<img src="{{site.baseurl}}/assets/images/sql_mitaco_sample_filled.png" alt="SQL Server Connection">

## Hướng dẫn sử dụng

- Sau khi kết nối thành công phần mềm sẽ tự động kiểm tra database mỗi 2ph/lần.
- Nếu database có dữ liệu chấm công mới thì phần mềm sẽ tự động lấy và đẩy dữ liệu đó lên HRM
- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).

<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">