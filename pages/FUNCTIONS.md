---
nav_order: 3
---

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

Phần thông tin `HRM clients`, cần nhập mã client và mật khẩu của mã trong phần cài đặt văn phòng trên hệ thống HRM.

<img src="{{site.baseurl}}/assets/images/get_hrm_client.png" alt="Phần HRM clients trên hệ thống HRM" class="doc-image">
