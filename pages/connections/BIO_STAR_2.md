---
title: Bio Star 2
parent: Các loại kết nối
nav_order: 3
---

# Bio Star 2

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).  
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

<img src="{{site.baseurl}}/assets/images/setting_bio_star_2.png" alt="Bio Star 2">

<img src="{{site.baseurl}}/assets/images/fill_setting_bio_star.png" alt="Bio Star 2 Filled data">

## Mô tả

- Chỉ được thêm một hệ thống (Một hệ thống sẽ bao gồm tất cả thiết bị chấm công thuộc hệ thống đó)
- Ở lần đầu tiên khi connect đến 1 thiết bị, phần mềm sẽ đồng bộ toàn bộ dữ liệu trong vòng 30 ngày gần nhất. Sau lần đồng bộ đầu tiên, phần mềm sẽ tự đồng bộ mỗi phút 1 lần. Các log được đồng bộ sẽ trong khoảng: Thời gian của log cuối cùng từ lần đồng bộ trước → thời điểm thực hiện đồng bộ.
- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).
<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">