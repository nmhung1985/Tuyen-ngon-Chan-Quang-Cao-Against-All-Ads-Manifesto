# Adhell3 - Ứng dụng chặn quảng cáo hiệu quả nhất cho riêng dòng máy Samsung
Riêng đối với Samsung, hãng này có tích hợp module Knox trong các dòng máy của họ để thực hiện các tính năng bảo mật đặc biệt độc quyền, trong đó có tính năng tường lửa. Tận dụng module này, các nhà phát triển đã viết ứng dụng Adhell3 để hỗ trợ chặn quảng cáo trên máy Samsung với các ưu điểm sau:
- **KHÔNG CẦN** root 
-  **KHÔNG** chạy nền, **KHÔNG** làm tốn pin như cách chặn dạng tạo VPN giả lập nội bộ
- **KHÔNG** bị chậm như cách chặn dạng DNS
- Cực kỳ nhanh và hiệu quả do mọi thứ được chính module tường lửa chính hãng xử lý
- Có thêm tính năng vô hiệu hóa thành phần của ứng dụng (vd một số ứng dụng đòi nhiều quyền truy cập danh bạ, hình ảnh không cần thiết)
- Có thêm tính năng vô hiệu hóa các ứng dụng ít dùng


![Hình 1](https://i.imgur.com/OxcgCcc.jpg)

### Thông tin về cách cài đặt
- Samsung không hỗ trợ các loại ứng dụng chặn quảng cáo này do có thể ảnh hưởng đến lợi ích của nhiều bên, nên các loại ứng dụng này sẽ không bao giờ có bản công khai chính thức hoặc trên Play Store. Để tránh bị Samsung làm phiền, bản thân tác giả không tạo sẵn ứng dụng để tải về. Trước đây, đáng nhẽ mỗi người sẽ phải tự làm thao tác build và đổi ID của ứng dụng. Tuy nhiên, trong cộng đồng có một người đã hỗ trợ build sẵn. Vì vậy, thực ra thì chúng ta không cần phải làm gì phức tạp, mà đây chỉ là thông tin thêm cho các bạn rõ.

- Để kích hoạt ứng dụng, vẫn phải cần có mã key từ Samsung, gọi là KPE (Knox Platform for Enterprise). Trước đây, Samsung cho cá nhân được quyền tạo ra key này để thử nghiệm, có thể tạo lại mỗi 3 tháng. Tuy nhiên, hiện tại Samsung chỉ bán quyền tạo key này cho đối tác doanh nghiệp. Trong cộng đồng có một người khác ủng hộ tác giả nên họ đã đăng ký làm doanh nghiệp đối tác đó để có quyền tạo key thoải mái có thời hạn vĩnh viễn.

- Chỉ hỗ trợ Knox 2.6 trở lên. Để biết phiên bản Knox máy mình là gì, bạn vào `Cài đặt> Về điện thoại> Thông tin phần mềm` (Settings> About Phone> Software Information)

### Cách mua key
Nhóm tác giả đang thử nghiệm giới hạn nên phải làm việc như trong hội kín :D 
1. Đầu tiên bạn tham gia vào Discord chính thức của Adhell3 tại https://discord.gg/prqxx5D
2. Nhóm tác giả đã yêu cầu người viết bỏ các thông tin chi tiết. Nên để biết thêm, bạn có thể hỏi người viết qua email:
nmhung1985 [A CÒNG] gmail.com

### Tải về
Vào link MediaFire dưới đây và chỉ cần tải tập tin có tên **ah3_v3.2.xxx...** ở ngoài. 

[Bản build của CitizenXVIL trên MediaFire](https://www.mediafire.com/folder/sb37c6gmhqgbn/AdHell+3)  

### Khởi chạy, cấu hình và sử dụng Adhell3
1. Mở Adhell3. Lần đầu tiên chạy:
- Ứng dụng sẽ đề nghị kích hoạt chức năng quản trị, chọn "Enable Admin permission"> "Activate"
- Điền key đã mua vào rồi "Submit/Activate License". Kể từ bây giờ Adhell3 sẽ chạy bình thường.
2. Vào "Domains"> "Providers", thêm hostsVN-dạng-domain theo link sau:
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/domain.txt

![Hình 2](https://i.imgur.com/mfiU6BF.jpg)

3. Vào "Domains"> "Blacklist", tạo thêm các rule sau:\
Trình duyệt Chrome: `com.android.chrome|*|53`\
Trình duyệt của Samsung (**có thể chỉ cần làm cho Note 9 và/hoặc Pie**): `com.sec.android.app.sbrowser|*|53`

4. Về "Home", gạt để kích hoạt "Domain rules" và "Firewall rules".

5. 
a) Do Google tích hợp thêm khả năng cho phép Chrome tự bỏ qua DNS trên máy để dùng trực tiếp DNS 8.8.8.8 của họ (tính năng "Data Saver" cũng tương tự), khiến bộ lọc có thể không còn tác dụng. Khi đó, bạn tắt các tính năng này bằng cách sau:
- Gõ chính xác cụm sau **chrome://flags** để truy cập trang cấu hình. Ở ô tìm kiếm, gõ "async", bạn sẽ thấy "Async DNS Resolver". Chọn "Disable" để tắt.
- Chạm dấu ba chấm dọc để vào "Settings", chọn tiếp "Data Saver" và gạt sang "Off" để tắt.
![Hình 3](https://i.imgur.com/PB65rB9.jpg)

b) Firefox đang dần tích hợp tính năng bảo mật DNS (DNS-over-HTTPS) nên có thể cũng bỏ qua DNS trên máy, khiến cũng bị tình trạng tương tự như trên. Bạn tắt bằng cách sau:
- Gõ chính xác cụm sau **about:config** để truy cập trang cấu hình.
- Gõ vào thanh tìm kiếm để tìm **network.trr.mode**. Chỉnh lại nếu cần để đảm bảo giá trị cho thuộc tính này là **0**

### Khắc phục vấn đề
Nếu bạn cần gỡ bỏ Adhell3 thì nhớ hủy quyền hạn quản trị bằng cách vào `Cài đặt> Màn hình khóa và bảo mật> Cài đặt bảo mật khác> Ứng dụng quản trị thiết bị` (Settings> Lock screen and security> Other security settings> Device admin apps).  

Như vậy là đã hoàn thành. Chúc mừng bạn đã chịu khó làm theo hướng dẫn của chúng tôi. Hãy thử trải nghiệm nhé, đảm bảo bạn sẽ thấy cách chặn quảng cáo trên Samsung hiệu quả hơn rất nhiều trên các máy Android khác và bên iOS.

Trang tổng hợp hình ảnh minh họa:
http://imgur.com/gallery/aKhDQvu
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMTA5MjIxMDgsLTE4OTEyNDEyMjYsLT
EzODQxMjYyMDQsMTgyNTg2MDYzNiwyMDI3NzY5MjAyLC0xMDIy
NDg1NTUzLC0yOTk5MjMwNDEsLTEyNjk0MDc2OSw0MTYzNzk0ND
gsNTc1MjIxNjE0LDEwNjE1NDExMzJdfQ==
-->