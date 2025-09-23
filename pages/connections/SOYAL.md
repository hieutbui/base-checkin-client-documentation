---
title: Soyal
parent: Các loại kết nối
nav_order: 13
---

<details open markdown="block">
  <summary>
    Mục lục
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

# Soyal

> ⚠️ **Lưu ý:** Trên thị trường hiện nay có rất nhiều loại máy chấm công của các hãng khác nhau, Check-in Client hiện chưa thể tích hợp được tất cả các máy chấm công.  
> 
> Để lựa chọn phương thức giải mã phù hợp, tham khảo thông tin danh sách các thiết bị đã kết nối thành công với Base Check-in Client - [Danh sách thiết bị đã kết nối](../TESTED_DEVICES).
> 
> Với các thiết bị không có trong danh sách, cần thử qua các loại phương thức và độ dài mã hoá để biết được thiết lập chính xác.

## Mô tả

- Máy chấm công Soyal sẽ đẩy dữ liệu về địa chỉ server với mỗi sự kiện chấm công: quẹt thẻ, vân tay, etc.

- Base Check-in Client sẽ trỏ đến địa chỉ server này để lắng nghe sự kiện chấm công.

- Do cơ chế lưu log chấm công của Soyal hoạt động như 1 hàng chờ → nếu muốn lấy 1 long chấm công thì phải đưa log chấm công này ra khỏi máy chấm công → Base Check-in Client hiện nay chỉ hỗ trợ ***lắng nghe log chấm công Real-time***, KHÔNG hỗ trợ đồng bộ hết log chấm công trong máy nhằm tránh mất mát dữ liệu.

## Hướng dẫn cài đặt

- Truy cập vào trang Soyal Access Controller của máy bằng địa chỉ IP máy chấm công.
- Tài khoản mặc định: ***SuperAdm/721568***.
- Truy cập vào trang cài đặt mạng và thiết lập địa chỉ lắng nghe dữ liệu. Có thể là bất kỳ địa chỉ IP nào nhưng cần đảm bảo 2 yếu tố: Địa chỉ này là một thiết bị hoạt động trong mạng và máy cài Base Check-in Client có thể liên lạc được đến địa chỉ này (Ví dụ: `ping ip`)

<img src="{{site.baseurl}}/assets/images/soyal_listening_server_address.png" alt="Soyal Server IP Setting">

- Chọn loại kết nối Soyal và điền các thông tin

<img src="{{site.baseurl}}/assets/images/soyal_filled_data.png" alt="Soyal Connection">