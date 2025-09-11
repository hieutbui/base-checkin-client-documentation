---
title: Zk Bio Security / Zk Bio Access
parent: Các loại kết nối
nav_order: 2
---

# Zk Bio Security / Zk Bio Access

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

<img src="{{site.baseurl}}/assets/images/zk_bio_security.png" alt="ZK Bio Security / ZK Bio Access"> 

## Mô tả

- ZkBioSecurity/ZkBioAccess là phần mềm được ZKTeco phát triển, không phải máy chấm công.
- Các dòng máy được ZkBioSecurity hỗ trợ: <a href="https://drive.google.com/file/d/1zK2fPgwKG3dCVjV-1yCgNJkWCpFo75qQ/view" target="_blank">ZkBioSecurity Suggestion List</a>
- Dưới đây là mô tả sơ đồ hoạt động:
<img src="{{site.baseurl}}/assets/images/zk_bio_workflow.png" alt="ZK Bio Security Diagram">

## Hướng dẫn cài đặt

- Cài đặt ZkBioSecurity/ZkBioAccess theo link của ZkTeco.
<img src="{{site.baseurl}}/assets/images/install_zkbiosecuirty.png" alt="ZK Bio Security Installation">
- Config máy chủ đám mây trên thiết bị chấm công.
<img src="{{site.baseurl}}/assets/images/setting_mcc_cloud_server.png" alt="Config Device">
- Truy cập ZkBioSecurity, tìm kiếm thiết bị và đồng bộ dữ liệu từ máy chấm công.
<img src="{{site.baseurl}}/assets/images/zkbio_sync_device.png" alt="ZK Bio Security Interface">
- Mở App Base Checkin Client, điền thông tin và bắt đầu đồng bộ dữ liệu.
<img src="{{site.baseurl}}/assets/images/zkbio_setup_checkin_client.png" alt="ZK Bio Security Check-in Client">

## Hướng dẫn sử dụng

- Ở lần đầu tiên khi connect hệ thống, cần nhấn tạm dừng đồng bộ để chuyển sang chế độ đồng bộ bằng tay. Phần mềm sẽ sync toàn bộ dữ liệu trong vòng 6 tháng trở về trước.
- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).
<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">
