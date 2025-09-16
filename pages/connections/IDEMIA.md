---
title: Idemia
parent: Các loại kết nối
nav_order: 6
---

# Idemia

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả
- Không kết nối trực tiếp đến máy chấm công mà kết nối đến địa chỉ quản lý do Idemia cung cấp.
- Base Check-in Client sẽ kết nối đến địa chỉ do API của Idemia cung cấp.  Ví dụ: `http://10.137.53.232:1100/api/LogDevice/getlogbytime`  → IP: `10.137.53.232`, Port: `1110`.

<img src="{{site.baseurl}}/assets/images/idemia.png" alt="Idemia">