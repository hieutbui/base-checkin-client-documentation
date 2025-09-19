---
title: Nuveq
parent: Các loại kết nối
nav_order: 10
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Nuveq

## Mô tả

- Các máy chấm công Nuveq sẽ sử dụng phần mềm quản lý riêng dưới dạng web-based.
- Base Checkin Client có khả năng kết nối đến phần mềm này và đọc dữ liệu chấm công thông qua Nuveq Cloud API của Nuveq. Các dữ liệu chấm công sẽ được phân biệt dựa trên `staffNo`.

## Hướng dẫn cài đặt

- Truy cập trang quản lý `Nuveq Portal`, đăng nhập sử dụng tài khoản do Nuveq cung cấp để lấy các thống tin ***api_id*** và ***token_key***. 
- ⚠️ Vui lòng liên hệ Nuveq nếu không tìm được các thông tin này.

<img src="{{site.baseurl}}/assets/images/nuveq_portal_login.png" alt="Nuveq Portal">

- Chọn loại thiết bị Nuveq và điền đầy đủ các thông tin bắt buộc.

<img src="{{site.baseurl}}/assets/images/select_nuveq.png" alt="Select Nuveq">

<img src="{{site.baseurl}}/assets/images/nuveq_filled_data.png" alt="Nuveq Connection">

## Một số lưu ý khi sử dụng

- Sau khi kết nối lần đầu tiên, ứng dụng sẽ tự động đồng bộ dữ liệu trong 3 ngày gần nhất. Để thay đổi ngày bắt đầu đồng bộ, chọn `Chỉnh sửa thiết bị` và `lựa chọn thời gian đồng bộ`. Thời gian đồng bộ ***KHÔNG*** vượt quá `3 tháng` trước so với hiện tại.

<img src="{{site.baseurl}}/assets/images/select_edit_device.png" alt="Nuveq Edit Device">

<img src="{{site.baseurl}}/assets/images/nuveq_change_sync_from.png" alt="Nuveq Change Sync From">

- Sau khi điều chỉnh thời gian bắt đầu đồng bộ, Base Checkin Client sẽ tự động đồng bộ dữ liệu từ ngày được thiết lập đến ngày hiện tại.
- Sau khi quá trình đồng bộ hoàn tất, mỗi `2 phút` sẽ tự động đồng bộ dữ liệu trong ngày.
- Để đồng bộ dữ liệu trong `3 ngày` gần nhất, chọn `Đồng bộ bản ghi`.

<img src="{{site.baseurl}}/assets/images/nuveq_sync_data_last_3_days.png" alt="Nuveq Sync Last 3 Days">

- Khi chọn chức năng `Đồng bộ từ thiết bị` để đồng bộ tất cả máy chấm công, Base Checkin Client sẽ đồng bộ dữ liệu trong ngày đối với máy Nuveq.

<img src="{{site.baseurl}}/assets/images/nuveq_sync_all.png" alt="Nuveq Sync All">
