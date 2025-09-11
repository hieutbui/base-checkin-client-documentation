---
title: Các chức năng chính
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

# Các chức năng chính

## Thanh chức năng phía trên

<img src="{{site.baseurl}}/assets/images/functions_at_top.png" alt="Thanh chức năng phía trên" class="doc-image">

Dưới đây là mô tả chi tiết về các chức năng:

- **Import**: Thêm thiết bị từ file .xls.
- **Export**: Xuất danh sách thiết bị ra file .xls.
- **Lịch sử**: Xem lịch sử hoạt động của ứng dụng.

<i>File .xls mẫu</i>: 
<a href="{{site.baseurl}}/assets/sample/import_devices_sample.xls" download>Mẫu file import</a>

## Thanh chức năng phía dưới

<img src="{{site.baseurl}}/assets/images/functions_at_bottom.png" alt="Thanh chức năng phía dưới" class="doc-image">

Dưới đây là mô tả chi tiết về các chức năng:

- **Lọc dữ liệu (Filter)**: Phần lọc dữ liệu cho phép lọc dữ liệu chấm công theo mã chấm công hoặc theo khoảng thời gian (tối đa 3 tháng).
- **Đồng bộ từ thiết bị**: Đồng bộ dữ liệu chấm công từ thiết bị về ứng dụng. Các thiết bị sẽ được đồng bộ lần lượt từ trái sang phải.
- **Thiết lập**: Mở trang thiết lập ứng dụng cho phép tuỳ chỉnh chu kỳ từ động đồng bộ (đồng bộ 1 lần mỗi X phút), chu kỳ tự động đẩy dữ liệu lên HRM (đẩy dữ liệu 1 lần mỗi X phút), tuỳ chọn tự động đẩy dữ liệu ngay sau khi đồng bộ thành công, tuỳ chỉnh thời gian cụ thể tránh/chỉ định đồng bộ và dọn dẹp dữ liệu đã lưu.

<img src="{{site.baseurl}}/assets/images/setting.png" alt="Trang thiết lập" class="doc-image">

- **Xem trạng thái**: Xem tổng số log chấm công đã đồn bộ/đẩy trong một khoảng thời gian.

<img src="{{site.baseurl}}/assets/images/push_pull_history.png" alt="Trang trạng thái" class="doc-image">

- **Đồng bộ lên HRM**: Đẩy dữ liệu chấm công đã đồng bộ từ thiết bị lên hệ thống HRM.

<img src="{{site.baseurl}}/assets/images/push_to_hrm.png" alt="Đồng bộ lên HRM" class="doc-image">

## Chức năng thêm thiết bị

<img src="{{site.baseurl}}/assets/images/add_device_button.png" alt="Nút thêm thiết bị" class="doc-image">

<img src="{{site.baseurl}}/assets/images/add_device_modal.png" alt="Form thêm thiết bị" class="doc-image">

Khi nhấn vào nút `Thêm thiết bị`, một cửa sổ sẽ hiện ra để nhập thông tin thiết bị mới. Các trường thông tin sẽ tuỳ thuộc vào loại kết nối được lựa chọn - tham khảo phần [Các loại kết nối](/pages/connections/CONNECTIONS_OVERVIEW) -  

Phần thông tin `HRM clients`, cần nhập mã client và mật khẩu của mã trong phần cài đặt văn phòng trên hệ thống HRM. Nếu có nhiều văn phòng nhưng dùng chung 1 nguồn chấm công → Thêm nhiều HRM clients.

<img src="{{site.baseurl}}/assets/images/get_hrm_client.png" alt="Phần HRM clients trên hệ thống HRM" class="doc-image">

## Chức năng chỉnh sửa thiết bị

<img src="{{site.baseurl}}/assets/images/device_setting.png" alt="Nút chỉnh sửa thiết bị">

Phần chỉnh sửa thiết bị sẽ thay đổi ứng với từng loại kết nối.

### Access Directly

<img src="{{site.baseurl}}/assets/images/setting_device_access_directly.png" alt="Chỉnh sửa thiết bị Access Directly" class="doc-image">

### Zk Bio Security / Zk Bio Access

<img src="{{site.baseurl}}/assets/images/setting_device_zkbiosecurity.png" alt="Chỉnh sửa thiết bị Zk Bio Security / Zk Bio Access" class="doc-image">

### BioStar 2

<img src="{{site.baseurl}}/assets/images/setting_device_biostar2.png" alt="Chỉnh sửa thiết bị BioStar 2" class="doc-image">

### HIK Vision

<img src="{{site.baseurl}}/assets/images/setting_device_hikvision.png" alt="Chỉnh sửa thiết bị HIK Vision" class="doc-image">

### Hanet AI

<img src="{{site.baseurl}}/assets/images/setting_device_hanet_ai.png" alt="Chỉnh sửa thiết bị Hanet AI" class="doc-image">

### Idemia

<img src="{{site.baseurl}}/assets/images/setting_device_idemia.png" alt="Chỉnh sửa thiết bị Idemia" class="doc-image">

### Sunbeam

<img src="{{site.baseurl}}/assets/images/setting_device_sunbeam.png" alt="Chỉnh sửa thiết bị Sunbeam" class="doc-image">

### SQL Server

<img src="{{site.baseurl}}/assets/images/setting_device_sql_server.png" alt="Chỉnh sửa thiết bị SQL Server" class="doc-image">

### ZK 5xxx

<img src="{{site.baseurl}}/assets/images/setting_device_zk_5xxx.png" alt="Chỉnh sửa thiết bị ZK 5xxx" class="doc-image">

### Nuveq

<img src="{{site.baseurl}}/assets/images/setting_device_nuveq.png" alt="Chỉnh sửa thiết bị Nuveq" class="doc-image">

### Dahahi

<img src="{{site.baseurl}}/assets/images/setting_device_dahahi.png" alt="Chỉnh sửa thiết bị Dahahi" class="doc-image">

### My Time Cloud

<img src="{{site.baseurl}}/assets/images/setting_device_mytime_cloud.png" alt="Chỉnh sửa thiết bị My Time Cloud" class="doc-image">

### Soyal

<img src="{{site.baseurl}}/assets/images/setting_device_soyal.png" alt="Chỉnh sửa thiết bị Soyal" class="doc-image">

### Dahua

<img src="{{site.baseurl}}/assets/images/setting_device_dahua.png" alt="Chỉnh sửa thiết bị Dahua" class="doc-image">

### ZK BioTime 8 & 9

<img src="{{site.baseurl}}/assets/images/setting_device_zkbiotime.png" alt="Chỉnh sửa thiết bị ZK BioTime 8 & 9" class="doc-image">
