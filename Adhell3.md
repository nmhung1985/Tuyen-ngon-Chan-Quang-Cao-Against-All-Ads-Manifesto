# Adhell3 - App chặn quảng cáo hiệu quả nhất cho riêng dòng máy Samsung
Riêng đối với Samsung, hãng này có tích hợp module Knox trong các dòng máy của họ để thực hiện các tính năng bảo mật đặc biệt độc quyền, trong đó có tính năng tường lửa. Tận dụng module này, các nhà phát triển đã viết app Adhell3 để hỗ trợ chặn quảng cáo trên máy Samsung với các ưu điểm sau:
- **KHÔNG CẦN** root 
-  **KHÔNG** chạy nền, **KHÔNG** làm tốn pin như cách chặn dạng tạo VPN giả lập nội bộ
- **KHÔNG** bị chậm như cách chặn dạng DNS
- cực kỳ nhanh và hiệu quả do mọi thứ được chính module tường lửa chính hãng xử lý
- có thêm tính năng vô hiệu hóa thành phần của app (vd một số app đòi nhiều quyền truy cập danh bạ, hình ảnh không cần thiết)
- có thêm tính năng vô hiệu hóa các app ít dùng
- Điểm trừ: Samsung đã chặn cách kích hoạt miễn phí, nên hiện tại phải tốn phí. Nhưng phí chỉ tương đương 1-2 ly cà phê mà có giấy phép vĩnh viễn (không bị phiền với việc thao tác nhiều bước và phải làm mỗi 3 tháng một lần như lúc miễn phí).

### Thông tin về cách cài đặt
- Samsung không hỗ trợ các loại app chặn quảng cáo này do có thể ảnh hưởng đến lợi ích của nhiều bên, nên các loại app này sẽ không bao giờ có bản công khai chính thức hoặc trên Play Store. Để tránh bị Samsung làm phiền, bản thân tác giả không build sẵn app để tải về, mà đáng nhẽ mỗi người sẽ phải tự làm thao tác build và đổi ID của app. Tuy nhiên, trong cộng đồng có một người khác đã hỗ trợ build sẵn. Vì vậy, thực ra thì chúng ta không cần phải làm gì phức tạp, mà đây chỉ là thông tin thêm cho các bạn rõ.

- Chỉ hỗ trợ Knox 2.6 trở lên. Để biết phiên bản Knox máy mình là gì, bạn vào `Cài đặt> Về điện thoại> Thông tin phần mềm` (Settings> About Phone> Software Information)

### Cách mua key
Nhóm tác giả đang thử nghiệm giới hạn nên có thể cần chịu khó chờ. 
1. Đầu tiên bạn tham gia vào Discord chính thức của Adhell3 tại https://discord.gg/prqxx5D

Đó là bạn có thể viết và gửi đề nghị tới địa chỉ email sau: **smileappbeta@gmail.com** 

### Tải về
Vào link MediaFire dưới đây và chỉ cần tải tập tin có tên **ah3_v3.2.xxx...** ở ngoài. 

[Bản build của CitizenXVIL trên MediaFire](https://www.mediafire.com/folder/sb37c6gmhqgbn/AdHell+3)  

### Khởi chạy, cấu hình và sử dụng Adhell3
1. Mở Adhell3. Lần đầu tiên chạy:
- app sẽ đề nghị kích hoạt chức năng quản trị, chọn "Enable Admin permission"> "Activate"
- điền key Knox vào rồi "Submit/Activate License". Kể từ bây giờ Adhell3 sẽ chạy bình thường.
2. Vào "Domains"> "Providers", thêm hostsVN-dạng-domain theo link sau:
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/domain.txt
3. Vào "Domains"> "Blacklist", tạo thêm các rule sau:
  Trình duyệt Chrome: `com.android.chrome|*|53`
  Trình duyệt của Samsung (**có thể chỉ cần làm cho Note 9 và/hoặc Pie**): `com.sec.android.app.sbrowser|*|53`
4. Về "Home", gạt để kích hoạt "Domain rules" và "Firewall rules".
5. 
a) Do Google tích hợp thêm khả năng cho phép Chrome tự bỏ qua DNS trên máy để dùng trực tiếp DNS 8.8.8.8 của họ (tính năng "Data Saver" cũng tương tự), khiến bộ lọc có thể không còn tác dụng. Khi đó, bạn tắt các tính năng này bằng cách sau:
- Gõ chính xác cụm sau **chrome://flags** để truy cập trang cấu hình. Ở ô tìm kiếm, gõ "async", bạn sẽ thấy "Async DNS Resolver". Chọn "Disable" để tắt.
- Chạm dấu ba chấm dọc để vào "Settings", chọn tiếp "Data Saver" và gạt sang "Off" để tắt.

b) Firefox đang dần tích hợp tính năng bảo mật DNS (DNS-over-HTTPS) nên có thể cũng bỏ qua DNS trên máy, khiến cũng bị tình trạng tương tự như trên. Bạn tắt bằng cách sau:
- Gõ chính xác cụm sau **about:config** để truy cập trang cấu hình.
- Gõ vào thanh tìm kiếm để tìm **network.trr.mode**. Chỉnh lại nếu cần để đảm bảo giá trị cho thuộc tính này là **0**

### Khắc phục một số vấn đề
Nếu bạn cần gỡ bỏ Adhell3 thì nhớ hủy quyền hạn quản trị bằng cách vào `Cài đặt> Màn hình khóa và bảo mật> Cài đặt bảo mật khác> Ứng dụng quản trị thiết bị` (Settings> Lock screen and security> Other security settings> Device admin apps).  



Như vậy là đã hoàn thành. Chúc mừng bạn đã chịu khó làm theo hướng dẫn của chúng tôi. Hãy thử trải nghiệm nhé, đảm bảo bạn sẽ thấy cách chặn quảng cáo trên Samsung hiệu quả hơn rất nhiều trên các máy Android khác và bên iOS.

Hình ảnh:
http://imgur.com/gallery/aKhDQvu
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI0NzkzNDY1OCwxMDYxNTQxMTMyXX0=
-->