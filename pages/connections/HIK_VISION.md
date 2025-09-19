---
title: HIK Vision
parent: Các loại kết nối
nav_order: 4
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# HIK Vision

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).  
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

<img src="{{site.baseurl}}/assets/images/setting_hik_vision.png" alt="HIK Vision">

## Mô tả

- Để có thể quản lý và vận hành máy chấm công HIKVision thì ngoài thiết bị phần cứng ra cần phải có một hệ thống đi kèm chuyên lưu trữ thông tin cũng như quản lý dữ liệu của mỗi thiết bị.

- Base Check-in Client có khả năng kết nối và đọc dữ liệu chấm công thông qua trang quản lý thiết bị riêng của HIKVision. Không kết nối trực tiếp đến máy chấm công HIKVision.

## Hướng dẫn cài đặt

- Truy cập phần cài đặt của máy chấm công, chọn Cài đặt mạng để biết IP của máy chấm công

<img src="{{site.baseurl}}/assets/images/hik_ip_address.jpeg" alt="HIK Vision Device IP">

- Truy cập trang quản lí thiết bị của HIKVision thông qua IP của máy chấm công
- ***Lưu ý***: Khi không truy cập được trang admin như ở dưới nghĩa là dòng máy này không hỗ trợ kết nối từ bên ngoài.

<img src="{{site.baseurl}}/assets/images/hik_web_ip.jpeg" alt="HIK Vision Admin Page">

<img src="{{site.baseurl}}/assets/images/hik_vision_admin_new_version.png" alt="HIK Vision Admin Page">

- ***Lấy thông tin cổng kết nối***: Truy cập trang quản lý máy chấm công trên trình duyệt bằng địa chỉ IP máy chấm công -> Vào phần Cài đặt mạng -> Cài đặt nâng cao cổng kết nối. Để ý giá trị cổng kết nối cho 2 loại giao thức mạng HTTP và HTTPS. Mặc định, giá trị này là 80 cho HTTP và 443 cho HTTPS. Nếu có thay đổi thì cần nhập đúng giá trị này vào phần cài đặt của Base Check-in Client.
- Nếu sử dụng giá trị cổng kết nối tương ứng với giao thức HTTPS, lưu ý chọn `Sử dụng HTTPS`.

<img src="{{site.baseurl}}/assets/images/hik_vision_port_setting_1.png" alt="HIK Vision Port Setting 1">

<img src="{{site.baseurl}}/assets/images/hik_vision_port_setting_2.png" alt="HIK Vision Port Setting 2">


## Hướng dẫn sử dụng

- Sau khi kết nối lần đầu tiên, ứng dụng sẽ tự động chạy đồng bộ dữ liệu trong 3 ngày gần nhất.
- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).
- Khi thay đổi thời gian bắt đầu đồng bộ, vui lòng thực hiện theo các bước sau: `Tạm dừng đồng bộ` -> `Thay đổi thời gian đồng bộ` -> `Đồng bộ bản ghi`.

<img src="{{site.baseurl}}/assets/images/hik_vision_change_sync_from.png" alt="HIK Vision Device Change Sync From">

<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">

- Khi chọn `Đồng bộ từ thiết bị` để đồng bộ tất cả thiết bị đã thêm trong máy → ứng dụng sẽ đồng bộ dữ liệu trong ngày hiện tại.
- Mỗi 2 phút, ứng dụng sẽ tự thực hiện đồng bộ dữ liệu trong 2 ngày gần nhất.
