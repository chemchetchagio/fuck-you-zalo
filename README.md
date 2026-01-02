# fuck-you-zalo
# **🛡️ Zalo  Blocker**

Lấy lại quyền riêng tư và ủng hộ sử dụng các ứng dụng OTT khác tốt hơn nghìn lần zalo.
Dự án này cung cấp danh sách các tên miền (domains) và địa chỉ IP được sử dụng bởi Zalo (VNG) cho mục đích quảng cáo, theo dõi người dùng (tracking), và thu thập dữ liệu nền (telemetry), nhắn tin, máy chủ

# ⚖️ Tuyên bố từ chối trách nhiệm (Disclaimer)

Dự án này không liên kết với VNG Corp hay Zalo Group.

Mục đích duy nhất là tôi ghét zalo vãi cả l.
 

# **📖 Giới thiệu**

Zalo là ứng dụng nhắn tin phổ biến nhất tại Việt Nam. Tuy nhiên, khác như nhiều ứng dụng "miễn phí" khác, nó rất tệ cực kì tệ, những tính năng cơ bản còn không xong, mà trả phí cũng không ổn tí nào, mỗi lần đổi máy lại thì lại phải sao lưu lại (tôi biết signal với whatapp cũng cần phải sao lưu thủ công) nhưng mà em ơi em ơi ZALO gửi 8500/6020 (5000vnd/sms) không thì 1900633200, mới đây thêm quả [chính sách](https://vnexpress.net/zalo-nhan-tin-zalo-cap-nhat-dieu-khoan-moi-4999790.html) cũng như cứt nốt

Bộ lọc này được tạo ra nhằm mục đích:
 1. Chặn sạch, chặn cứng zalo, chặn không thiếu cái gì cả
 2. Giúp người dùng chuyển sang nền tảng khác

# **🛠️ Hướng dẫn cài đặt**

## 1. AdGuard Home / AdGuard App

Dành cho người dùng quản lý mạng gia đình hoặc cài app trên điện thoại.

Mở trang quản trị AdGuard Home hoặc App AdGuard.

Vào mục Filters (Bộ lọc) -> DNS Blocklists.

Chọn Add Blocklist -> Add a custom list.

Dán URL của danh sách bạn chọn ở trên vào.

Đặt tên (ví dụ: Zalo Blocker) và nhấn Save.

## 2. Pi-hole

Dành cho người dùng Raspberry Pi hoặc Docker.

Truy cập trang quản trị Pi-hole.

Vào mục Group Management -> Adlists.

Dán URL vào ô Address.

Nhấn Add.

Mở Terminal và chạy lệnh cập nhật: pihole -g.

## 3. uBlock Origin (Trình duyệt)

Dành cho Zalo Web (chat.zalo.me).

Mở Dashboard của uBlock Origin.

Tab Filter lists -> Kéo xuống dưới cùng chọn Import.

Dán URL danh sách vào và nhấn Apply changes.

## 4. File Hosts (Windows/Mac/Linux)

Dành cho người dùng muốn chặn thủ công trên máy tính.

Tải file hosts-basic.txt về máy.

Mở file hosts trên máy tính của bạn:

Windows: C:\Windows\System32\drivers\etc\hosts

Mac/Linux: /etc/hosts

Copy nội dung và dán vào cuối file hosts.

Lưu lại (cần quyền Admin/Sudo).

# 🤝 Đóng góp (Contributing)

Dự án này cần sự chung tay của cộng đồng để liên tục cập nhật các tên miền mới của Zalo. Nếu bạn phát hiện quảng cáo vẫn hiện hoặc tính năng nhắn tin bị lỗi:

Tạo một Issue/Pull mới thông báo vấn đề về việc chặn thiếu/bổ sung.
