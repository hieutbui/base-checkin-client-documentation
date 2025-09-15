---
title: Access Directly
parent: Các loại kết nối
nav_order: 1
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Access Directly

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).  
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

<img src="{{site.baseurl}}/assets/images/access_directly.png" alt="Access Directly">

## Mô tả

<img src="{{site.baseurl}}/assets/images/access_directly_flow.png" alt="Access Directly Flow">

Base Check-in Client sẽ kết nối trực tiếp đến địa chỉ IP và Port của máy chấm công để gửi lệnh lấy dữ liệu thông qua các `Phương thức giải mã`:
- Pyatt
- Zkemkeeper
- Large Dataset
- Legacy
- FP_Clock
- FP_Clock_2018

Các phương thức giải mã Pyatt, Large Dataset và Legacy có logic xử lý tương tự nhau. Riêng phương thức Pyatt cho phép nhập mật khẩu của thiết bị.

Phương thức FP_CLOCK & FP_CLOCK_2018 sử dụng cho các máy chấm công có port kết nối mặc định là `5005`, thường do Mitaco phát hành. Với phương thức này, cần nhập các thông tin sau: IP, port, machine number và mật khẩu - Các thông tin này có trong phần mềm MitaPro được Mitaco cung cấp

Tham khảo tài liệu đặc tả về các phương thức giải mã tại:

- <a href="https://github.com/adrobinoga/zk-protocol/tree/master/sections" target="_blank">Pyatt, Large Dataset, Legacy</a>
- <a href="{{site.baseurl}}/assets/documents/zkemkeeper.pdf" target="_blank">Zkemkeeper</a>
- <a href="{{site.baseurl}}/assets/documents/fp_clock.doc" target="_blank">FP_Clock & FP_Clock_2018</a>

<img src="{{site.baseurl}}/assets/images/sync_method_access_directly.png" alt="Access Directly">

Mỗi log được lưu trong máy chấm công là một dãy số thập lục phân, mỗi máy chấm công có quy định của dãy số này khác nhau, thường là: 40, 48 hoặc 49. Base Check-in Client sẽ sử dụng độ dài này để giải mã log chấm công nhận được từ máy chấm công.

<img src="{{site.baseurl}}/assets/images/encode_length.png" alt="Encoding Length">

Một số tuỳ chỉnh cho loại kết nối `Access Directly`:
- `Giao thức kết nối`: TCP hoặc UDP - Loại giao thức sử dụng để gửi lệnh lấy dữ liệu đến máy chấm công. Thường sử dụng TCP
- `Heart beat`: Tần suất tự kiểm tra kết nối giữa Base Check-in Client và máy chấm công xem có còn đang kết nối hay không. <i>Nếu là máy chấm công đời cũ, hoặc máy yếu, nên chọn thời gian lớn hơn </i>
- `Tự kết nối lại`: Tần suất mà Check-in Client tự kết nối lại với máy chấm công nếu bị mất kết nối. <i>Nếu máy chấm công đời cũ hoặc yếu, nên chọn thời gian lớn hơn</i>

## Kiểm tra kết nối máy chấm công

- Nếu đang sử dụng phần mềm quản lý máy chấm công được nhà phân phối cung cấp, đảm bảo phần mềm có thể kết nối và đồng bộ được dữ liệu chấm công.
- Mở **Window PowerShell/Terminal/Command Prompt** bằng quyền **Admin (Run as administrator)**.
- Bật tính năng telnet của Window: `dism /online /Enable-Feature /FeatureName:TelnetClient`.
- Kiểm tra kết nối giữa máy tính cài Base Check-in Client và máy chấm công: **ping ip_máy_chấm_công**.
- Kiểm có thể truy cập vào port của máy chấm công từ bên ngoài không: **telnet ip_máy_chấm công port_máy_chấm_công**.

<figure>
  <img src="{{site.baseurl}}/assets/images/ping_success.png" alt="Ping Success">
  <figcaption>Ví dụ kết quả ping thành công</figcaption>
</figure>

<br/>

<figure>
  <img src="{{site.baseurl}}/assets/images/ping_failure.png" alt="Ping Failure">
  <figcaption>Ví dụ kết quả ping không thành công</figcaption>
</figure>

<br/>

<figure>
  <img src="{{site.baseurl}}/assets/images/telnet_not_recognized.png" alt="Telnet Not Recognized">
  <figcaption>Ví dụ telnet chưa được bật</figcaption>
</figure>

<br/>

<figure>
  <img src="{{site.baseurl}}/assets/images/telnet_failed.png" alt="Telnet Failed">
  <figcaption>Ví dụ telnet không thành công</figcaption>
</figure>

<br/>

<figure>
  <img src="{{site.baseurl}}/assets/images/telnet_success.png" alt="Telnet Success">
  <figcaption>Ví dụ telnet thành công</figcaption>
</figure>

## Web Interface

Với một số máy cài đặt truy cập thông qua `Web Interface` ([http:///csl/login](http:///csl/login)), Base Check-in Client cũng hỗ trợ phương thức này:

<img src="{{site.baseurl}}/assets/images/web_interface_access_directly.png" alt="Web Interface">

Để sử dụng Web Interface, người dùng cần tạo User ở máy chấm công với quyền SuperAdmin:
- B1: Chọn “Người sử dụng” ở giao diện Menu máy chấm công

<img src="{{site.baseurl}}/assets/images/web_interface_select_user_1.png" alt="Select User 1">

<img src="{{site.baseurl}}/assets/images/web_interface_select_user_2.png" alt="Select User 2">

- B2: Chọn “Vai trò người sử dụng” và cài thành “Quản trị cấp cao”

<img src="{{site.baseurl}}/assets/images/web_interface_select_user_role_1.png" alt="Select SuperAdmin 1">

<img src="{{site.baseurl}}/assets/images/web_interface_select_user_role_2.png" alt="Select SuperAdmin 2">

- B3: Cài mật mã cho tài khoản

<img src="{{site.baseurl}}/assets/images/web_interface_setup_password.png" alt="Set Password">

- Sau khi hoàn thành các bước trên và lưu thông tin, truy cập trình duyệt bằng IP của máy chấm công (Ví dụ : 10.20.0.18)

<img src="{{site.baseurl}}/assets/images/web_interface_access_machine.png" alt="Web Interface access to machine">

- Nhập thông tin đăng nhập ( Login ID : Mã chấm công , Password : Mật mã tạo ở bước 3), nếu thành công, giao diện giống như hình dưới đây :

<img src="{{site.baseurl}}/assets/images/web_interface_login.png" alt="Web Interface login">
