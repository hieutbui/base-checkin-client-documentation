---
title: Access Directly
parent: Các loại kết nối
nav_order: 1
---

# Access Directly

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).  
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

Base Check-in Client sẽ kết nối trực tiếp đến địa chỉ IP và Port của máy chấm công thông qua các phương thức giải mã:
- Pyatt
- Zkemkeeper
- Large Dataset
- Legacy
- FP_Clock
- FP_Clock_2018

<img src="{{site.baseurl}}/assets/images/sync_method_access_directly.png" alt="Access Directly">

Mỗi log được lưu trong máy chấm công là một dãy số thập lục phân, mỗi máy chấm công có quy định độ dài khác nhau, thường là: 40, 48 hoặc 49. Vì vậy, cần nhập thông số này vào trường `Độ dài mã hoá` trong Base Check-in Client để phần mềm có thể giải mã đúng.

<img src="{{site.baseurl}}/assets/images/encode_length.png" alt="Encoding Length">

Với một số máy cài đặt truy cập thông qua `Web Interface` ([http:///csl/login](http:///csl/login)), Base Check-in Client cũng hỗ trợ phương thức này:

<img src="{{site.baseurl}}/assets/images/web_interface_access_directly.png" alt="Web Interface">

Một số tuỳ chỉnh cho loại kết nối `Access Directly`:
- `Giao thức kết nối`: TCP hoặc UDP - Loại giao thức liên kết
- `Heart beat`: Tần suất tự kiểm tra kết nối giữa Base Check-in Client và máy chấm công xem có còn đang kết nối hay không. <i>Nếu là máy chấm công đời cũ, hoặc máy yếu, nên chọn thời gian lớn hơn </i>
- `Tự kết nối lại`: Tần suất mà Check-in Client tự kết nối lại với máy chấm công nếu bị mất kết nối. <i>Nếu máy chấm công đời cũ hoặc yếu, nên chọn thời gian lớn hơn</i>

## Kiểm tra kết nối máy chấm công
