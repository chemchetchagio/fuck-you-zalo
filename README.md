# fuck-you-zalo
# **🛡️ Zalo  Blocker**
#**HIỆN TẠI CHUNG TÔI CẦN HỖ TRỢ XÂY DỰNG README TRONG VIỆC CÁCH SETUP BLOCKLIST!?!?!?!**

Lấy lại quyền riêng tư và ủng hộ sử dụng các ứng dụng OTT khác tốt hơn nghìn lần zalo.

Dự án này cung cấp danh sách các tên miền (domains) và địa chỉ IP được sử dụng bởi Zalo (VNG) cho mục đích quảng cáo, theo dõi người dùng (tracking), và thu thập dữ liệu nền (telemetry), nhắn tin, máy chủ

# ⚖️ Tuyên bố từ chối trách nhiệm
**Dự án này không liên kết với VNG Corp hay Zalo Group.**

Mục đích duy nhất là tôi ghét zalo vãi cả l.
 

# **📖 Giới thiệu**

Zalo là ứng dụng nhắn tin phổ biến nhất tại Việt Nam. Tuy nhiên, khác như nhiều ứng dụng "miễn phí" khác, nó rất tệ cực kì tệ, những tính năng cơ bản còn không xong, mà trả phí cũng không ổn tí nào zcloud thì chập chờn, mỗi lần đổi máy lại thì lại phải sao lưu lại (tôi biết signal với whatapp cũng cần phải sao lưu thủ công) nhưng mà em ơi em ơi ZALO gửi 8500/6020 (5000vnd/sms) không thì 1900633200. Dùng bản web thì không cho đồng bộ tin nhắn, tải app thì tốn hết cả chip nhớ xong làm trên quả electron thì tốn hết cả tài nguyên. Zbusiness thì toàn tín năng mà whatapp ăn sạch mới đây thêm quả [chính sách](https://vnexpress.net/zalo-nhan-tin-zalo-cap-nhat-dieu-khoan-moi-4999790.html) cũng như cứt nốt

Bây giờ lại thêm quả xác minh cccd như gọi 4 nữa

Sau tất cả Zalo chỉ ăn được cái Mini App 

Bộ lọc này được tạo ra nhằm mục đích:
 1. Chặn sạch, chặn cứng zalo, chặn không thiếu cái gì cả
 2. Giúp người dùng chuyển sang nền tảng khác

# **🛠️ Hướng dẫn cài đặt**

## 1. AdGuard Home / AdGuard App 

Mở trang quản trị AdGuard Home hoặc App AdGuard.

Vào mục Filters (Bộ lọc) -> DNS Blocklists.

Chọn Add Blocklist -> Add a custom list.

Dán [URL Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/adblocker.txt) hoặc [URL forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/adblocker.txt) sau

Đặt tên (ví dụ: zalo-fucker) và nhấn Save.

## 2. Pi-hole / OpenSnitch

1. Truy cập trang quản trị Pi-hole.

2. Vào mục Group Management -> Adlists.

3. Dán [URL Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/host.txt) hoặc [URL forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/host.txt) vào ô Address.

Nhấn Add.

Mở Terminal và chạy lệnh cập nhật: ```pihole -g```.

## 3. uBlock Origin / Adguard Adblocker (Trình duyệt)

Mở Dashboard của uBlock Origin.

Tab Filter lists -> Kéo xuống dưới cùng chọn Import.

Dán [URL Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/adblocker.txt) hoặc [URL forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/adblocker.txt)  danh sách vào và nhấn Apply changes.

## 4. File Hosts (Windows)

Tải file [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/windows.txt) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/windows.txt)  về máy.

Mở file hosts trên máy tính của bạn:

 ```C:\Windows\System32\drivers\etc\hosts```

### 4.1. File Host (Macos/Linux)
Truy cập vào (sử dụng nano,vim để chỉnh sửa)
 
 ```/etc/hosts```

Copy nội dung trong [file sau](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/adaway.txt) và dán vào cuối file hosts.

Lưu lại (có thể cần quyền Admin/Sudo).

**HIỆN TẠI ĐÃ RA MẮT CÔNG CỤ GIÚP BẠN CHẶN DỄ DÀNG HƠN, XEM QUA TẠI [ĐÂY](https://github.com/zalofucker/Tool-block-zalo) HOẶC [ĐÂY](https://codefloe.com/zalofucker/Tool-block-zalo)**


## 5.Unbound
Bước 1: Tạo file chứa danh sách chặn
Đầu tiên, hãy tạo một file mới để chứa danh sách các tên miền bạn muốn chặn.

Mở Terminal.

Tạo và mở file (ví dụ đặt tên là zaloblocklist.conf) (có thể dùng nano, vim,...):

```sudo nano /etc/unbound/zaloblocklist.conf```

Bước 2: Dán nội dung vào file
Copy toàn bộ danh sách ở file [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/unbound.txt) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/unbound.txt) sau đó lưu lại file

Bước 3: Cấu hình Unbound để nhận file này
Mở file cấu hình chính (thường nằm ở /etc/unbound/unbound.conf):

```sudo nano /etc/unbound/unbound.conf```

Tìm đến phần server: (nếu không thấy, bạn có thể viết thêm vào). Thêm dòng include: trỏ đến file bạn vừa tạo. Nó sẽ trông giống như sau:


```
server:
    # ... các cấu hình khác ...
    # Thêm dòng này vào:
    include: "/etc/unbound/blocklist.conf" 
```
**Lưu ý: Nếu bạn đang dùng Ubuntu/Debian based, thư mục /etc/unbound/unbound.conf.d/ thường được tự động load. Nếu vậy, bạn chỉ cần lưu file ở Bước 1 vào thư mục đó (ví dụ: /etc/unbound/unbound.conf.d/blocklist.conf) là xong, không cần làm Bước 3.**

Bước 4: Kiểm tra lỗi cú pháp
Trước khi khởi động lại, hãy kiểm tra xem file cấu hình có bị lỗi không để tránh làm sập DNS server.

```unbound-checkconf```

Nếu kết quả trả về `no errors in /etc/unbound/unbound.conf`, bạn đã làm đúng.

Nếu có lỗi, nó sẽ chỉ ra dòng bị sai để bạn sửa.

Bước 5: Khởi động lại Unbound
Áp dụng thay đổi bằng cách khởi động lại dịch vụ:

```sudo systemctl restart unbound```
### Dành cho người dùng OPNsense / pfSense
Nếu bạn đang dùng router OPNsense hoặc pfSense chạy Unbound:

1. Truy cập vào trang quản trị (Web UI).

2. Tìm đến mục Services -> Unbound DNS -> Overrides (hoặc Advanced / Custom Options tùy phiên bản).

3. Tìm ô Custom Options (Tùy chọn tùy chỉnh).

4. Dán trực tiếp danh sách [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/unbound.txt) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/unbound.txt) vào đó

5. Nhấn Save và Apply Changes.

## 6.Knot / Bind9 / PowerDNS
### 6.1 Bind9

Bước 1: Tạo file Zone RPZ Tạo file `/etc/bind/db.rpz` sau đó dán danh sách vào:
```
$TTL 60
@            IN    SOA  localhost. root.localhost.  (
                          2   ; Serial
                          3H  ; Refresh
                          1H  ; Retry
                          1W  ; Expire
                          1H ) ; Minimum TTL
@            IN    NS    localhost.

```
Bước 2: dán danh sách domain [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/powerdns.rpz) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/powerdns.rpz) vào trong file 

Bước 3: Khai báo trong `named.conf.options`
Mở file cấu hình chính (thường là `/etc/bind/named.conf.options` hoặc `/etc/named.conf`). Thêm đoạn sau vào trong khối `options { ... };`

```response-policy { zone "rpz"; };```

Bước 4: Khai báo Zone trong `named.conf.local` 
Thêm đoạn cấu hình zone vào file `/etc/bind/named.conf.local`:
```
zone "rpz" {
    type master;
    file "/etc/bind/db.rpz";
    allow-query { none; };
};
```
Bước 5: Tải lại dữ liệu

`sudo systemctl reload bind9` hoặc `sudo rndc reload`
### 6.2 Knot
Bước 1: Tải file  [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/powerdns.rpz) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/powerdns.rpz)

Bước 2: Chuyển vào `/etc/knot-resolver/powerdns.rpz`

Bước 3: Cấu hình `kresd.conf` Mở file config (thường là `/etc/knot-resolver/kresd.conf`). Thêm dòng sau vào:
```
-- Load module policy
modules = { 'policy' }

-- Load file RPZ
policy.add(policy.rpz(policy.DENY, '/etc/knot-resolver/powerdns.rpz'))
```
Bước 4: Khởi động lại
```sudo systemctl restart knot-resolver```
### 6.3 PowerDNS
Bước 1: Tải file  [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/powerdns.rpz) hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/powerdns.rpz)

Bước 2: Chuyển vào `/etc/knot-resolver/powerdns.rpz`
Bước 3: Tạo file `/etc/powerdns/recursor.lua` với nội dung:
```
rpzFile("/etc/powerdns/powerdns.rpz", {
    defpol = Policy.Custom,
    defcontent = "CNAME ." 
})
```
Bước 4: Cấu hình `recursor.conf`
Mở file `/etc/powerdns/recursor.conf`. Tìm và sửa dòng `lua-dns-script`:

```lua-dns-script=/etc/powerdns/recursor.lua```

Bước 5: khởi động lại

```sudo systemctl restart pdns-recursor```
## 7.Adaway
Bước 1: Tải hoặc thêm trực tiếp bộ lọc [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/adaway.txt)  hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/adaway.txt) 

Bước 2: Bấm vào nút cập nhật 

Bước 3: Chờ một lúc và tắt đi bật lại

## 8.DNSCloak
Bước 1: Tải file [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/host.txt) hoặc  [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/host.txt) 

Bước 2: Mở ứng dụng DNSCloak.

Bước 3: Chạm vào biểu tượng 3 dấu gạch ngang (Menu) ở góc trên bên trái.

Bước 4: Tìm mục Blacklists & Whitelists và chạm vào đó.

Bước 5: Nhấn vào dòng Pick Blacklist file....

Bước 6: Cửa sổ chọn file hiện ra, bạn tìm đến file blacklist.txt vừa lưu ở Bước 1 và chọn nó.

**QUAN TRỌNG: Gạt công tắc Enable Blacklist sang màu xanh (On).**

Bước 7: Về lại màn hình chính và nhấn nút Play (hình tam giác) ở đầu tên máy chủ để bắt đầu VPN.
## 9.dnsmasq
Bước 1: Tải về file cấu hình [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/dnsmasq.conf) hoặc  [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/dnsmasq.conf) 

Bước 2: Tạo một file cấu hình mới trong thư mục cấu hình của dnsmasq (VD:zalofucker)

```sudo nano /etc/dnsmasq.d/zalofucker.conf```

Bước 3: Mở cái file cấu hình mới vừa tạo và dán những gì có trong file đã có ở bước 1 vào

Bước 4: Lưu lại và khởi động bằng lệnh sau
```sudo systemctl restart dnsmasq```
### 9.1 Với Openwrt
Bước 1: Mở file cấu hình
```vi /etc/dnsmasq.conf```

Bước 2:Bấm phím `i` để vào chế độ chỉnh sửa, dán danh sách vào cuối file.

Bước 3:Bấm Esc, sau đó gõ :wq để lưu và thoát.

Bước 4: Khởi động lại dịch vụ bằng lệnh sau
```/etc/init.d/dnsmasq restart```
### 9.2 Với DD-WRT
Bước 1: Vào trang quản trị Router (Web GUI).

Bước 2: Tìm mục Services -> DNSMasq.

Bước 3: Tìm ô Additional DNSMasq Options (Tùy chọn bổ sung).

Bước 4: Dán danh sách trên vào ô đó.

Bước 5: Nhấn Save và Apply Settings.
## 10. RouterOS

Bước 1: Lưu file [này từ Github](https://raw.githubusercontent.com/zalofucker/fuck-you-zalo/refs/heads/main/mikrotik.rsc)  hoặc [này từ forgejo](https://codefloe.com/Zalofucker/fuck-you-zalo/raw/branch/main/mikrotik.rsc) 

Bước 2: Mở New Terminal.

Bước 3: Sử dụng lệnh sau để nhập dữ liệu:


```/import mikrotik.rsc```


**Nếu bạn không muốn tạo file, bạn cũng có thể copy toàn bộ nội dung script và dán (Paste) trực tiếp vào cửa sổ New Terminal là được.**

# 🤝 Đóng góp 
## Hiện tại tôi rất cần các bạn tìm ra những phốt của zalo để tôi up lên README vậy nên nếu bạn nào có vui lòng tạo issue giúp tôi!?!?!?

Dự án này cần sự chung tay của cộng đồng để liên tục cập nhật các tên miền mới của Zalo

Tạo một Issue/Pull mới thông báo vấn đề về việc chặn thiếu/bổ sung.
