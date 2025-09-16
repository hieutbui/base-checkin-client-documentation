---
title: Hanet AI
parent: Các loại kết nối
nav_order: 5
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Hanet AI

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả
- Camera chấm công HANET AI được tích hợp công nghệ chấm công bằng trí tuệ nhân tạo (AI) nhận diện khuôn mặt nhanh chóng khác với các máy chấm công truyền thống bằng vân tay.
- Để quản lý máy chấm công, người dùng cần sử dụng hệ thống đi kèm để lưu trữ và quản lý dữ liệu của các thiết bị trong cùng một địa điểm. 
- Base Check-in Client có khả năng kết nối và đọc dữ liệu thông qua hệ thống quản lý của HANET theo  địa điểm đã cài đặt, không kết nối trực tiếp đến camera chấm công HANET AI.

## Hướng dẫn cài đặt

### Lấy các thông số cần thiết để kết nối thiết bị 

#### Lấy mã access token 

- Truy cập đường link <a href="https://developers.hanet.ai" target="_blank">https://developers.hanet.ai</a>  -> Đăng nhập bằng tài khoản quản trị (tài khoản quản trị là là tài khoản đã thêm địa điểm, và máy chấm công, thông tin nhân sự) - phần thông tin này khách hàng sẽ được hướng dẫn tạo khi mua sản phẩm từ nhà sản xuất.

<img src="{{site.baseurl}}/assets/images/developer_hanet_ai_login.png" alt="Hanet AI Login developer">

- Truy cập mục App Console

<img src="{{site.baseurl}}/assets/images/hanet_ai_access_app_console.png" alt="Hanet AI App Console">

- Chọn Tạo ứng dụng

<img src="{{site.baseurl}}/assets/images/hanet_ai_create_application.png" alt="Hanet AI Create App">

- Nhập tên ứng dụng: (VD: Base.vn) -> Nhập Mô tả -> Nhấn Thêm

<img src="{{site.baseurl}}/assets/images/hanet_ai_fill_info_create_application.png" alt="Hanet AI Create App Form">

- Sau khi thêm ứng dụng, nhấn vào biểu tượng ứng dụng tại màn hình App console để xem thông tin ứng dụng

<img src="{{site.baseurl}}/assets/images/hanet_ai_view_application.png" alt="Hanet AI View App">

- Chọn Hiển thị thông tin Access Token

<img src="{{site.baseurl}}/assets/images/hanet_ai_show_token.jpg" alt="Hanet AI Show Access Token">

- Copy và lưu lại Access token (1)

<img src="{{site.baseurl}}/assets/images/hanet_ai_copy_token.jpg" alt="Hanet AI Copy Access Token">

#### Thông tin thiết bị, địa điểm

- Truy cập vào Hanet Connect: <a href="https://connect.hanet.ai" target="_blank">https://connect.hanet.ai</a> (website quản lý dữ liệu của Hanet)
- Đăng nhập bằng tài khoản quản trị giống ở phần trên
- Truy cập địa điểm đã cài đặt camera chấm công (địa điểm đã được người dùng tạo để thêm máy chấm công và thông tin nhân sự, một địa điểm có thể có nhiều máy chấm công)

<img src="{{site.baseurl}}/assets/images/hanet_ai_select_place.png" alt="Hanet AI Select Place">

- Copy PlaceID (2) của địa điểm lấy thông tin trên đường link như hình

<img src="{{site.baseurl}}/assets/images/hanet_ai_copy_place_id.png" alt="Hanet AI Place ID">

### Kết nối với Base Checkin Client

- Tại cửa sổ thêm thiết bị, chọn phiên bản “Hanet AI”

<img src="{{site.baseurl}}/assets/images/hanet_ai_checkin_client.png" alt="Hanet AI Select Version">

- Nhập các thông tin của địa điểm cần thêm

<img src="{{site.baseurl}}/assets/images/hanet_ai_checkin_client_fill_info.png" alt="Hanet AI Fill Info">

- Bấm xác nhận để thêm địa điểm.

<img src="{{site.baseurl}}/assets/images/hanet_ai_connected.png" alt="Hanet AI Added Device">

- Khi kết nối lần đầu, hệ thống sẽ bắt đầu đồng bộ dữ liệu từ ngày bắt đầu của tháng hiện tại.
- Sau lần đồng bộ đầu tiên, mỗi 2 phút ứng dụng sẽ tự đồng bộ 1 lần với dữ liệu chấm công trong 3 ngày gần nhất.
- Để đồng bộ các log trong khoảng thời gian khác hãy chọn lại `Thời gian đồng bộ từ` trong phần [Chỉnh sửa thiết bị](../FUNCTIONS#chức-năng-chỉnh-sửa-thiết-bị).

<img src="{{site.baseurl}}/assets/images/sync_from.png" alt="ZK Bio Security Sync Time">