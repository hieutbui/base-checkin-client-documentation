---
title: Dahahi
parent: Các loại kết nối
nav_order: 11
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Dahahi

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

- Các máy chấm công Dahahi sẽ sử dụng phần mềm quản lý riêng dưới dạng web-based.
- Base Checkin Client có khả năng kết nối đến phần mềm này và đọc dữ liệu chấm công thông qua SubDomain API do Dahahi cung cấp. Các dữ liệu chấm công sẽ được phân biệt dựa trên `EmployeeCode`.

## Hướng dẫn cài đặt

- Liên hệ nhà cung cấp máy chấm công Dahahi để nhận địa chỉ SubDomain chính xác.
- Truy cập vào SubDomain được cập để lấy các thông tin: `AppKey` và `SecretKey`.

<img src="{{site.baseurl}}/assets/images/dahahi_admin_page.png" alt="Dahahi Admin Page">

- Chọn phiên bản Dahahi và điền đầy đủ các thông tin bắt buộc.

<img src="{{site.baseurl}}/assets/images/select_dahahi.png" alt="Select Dahahi">

<img src="{{site.baseurl}}/assets/images/dahahi.png" alt="Dahahi Connection">

## Một số lưu ý khi sử dụng

- Sau khi kết nối lần đầu tiên, ứng dụng sẽ tự động đồng bộ dữ liệu trong `3 ngày` gần nhất. Để thay đổi ngày bắt đầu đồng bộ, chọn `Chỉnh sửa thiết bị` và `lựa chọn thời gian đồng bộ`. Thời gian đồng bộ ***KHÔNG*** vượt quá `3 tháng` trước so với hiện tại.

<img src="{{site.baseurl}}/assets/images/dahahi_select_edit_device.png" alt="Dahahi Edit Device">

<img src="{{site.baseurl}}/assets/images/dahahi_change_sync_from.png" alt="Dahahi Change Sync From">

- Sau khi điều chỉnh thời gian bắt đầu đồng bộ, Base Checkin Client sẽ tự động đồng bộ dữ liệu từ ngày được thiết lập đến ngày hiện tại.
- Sau khi quá trình đồng bộ hoàn tất, mỗi `2 phút` sẽ tự động đồng bộ dữ liệu trong ngày.
- Để đồng bộ dữ liệu trong `3 ngày` gần nhất, chọn `Đồng bộ bản ghi`.

<img src="{{site.baseurl}}/assets/images/dahahi_sync_data_last_3_days.png" alt="Dahahi Sync Last 3 Days">

- Khi chọn chức năng `Đồng bộ từ thiết bị` để đồng bộ tất cả máy chấm công, Base Checkin Client sẽ đồng bộ dữ liệu trong ngày đối với máy Dahahi.

<img src="{{site.baseurl}}/assets/images/dahahi_sync_all.png" alt="Dahahi Sync All">
