Bài viết hướng dẫn cài Adhell3 cho dòng máy Samsung. Thông tin mới nhất luôn được cập nhật ở bài đầu này. (Các thông tin cũ nhưng có tính tham khảo sẽ được post ở dưới comment nếu cần).

___________________

### Adhell3 - App chặn quảng cáo hiệu quả nhất cho riêng dòng máy Samsung
Riêng đối với Samsung, hãng này có tích hợp module Knox trong các dòng máy của họ để thực hiện các tính năng bảo mật đặc biệt độc quyền, trong đó có tính năng tường lửa. Tận dụng module này, các nhà phát triển đã viết app Adhell3 để hỗ trợ chặn quảng cáo trên máy Samsung với các ưu điểm sau:
- **KHÔNG CẦN** root hay chạy VPN giả lập
- **KHÔNG** bị chậm như khi dùng cách chặn bằng DNS như trên Android Pie
- cực kỳ nhanh và hiệu quả do dùng sẵn module tường lửa chính hãng tích hợp sẵn
- nhờ lý do trên nên app không cần chạy nền, không tiêu tốn pin
- có thêm tính năng vô hiệu hóa thành phần của app (vd một số app đòi nhiều quyền truy cập danh bạ, hình ảnh không cần thiết)
- có thêm tính năng vô hiệu hóa các app ít dùng
- Điểm trừ: Samsung đã chặn cách kích hoạt miễn phí, nên hiện tại phải tốn phí. Nhưng phí chỉ tương đương 1-2 ly cà phê mà có giấy phép vĩnh viễn (không bị phiền với việc thao tác nhiều bước và phải làm mỗi 3 tháng một lần như lúc miễn phí).

### Thông tin về cách cài đặt
- Samsung không thích các loại app chặn quảng cáo này do có thể ảnh hưởng đến đối tác của họ. Nên các loại app này sẽ không bao giờ có bản public chính thức hoặc trên Play Store vì Samsung có thể chặn định danh (ID) của app khiến không hoạt động được. Để tránh bị Samsung làm phiền, bản thân tác giả không build sẵn app để chúng ta tải về. Do đó, đáng nhẽ mỗi người sẽ phải tự làm thao tác build và đổi ID của app. Tuy nhiên, trong cộng đồng có một người khác (CitizenXVIL) hỗ trợ build và đưa lên Mediafire. Vì vậy, thực ra thì chúng ta không cần phải làm gì phức tạp, mà đây chỉ là thông tin thêm cho các bạn rõ.

- Chỉ hỗ trợ Knox 2.6 trở lên. Để biết phiên bản Knox máy mình là gì, bạn vào `Cài đặt> Về điện thoại> Thông tin phần mềm` (Settings> About Phone> Software Information)

### Cách mua key
Nhóm tác giả đang thử nghiệm giới hạn nên có thể không mua được dễ dàng. Tuy nhiên, bài viết vẫn cung cấp thông tin cho những ai háo hức muốn thử nghiệm sớm và chịu khó trao đổi. Khi nào có thông tin mới thì bài viết cũng sẽ cập nhật ngay.

Đó là bạn có thể viết và gửi đề nghị tới địa chỉ email sau: **smileappbeta@gmail.com** 

### Tải về
Vào link MediaFire dưới đây và chỉ cần tải tập tin có tên "ah3_v3.2.xxx..." ở ngoài. 

[MediaFire](https://www.mediafire.com/folder/sb37c6gmhqgbn/AdHell+3)  

### Khởi chạy, cấu hình và sử dụng Adhell3
1. Mở Adhell3. Lần đầu tiên chạy:
- app sẽ đề nghị kích hoạt chức năng quản trị, chọn "Enable Admin permission"> "Activate"
- điền key Knox vào rồi "Submit/Activate License". Kể từ bây giờ Adhell3 sẽ chạy bình thường.
2. Vào "Domains"> "Providers", thêm hostsVN-dạng-domain theo link sau:
https://raw.githubusercontent.com/bigdargon/hostsVN/master/option/domain.txt
3. Vào "Domains"> "Blacklist", tạo thêm các rule sau:
`com.android.chrome|*|53`
**Lưu ý cho Note 9 và/hoặc Pie**: thêm `com.sec.android.app.sbrowser|*|53`
4. Về "Home", gạt để kích hoạt "Domain rules" và "Firewall rules".
5. 
a) Do Google tích hợp thêm khả năng cho phép Chrome tự bỏ qua DNS trên máy để dùng trực tiếp DNS 8.8.8.8 của họ (tính năng "Data Saver" cũng tương tự), khiến bộ lọc có thể không còn tác dụng. Khi đó, bạn tắt các tính năng này bằng cách sau:
- Gõ chính xác cụm sau **chrome://flags** để truy cập trang cấu hình. Ở ô tìm kiếm, gõ "async", bạn sẽ thấy "Async DNS Resolver". Chọn "Disable" để tắt.
- Chạm dấu ba chấm dọc để vào "Settings", chọn tiếp "Data Saver" và gạt sang "Off" để tắt.
b) Firefox đang dần tích hợp tính năng bảo mật DNS (DNS-over-HTTPS) nên có thể cũng bỏ qua DNS trên máy, khiến cũng bị tình trạng tương tự như trên. Bạn tắt bằng cách sau:
- Gõ chính xác cụm sau **about:config** để truy cập trang cấu hình.
- Gõ vào thanh tìm kiếm để tìm **network.trr.mode**. Chỉnh lại nếu cần để đảm bảo giá trị cho thuộc tính này là "0".

### Khắc phục một số vấn đề
Nếu bạn cần gỡ bỏ Adhell3 thì nhớ hủy quyền hạn quản trị bằng cách vào `Cài đặt> Màn hình khóa và bảo mật> Cài đặt bảo mật khác> Ứng dụng quản trị thiết bị` (Settings> Lock screen and security> Other security settings> Device admin apps).  



Như vậy là đã hoàn thành. Chúc mừng bạn đã chịu khó làm theo hướng dẫn của chúng tôi. Hãy thử trải nghiệm nhé, đảm bảo bạn sẽ thấy cách chặn quảng cáo trên Samsung hiệu quả hơn rất nhiều trên các máy Android khác và bên iOS.

Hình ảnh:
http://imgur.com/gallery/aKhDQvu
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5ODQ5OTIxMF19
-->