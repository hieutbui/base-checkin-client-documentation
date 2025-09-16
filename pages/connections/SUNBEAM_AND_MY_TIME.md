---
title: Sunbeam/MyTime Cloud
parent: Các loại kết nối
nav_order: 7
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Sunbeam/MyTime Cloud

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

- Phần mềm SunBeam bản chất là phần mềm MyTime nhưng được tuỳ chỉnh lại.
- Phần mềm Base Check-in Client sẽ lấy dữ liệu MCC thông qua phần mềm SunBeam/MyTime chứ không kết nối trực tiếp tới MCC.

## Các dữ liệu cần thiết để kết nối
- Máy tính đã cài đặt phần mềm SunBeam/MyTime và đảm bảo phần mềm Sunbeam/MyTime có thể kết nối và lấy dữ liệu chấm công từ máy chấm công.
- Các thông tin để kết nối bao gồm: Địa chỉ server (phần mềm SunBeam/MyTime), port kết nối , username và pasword để đăng nhập. 
- Tài khoản mặc định là: Username: `admin`; Password: `123` 

<img src="{{site.baseurl}}/assets/images/ip_port_sunbeam_mytime.png" alt="IP và Port Sunbeam/MyTime">

<img src="{{site.baseurl}}/assets/images/sunbeam.png" alt="Cài đặt Sunbeam">

<img src="{{site.baseurl}}/assets/images/mytime.png" alt="Cài đặt MyTime">

## Lỗi thường gặp khi sử dụng

Lỗi thường xảy ra nhất khi sử dụng phần mềm SunBeam và MyTime là lỗi HPA → Xảy ra khi địa chỉ IP, kết nối Internet, Router, etc. của máy tính cài phần mềm này thay đổi nhiều lần → Phần mềm không thể khởi tạo server cloud.

<img src="{{site.baseurl}}/assets/images/hpa_error.png" alt="Lỗi HPA">

### Cách khắc phục lỗi HPA
- B1. Vào Cài đặt chấm công.
- B2. Tham số tải công.
  
<img src="{{site.baseurl}}/assets/images/fix_hpa_error_1.png" alt="Fix HPA Error 1">

- B3. Sửa Port nếu cần đổi Port khác hoặc sửa tham số Địa chỉ máy chủ đám mây về giá trị là 1 
(nếu bị đổi IP phần mềm báo HPA ) sau đó lưu lại và tắt phần mềm đi mở lại.

<img src="{{site.baseurl}}/assets/images/fix_hpa_error_2.png" alt="Fix HPA Error 2">

- ***Lưu ý***: Với bản cài là MyTime Server cần thực hiện thêm 1 bước là Restart Mytime HRS - Vào Task Manager -> Services -> Kích chuột phải vào MyTime HRS và chọn Restart. -> Sau đó mở lại phần mềm 

<img src="{{site.baseurl}}/assets/images/restart_mytime_hrs.png" alt="Restart MyTime HRS">
