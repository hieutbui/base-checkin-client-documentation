---
title: ZK BioTime 8 & 9
parent: Các loại kết nối
nav_order: 15
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# ZK BioTime 8 & 9

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

- Các máy chấm công ZKTeco sẽ sử dụng phần mềm quản lý ***Zk Bio Time 8 & 9*** riêng dưới dạng web-based.
- Base Checkin Client có khả năng kết nối đến phần mềm này và đọc dữ liệu chấm công thông qua ZK BioTime API do ZKTeco cung cấp.

## Hướng dẫn cài đặt

- Truy cập vào trang quản lý `ZK BioTime`, đảm bảo các thông tin `Username` và `Password` là chính xác.
- ⚠️ Vui lòng liên hệ ZKTeco nếu không tìm được các thông tin này.

<img src="{{site.baseurl}}/assets/images/zk_biotime_login.png" alt="ZK BioTime Login">

- Chọn loại thiết bị ZK BioTime và điền đầy đủ các thông tin bắt buộc.

<img src="{{site.baseurl}}/assets/images/select_zk_biotime.png" alt="Select ZK BioTime">


## Hướng dẫn sử dụng

- Sau khi kết nối lần đầu tiên, ứng dụng sẽ tự động chạy đồng bộ dữ liệu trong 3 ngày gần nhất.

- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).

<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">

- Mỗi 2 phút, ứng dụng sẽ tự thực hiện đồng bộ dữ liệu trong 4 ngày gần nhất.