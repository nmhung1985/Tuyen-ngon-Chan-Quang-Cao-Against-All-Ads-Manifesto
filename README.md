# Tuyên ngôn Chặn Quảng Cáo



Có nhiều phương thức và ứng dụng chặn quảng cáo, bài viết này sẽ cố gắng tổng hợp tất cả các loại để giúp bạn chọn phương thức và ứng dụng tốt nhất cho mình.

Đây là bài viết tổng hợp quan trọng nên khả năng cao là sẽ được cập nhật thông tin lâu dài, dù có thể không thường xuyên. Phiên bản gốc luôn nằm trên GitHub: link ở đây.

## Tại sao cần chặn quảng cáo
Bạn chắc hẳn đã trải qua cảm giác mất hứng khi đang xem phim đến đoạn hay trên TV thì nhà đài cho dừng một lúc để quảng cáo? 

Trên thế giới Internet, hẳn thi thoảng bạn xem YouTube được một chút thì gặp video quảng cáo cả vài phút?

Bạn có biết gói data 4G của bạn bị hết dung lượng sớm vì bị quảng cáo chiếm tới 80% không?

Nghiêm trọng hơn, bạn có biết đôi khi các trang quảng cáo còn nhúng cả mã theo dõi hoặc thậm chí là bị chèn mã độc hại (tải ngầm virus hoặc đào bitcoin)?

Nói chung các dữ liệu rác rưởi và độc hại này thường chiếm trung bình ít nhất khoảng 40% trên các hệ thống hay thiết bị kết nối mạng của bạn:
- làm tốn dung lượng và khiến thông tin bạn cần bị tải chậm hơn
- làm tốn pin do dữ liệu luôn được tải ngầm
- gây ảnh hưởng tới việc bạn tận hưởng các nội dung thú vị.

Do đó, áp dụng phương thức chặn các dữ liệu rác này, mà ta sẽ gọi chung là **Chặn Quảng Cáo (CQC)**, hiệu quả sẽ khiến hệ thống hoặc thiết bị của bạn luôn chỉ tải nhanh chóng và thể hiện đúng thông tin cần thiết, giúp đem lại một trải nghiệm an toàn và vui vẻ.

## Cấp độ chặn quảng cáo
#### 1. Cấp 1 (tạm coi là "nguyên lý", "tiên đề"):

1.1.  Các tên miền quảng cáo không thể truyền dữ liệu nào đến hệ thống của bạn (lọc lớp mạng - network filter): đây là cách rất hiệu quả trong việc không để băng thông hệ thống bị quảng cáo chiếm dụng, tuy nhiên hạn chế hay được nhắc tới là hầu như không thể chặn quảng cáo của YouTube, cũng như có thể làm vỡ bố cục trang web.

1.2. Chỉ làm nhiệm vụ ẩn quảng cáo chứ không chặn (lọc lớp giao diện - cosmetic filter): không có khả năng giảm tải băng thông, nhưng bạn không phải nhìn thấy hay bị làm phiền, cũng như ưu điểm thường thấy là có thể chặn quảng cáo của YouTube, giữ bố cục trang web gọn gàng, **không bao giờ được áp dụng riêng** mà luôn bổ sung thêm cho nguyên lý trên, giúp đạt hiệu quả tốt nhất.

*Hình minh họa: Bên trái áp dụng nguyên lý 1 chặn được quảng cáo nhưng vẫn còn khoảng trống bị dư thừa. Bên phải là sau khi áp dụng thêm nguyên lý 2.*

![So sánh](https://cdn.adguard.com/public/Adguard/Blog/Android/comparison/ad_leftovers_resized.png?1)

#### 2. Cấp 2, phân loại theo phương thức:

2.1. Hosts/Tường lửa: 
- danh sách chặn được ghi trực tiếp vào cơ sở dữ liệu nội tại của thiết bị, được chính hệ thống nội tại chính chủ xử lý (tập tin hosts trên máy tính, Knox trên điện thoại Samsung)
- áp dụng nguyên lý 1

2.2. DNS:
- thiết lập hệ thống hoặc thiết bị để dùng DNS-có-tính-năng-chặn-quảng-cáo, DNS từ xa kia sẽ chịu trách nhiệm kiểm tra thông tin chặn
- người dùng Việt Nam có thể cảm thấy chậm hơn một chút
- áp dụng nguyên lý 1

2.3. VPN:
- chạy một VPN giả lập nội bộ để can thiệp thông tin lưu lượng mạng
- có thể hỗ trợ thêm 2 tính năng trên với đặc điểm: ứng dụng tự xử lý chứ hệ thống không xử lý
- có thể làm tốn pin hơn một chút (không đáng lo ngại vì hiện nay các ứng dụng đều tối ưu)
- chủ yếu cho điện thoại
- thường áp dụng nguyên lý 1 (có ngoại lệ)

2.4. Tiện ích (addon/extension) cho trình duyệt:
- tiện ích riêng đảm nhiệm chặn quảng cáo cho trình duyệt
- chủ yếu cho máy tính
- áp dụng kết hợp được cả 2 nguyên lý

#### 3. Cấp 3, phân loại theo độ bao phủ:

3.1. Cấp độ Mạng Nội Bộ: 
- chỉ cần thiết lập trên một thiết bị có chức năng quản lý hệ thống mạng trong nhà như Router (hay được gọi bình dân là "cục modem", "cục wifi") hoặc máy tính PC có cài hệ thống tường lửa đặc biệt (pfSense, pi-hole, Adguard Home v.v...).
- toàn bộ các thiết bị khác kết nối cùng mạng nội bộ này sẽ không cần làm gì thêm mà vẫn được chặn quảng cáo
- cách duy nhất để chặn quảng cáo trên các thiết bị như AppleTV, TV thông minh, IoT (Internet of Things) v.v...
- chủ yếu áp dụng nguyên lý 1 (ngoại trừ pfSense và một vài hệ thống tương đương)

3.2. Cấp độ Thiết bị: 
- thiết lập trên từng thiết bị muốn chặn quảng cáo
- toàn bộ các phần mềm, ứng dụng trên thiết bị đó sẽ được chặn quảng cáo
- chủ yếu áp dụng nguyên lý 1 (có ngoại lệ sẽ đề cập ở dưới)

3.3. Cấp độ Trình duyệt:
- chỉ hoạt động trên trình duyệt được thiết lập hoặc sử dụng trình duyệt chuyên chặn quảng cáo (ví dụ Brave)
- thường áp dụng được cả 2 nguyên lý

Từ các cách phân loại này, ngoài việc các chương trình và ứng dụng trên các nền tảng áp dụng riêng rẽ hoặc kết hợp các phương thức, thì bản thân chúng ta cũng có thể chọn áp dụng riêng rẽ hoặc kết hợp các chương trình và ứng dụng. Điều này khiến chúng ta có nhiều lựa chọn khá là phong phú :)

## Vậy chặn như thế nào?
Bạn có thể cũng đã từng nghe qua hoặc được chỉ cài phần mềm này, ứng dụng kia để chặn. Nhưng sau khi cài rồi bạn thấy hình như không hiệu quả lắm. Đó là vì:
1. Chương trình, phần mềm là để xử lý.
2.  Ngoài ra còn cần bộ lọc/danh sách chặn (filters list/hosts) phù hợp với khu vực, quốc gia thì mới tối ưu. (Do ứng dụng đều là của nước ngoài nên mặc định họ thường sẽ không kích hoạt bộ lọc cho Việt Nam)
3. Nhiều trang web có khả năng phát hiện người dùng đang chặn quảng cáo của họ, nên còn cần phải cài thêm ứng dụng "chống ứng dụng phát hiện chặn quảng cáo (anti-anti-adblock)". Có thể xem đây như cuộc chiến giữa người làm khóa và kẻ bẻ khóa vậy :)
4. Do đó, bạn lưu ý 3 bộ lọc dành cho Việt Nam tốt nhất hiện nay.
- [HostsVN của BigDargon](https://github.com/bigdargon/hostsVN): bộ lọc đang nổi gần đây, dần có mặt chính thức trong các ứng dụng nổi tiếng như Adguard, NextDNS, v.v..., áp dụng nguyên lý 1 nên dùng được trên nhiều phần mềm, ứng dụng (Minh bạch: Bản thân bài viết này trỏ tới nhiều bài hướng dẫn chi tiết bên HostsVN :)
- [ABPVN của hoangrio](https://github.com/abpvn/abpvn): có mặt chính thức trong vài ứng dụng nổi tiếng như Adblock Plus (tên nhóm lấy từ đây), uBlock Origin, v.v... , áp dụng kết hợp 2 nguyên lý nên hoạt động trên ít ứng dụng hơn (chủ yếu là cho các tiện ích cài bổ sung trình duyệt).
- [FMSF của nmtrung](https://github.com/nmtrung/FMSF-2.0): tác giả là thành viên voz.vn nên bộ lọc khá nổi bên đó, đáng tiếc là không thấy tác giả đề xuất được đưa vào các ứng dụng nổi tiếng, áp dụng kết hợp 2 nguyên lý như ABPVN.

## Hướng dẫn tổng quan

Các chương trình, phần mềm, ứng dụng được liệt kê theo đánh giá cá nhân tác giả dựa trên *tổng hợp của lần lượt* bốn yếu tố: tốt nhất, miễn phí, dễ cài đặt, trả phí. Thành ra ví dụ nếu ứng dụng trả phí vượt trội thì vẫn sẽ được liệt kê trước.

|[Mạng nội bộ](#mạng-nội-bộ)|[Máy tính (Windows/Mac)](#máy-tính)|[Android](#android)  |[iOS](#ios)|
|:-:|:-:|:-:|:-:|

### Mạng nội bộ
Đây là cấp độ khó nên người nào biết thiết lập cho cấp độ này thường là tay chuyên và không cần đọc bài viết này. Do đó, phần này sẽ không có nhiều thông tin.

Tuy nhiên, đối với dòng Router Asus vẫn có cách thiết lập khá dễ cho người có kiến thức máy tính trung bình. Mời bạn xem ở đây.

### Máy tính

1. Toàn bộ máy tính: Adguard (Trả phí, Windows, Mac) là phần mềm tốt nhất, nếu có thể nói là duy nhất. Cũng đa dạng nhất hiện nay khi có gần như đầy đủ phiên bản phủ hết các cấp độ trình bày ở trên.

2. Tiện ích cho trình duyệt: Cách tốt nhất không bị quảng cáo YouTube trên máy tính và đều miễn phí. Có rất nhiều, ví dụ Adguard vừa nói ở trên cũng có phiên bản riêng, Adblock Plus, Adblock, Adblocker v.v...
- uBlock Origin: tiện ích phổ biến nhất, nhưng lời khuyên là nên dùng 2 tiện ích ở dưới
- Nano Adblocker & Nano Defender: Nano Adblocker là bản fork của uBlock Origin với một số tối ưu, nên dùng kết hợp Nano Defender để tránh bị các trang web nhận diện là đang dùng trình chặn quảng cáo.

3. DNS: Xem trong bài hướng dẫn chung


### Android
- Adhell3 (Trả phí): tốt nhất, nhưng **chỉ hoạt động trên máy Samsung**, chèn thông tin trực tiếp vào hệ thống Knox của máy Samsung (không được Samsung hỗ trợ chính thức). Đang beta test vụ trả phí nên đến thời điểm này (29/7/2019) chưa thể mua được.

- Adguard Premium (Trả phí): loại giả lập VPN duy nhất hiện tại có thể áp dụng cả 2 nguyên lý, hỗ trợ DNS, HTTPS

- Blokada: giả lập VPN, có tính năng kết nối VPN thật (cần trả phí), DNS, chưa hỗ trợ HTTPS (tác giả biết nhưng đang cân nhắc vì sự bảo mật của người dùng -> có vẻ như là rất có trách nhiệm, nên lưu ý để ủng hộ :)

- AdClear: giả lập VPN, DNS, hỗ trợ HTTPS, có tính năng tường lửa

- AdAway (**Root**): chặn dạng hosts

- Disconnect Pro (Trả phí): không được đánh giá cao nhưng do hơi đặc biệt nên cần nhắc tới. Có vẻ như có mối quan hệ tốt nên là ứng dụng duy nhất được Samsung chính thức cho phép can thiệp Knox, và bộ lọc của họ được trình duyệt của Mozilla, Brave sử dụng chính thức. Có phiên bản chạy dạng VPN cho máy Android khác, tên "Disconnect Premium VPN". 

*Các ứng dụng đặc biệt*

- YouTube Vanced: ứng dụng chuyên chỉ để xem YouTube không quảng cáo

- Brave Browser/Firefox Focus: trình duyệt chuyên biệt chặn quảng cáo nên áp dụng được cả 2 nguyên lý, chặn được quảng cáo YouTube, dùng kết hợp bộ lọc của Disconnect và EasyList.

- Firefox (bản chuẩn cho Android): do có thể cài tiện ích như bản cho máy tính nên mọi thông tin đều tương tự như phần tiện ích cho máy tính.

### iOS
Đều là dạng chạy giả lập VPN
1. [Quantumult](https://github.com/bigdargon/hostsVN/wiki/Quantumult) (Trả phí): tốt nhất, bản chất là ứng dụng phân tích truy vấn mạng, nhưng được tận dụng để có thể chặn quảng cáo. Áp dụng nguyên lý 1.
2. [Surge](https://github.com/bigdargon/hostsVN/wiki/Surge): cách hoạt động như Quantumult, thiếu tính năng hơn một chút.
3. Adguard: trả phí khác gì miễn phí?

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEzNDIyODI2OCwxNzYyMTc1NzUyLDEzND
I4ODE0NDIsMzg3Mjg5ODM3LC0xNDkxMTEwNzU3LDgyMzk0MTUx
LDM5MTQ5MjQ0LC02MTI5MTk1MjcsLTcxNjE0MDM0OSwtNTQyMT
U0MTQsLTIxMDA2ODc4NDIsMzMyMzMxMzk4LC0xMTM5NTQ5NDQ5
LC00OTY0MDE5NSwtMTMyNDQxMTE0NCwtNjIwMTEyMjYzLDE2MD
c0NDI3OTMsOTMwODQ5MTAsLTIxNDQ5NDY0MDcsMTkxNzI3NjI1
OV19
-->