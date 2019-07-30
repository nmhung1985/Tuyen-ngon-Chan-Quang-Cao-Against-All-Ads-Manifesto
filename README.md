# Tuyên ngôn Chặn Quảng Cáo

***Lời nhắn nhủ**: Đây đảm bảo là bài viết tổng hợp đầy đủ nhất bằng tiếng Việt về việc chặn quảng cáo. Nếu thấy hữu ích, bạn hãy hướng dẫn hoặc giới thiệu bài viết này cho những người xung quanh mình nhé. Hãy cùng giúp nhau có một không gian Internet sạch và an toàn!*

Nếu hay xem TV, bạn chắc hẳn đã trải qua cảm giác mất hứng khi phim đang đến đoạn hay thì đài truyền hình cho dừng một lúc để quảng cáo?

Sang thời đại Internet, hẳn bạn cũng đã gặp tình cảnh xem YouTube được một chút thì gặp video quảng cáo cả vài phút?

Bạn có biết gói data 4G của bạn có thể hết dung lượng sớm vì bị quảng cáo [chiếm tới 79%](https://www.businessinsider.com/enders-analysis-ad-blocker-study-finds-ads-take-up-79-of-mobile-data-transfer-2016-3) không?

Nghiêm trọng hơn, bạn có biết nhiều trang web âm thầm nhúng mã theo dõi, lừa bạn đăng nhập tài khoản tài chính, hoặc thậm chí chủ động gieo rắc mã độc hại vào thiết bị của bạn (tải ngầm virus hoặc đào bitcoin)?

Nếu nhà có trẻ em, chắc bạn cũng không muốn trẻ vô tình thấy những nội dung người lớn?

Nói chung các dữ liệu rác rưởi và độc hại này (gọi chung là "**quảng cáo**") thường chiếm trung bình ít nhất từ [40%](https://blog.donbowman.ca/2018/03/20/advertisement-traffic-is-40-of-bandwidth/) đến [60%](http://web.archive.org/web/20190730053655/https://forums.voz.vn/showpost.php?p=149131673&postcount=49) trên các hệ thống hay thiết bị kết nối mạng của bạn:
- Làm tốn dung lượng và khiến thông tin bạn cần bị tải chậm hơn
- Làm tốn pin do dữ liệu luôn được tải ngầm
- Gây ảnh hưởng tới trải nghiệm và sự an toàn của bạn khi thưởng thức các nội dung thú vị trên Internet.

Do đó, áp dụng phương thức **Chặn Quảng Cáo** (CQC) hiệu quả sẽ khiến hệ thống hoặc thiết bị của bạn luôn tải nhanh chóng và thể hiện đúng thông tin cần thiết, giúp đem lại một trải nghiệm an toàn và vui vẻ.

*Hình minh họa 1: Sau khi áp dụng chặn quảng cáo, lưu lượng và thời gian tải được giảm tới gần 3 lần*

![So sánh trước và sau khi chặn](https://cdn.adguard.com/public/Adguard/Blog/AGHome/devcomp.jpg)

## Nguyên lý chặn quảng cáo
1.  Lọc lớp mạng (network filter): 
- Không dữ liệu quảng cáo nào có thể đi vào hệ thống
- Hiệu quả trong việc không để băng thông hệ thống bị quảng cáo chiếm dụng
- Hạn chế hay được nhắc tới là khó chặn quảng cáo của YouTube, cũng như có thể làm vỡ bố cục trang web.

2. Lọc lớp giao diện (cosmetic filter):
- Chỉ làm nhiệm vụ ẩn dữ liệu quảng cáo chứ không chặn
- Không có khả năng giảm tải băng thông, nhưng vẫn giúp bạn không phải nhìn thấy hay bị làm phiền bởi quảng cáo
- Ưu điểm thường thấy là có thể ẩn quảng cáo của YouTube, giữ bố cục trang web gọn gàng
-  **Không bao giờ được áp dụng riêng** mà luôn bổ sung thêm cho nguyên lý trên, giúp nâng cao khả năng chặn.

*Hình minh họa 2: Bên trái áp dụng nguyên lý 1 chặn được quảng cáo nhưng vẫn còn khoảng trống bị dư thừa. Bên phải là sau khi áp dụng thêm nguyên lý 2.*

![So sánh nguyên lý 1 và 2](https://cdn.adguard.com/public/Adguard/Blog/Android/comparison/ad_leftovers_resized.png?1)

## Cấp độ chặn quảng cáo

### 1. Phân loại theo phương thức:

1.1. Hosts/Tường lửa: 
- Danh sách chặn được ghi trực tiếp vào cơ sở dữ liệu nội tại của thiết bị, được chính hệ thống bảo mật nội tại chính chủ xử lý (tập tin hosts trên máy tính, Knox trên điện thoại Samsung)
- Áp dụng nguyên lý 1

1.2. Hệ thống phân giải tên miền (DNS):
- Thiết lập hệ thống hoặc thiết bị để dùng DNS-có-tính-năng-chặn-quảng-cáo, DNS từ xa kia sẽ chịu trách nhiệm lọc và chặn
- Hệ thống máy chủ chưa tối ưu cho Việt Nam, nên người dùng Việt Nam có thể cảm thấy chậm hơn một chút
- Áp dụng nguyên lý 1

1.3. Mạng riêng ảo (VPN):
- Chạy một VPN giả lập nội bộ để can thiệp thông tin lưu lượng mạng
- Có thể hỗ trợ thêm 2 tính năng trên với đặc điểm: ứng dụng tự xử lý chứ hệ thống không xử lý
- Có thể làm tốn pin hơn một chút (không đáng lo ngại vì hiện nay các ứng dụng đều tối ưu)
- Chủ yếu cho điện thoại
- Thường áp dụng nguyên lý 1 (có ngoại lệ)

1.4. Tiện ích (addon/extension) cho trình duyệt:
- Tiện ích riêng đảm nhiệm chặn quảng cáo cho trình duyệt
- Chủ yếu cho máy tính
- Áp dụng kết hợp được cả 2 nguyên lý

[**Đặc biệt**] Lọc lớp mã hóa (HTTPS filter): Không phải phương thức hay nguyên lý chặn, mà là tính năng bổ sung trong ứng dụng
- Bổ sung khả năng đọc và phân tích các truy vấn/kết nối được mã hóa
- Giúp nguyên lý 1 có thể chặn thêm được một phần quảng cáo mà Youtube, Facebook mã hóa
- Nếu không có tính năng này thì dù áp dụng được nguyên lý 2 vẫn có thể không ẩn được quảng cáo YouTube

### 2. Phân loại theo độ bao phủ:

2.1. Cấp độ Mạng Nội Bộ: 
- Chỉ cần thiết lập trên một thiết bị có chức năng quản lý hệ thống mạng trong nhà như Router (hay được gọi bình dân là "cục modem", "cục wifi") hoặc thiết bị/máy tính có cài hệ thống chặn đặc biệt (pfSense, pi-hole, Adguard Home v.v...).
- Toàn bộ các thiết bị khác kết nối cùng mạng nội bộ này sẽ không cần làm gì thêm mà vẫn được chặn quảng cáo
- **Cách duy nhất** để chặn quảng cáo trên các thiết bị như AppleTV, TV thông minh, IoT (Internet of Things) v.v...
- Chủ yếu áp dụng nguyên lý 1 (ngoại trừ pfSense và một vài hệ thống tương đương)

2.2. Cấp độ Thiết bị: 
- Thiết lập trên từng thiết bị muốn chặn quảng cáo
- Toàn bộ các phần mềm, ứng dụng trên thiết bị đó sẽ được chặn quảng cáo
- Chủ yếu áp dụng nguyên lý 1

2.3. Cấp độ Trình duyệt:
- Chỉ hoạt động trên trình duyệt được thiết lập, hoặc có thể kể đến trình duyệt tích hợp sẵn tính năng chặn quảng cáo (ví dụ Brave)
- Thường áp dụng được cả 2 nguyên lý

Từ các cách phân loại này, ngoài việc các chương trình, phần mềm và ứng dụng (từ đây gọi chung là "**ứng dụng**") trên các nền tảng áp dụng riêng rẽ hoặc kết hợp các phương thức, thì bản thân chúng ta cũng có thể chọn riêng rẽ hoặc kết hợp các chương trình và ứng dụng. Điều này khiến chúng ta có nhiều lựa chọn khá là phong phú :)

Do đó, bài viết này không thể hướng dẫn chi tiết tường tận từng ứng dụng. Mà mục đích chính vẫn là các thông tin cơ bản để bạn hiểu và từ đó chọn được cái phù hợp với mình nhất. Tuy nhiên, ở các phần kế tiếp vẫn có tổng quan sơ lược gợi ý một số ứng dụng nên dùng cho từng hệ thống, và dẫn link tới hướng dẫn chi tiết tương ứng. (Lưu ý: do người viết thu thập từ nhiều nguồn khác nhau nên không thể đảm bảo các bài hướng dẫn có chất lượng đồng đều, chỉ đọc tham khảo và chỉ luôn tải hoặc mua bản mới nhất ở trang gốc).

## Các bước cơ bản để chặn quảng cáo
Bạn có thể cũng đã từng nghe qua hoặc được chỉ cài phần mềm này, ứng dụng kia để chặn. Nhưng sau khi cài rồi bạn thấy hình như không hiệu quả lắm. Vậy hãy kiểm tra lại từng bước:
1. Đầu tiên, phải có hệ thống/ứng dụng để xử lý.
2. Ngoài ra còn cần bộ lọc/danh sách chặn (filters lists/hosts) phù hợp với khu vực, quốc gia thì mới tối ưu. (Do ứng dụng đều là của nước ngoài nên mặc định họ thường sẽ không kích hoạt bộ lọc cho Việt Nam)
3. Nhiều trang web có khả năng phát hiện người dùng đang chặn quảng cáo của họ, nên còn cần phải cài thêm ứng dụng "chống ứng dụng phát hiện quảng cáo bị chặn (anti-anti-adblock)". Có thể xem đây như cuộc chiến giữa người làm khóa và kẻ bẻ khóa vậy :)
4. Trong trường hợp chặn theo phương thức DNS: Chrome với tính năng Async DNS Resolver, cũng như các trình duyệt tích hợp chức năng mã hóa DNS hoặc "tiết kiệm dung lượng" (data saver), có thể bỏ qua danh sách lọc. Khi đó cần tắt các tính năng này.
5. Lưu ý 3 bộ lọc dành cho Việt Nam tốt nhất hiện nay.
- [HostsVN của BigDargon](https://github.com/bigdargon/hostsVN): bộ lọc đang nổi gần đây, dần có mặt chính thức trong các ứng dụng nổi tiếng như Adguard, nextdns, v.v..., áp dụng được cho nguyên lý 1 nên dùng được trên nhiều phần mềm, ứng dụng (Minh bạch: Bản thân bài viết này trỏ tới nhiều bài hướng dẫn chi tiết bên HostsVN :)
- [ABPVN của hoangrio](https://github.com/abpvn/abpvn): có mặt chính thức trong vài ứng dụng nổi tiếng như Adblock Plus, uBlock Origin, v.v... , áp dụng được cho 2 nguyên lý nên hoạt động trên ít ứng dụng hơn (chủ yếu là cho các tiện ích cài bổ sung trình duyệt).
- [FMSF của nmtrung](https://github.com/nmtrung/FMSF-2.0): tác giả là thành viên voz.vn nên bộ lọc khá nổi bên đó, đáng tiếc là không thấy tác giả đề xuất được đưa vào các ứng dụng nổi tiếng, áp dụng được cho 2 nguyên lý như ABPVN.

## Tổng quan và sơ lược các ứng dụng nên dùng

Các ứng dụng được liệt kê theo *cảm nhận tổng hợp* của cá nhân người viết dựa trên bốn yếu tố: dễ cài đặt và thiết lập ngay, miễn phí, tốt nhất, trả phí. Thành ra ví dụ nếu ứng dụng trả phí vượt trội thì vẫn sẽ được liệt kê trước.

- [Mạng nội bộ](#mạng-nội-bộ)
- [Máy tính (Windows/Mac)](#máy-tính)
- [Android](#android)
- [iOS](#ios)
- [DNS](#dns)


### Mạng nội bộ
Đây là cấp độ khó nên người nào biết thiết lập cho cấp độ này thường là đã có kiến thức CNTT tốt. Do đó, phần này sẽ không có các thông tin chi tiết mà chỉ cung cấp một số link hướng dẫn.

- Router Asus (chạy [firmware Merlin](https://www.asuswrt-merlin.net/)): cách dễ nhất cho người có kiến thức máy tính trung bình. Chỉ hoạt động trên một số loại router của Asus như AC66U, AC68U, AC86U, AC88U v.v... Hướng dẫn cho thiết bị đã flash Merlin: [1](https://github.com/nmhung1985/Tuyen-ngon-Chan-Quang-Cao-Against-All-Ads-Manifesto/blob/master/AsusRouter.md)
- [pi-hole](https://pi-hole.net/): ứng dụng chặn quảng cáo cho mạng nội bộ phổ biến nhất hiện nay. Phát triển ban đầu cho dòng Raspberry Pi nhưng hiện tại có thể chạy trên nhiều thiết bị và hệ điều hành. Hướng dẫn: [1](http://web.archive.org/web/20190730080355/https://cuccode.com/pihole.html), [video](https://www.youtube.com/watch?v=1lmQqGZf_4A), [voz](https://forums.voz.vn/showthread.php?t=7437968)
- [Adguard Home](https://adguard.com/en/adguard-home/overview.html): tham vọng thay thế pi-hole nên hỗ trợ nhiều nền tảng và tích hợp sẵn nhiều tính năng. Hướng dẫn: [1](https://adguard.com/en/adguard-home/overview.html)
- [pfSense](https://www.pfsense.org/), [OPNsense](https://opnsense.org/), Sophos [XG Firewall Home Edition](https://www.sophos.com/en-us/products/free-tools/sophos-xg-firewall-home-edition.aspx) hoặc [UTM Home Edition](https://www.sophos.com/en-us/products/free-tools/sophos-utm-home-edition.aspx), [nethserver](https://www.nethserver.org/), [Untangle NG Firewall](https://www.untangle.com/get-untangle/), [ClearOS](https://www.clearos.com/), [VyOS](https://vyos.io/): là các bộ ứng dụng hoặc thậm chí là một hệ điều hành chỉ làm nhiệm vụ tường lửa, bảo mật nên chặn quảng cáo là một tính năng trong đó. Cực mạnh mẽ và nhiều cấu hình nâng cao, phức tạp. Thường áp dụng được cả 2 nguyên lý và HTTPS.

### Máy tính

1. Toàn bộ máy tính: Adguard (Trả phí, [Windows](https://adguard.com/en/adguard-windows/overview.html), [Mac](https://adguard.com/en/adguard-mac/overview.html)) là phần mềm tốt nhất, nếu có thể nói là duy nhất. Cũng đa dạng nhất hiện nay khi có gần như đầy đủ phiên bản phủ hết các cấp độ trình bày ở trên. Hướng dẫn: [1](https://win10.vn/adguard-premium-post6073.html), [2](http://echip.com.vn/adguard-cong-cu-chan-quang-cao-manh-me-cho-may-tinh-va-dien-thoai-a20170523105438589-c1079.html)

2. Tiện ích cho trình duyệt: Cách tốt nhất không bị quảng cáo YouTube trên máy tính và đều miễn phí. Có rất nhiều, ví dụ Adguard vừa nói ở trên cũng có phiên bản riêng, Adblock Plus, Adblock, Adblocker v.v...

2.1. Các trình duyệt cùng nhân với Chrome/Firefox:
- uBlock Origin: tiện ích phổ biến nhất, nhưng lời khuyên là nên dùng 2 tiện ích ở dưới
- [Nano Adblocker](https://github.com/NanoAdblocker/NanoCore) & [Nano Defender](https://jspenguin2017.github.io/uBlockProtector/): ==**Tốt nhất!**== Nano Adblocker là bản fork của uBlock Origin với một số tối ưu, nên dùng kết hợp Nano Defender để tránh bị các trang web nhận diện là đang dùng trình chặn quảng cáo. Hướng dẫn: Vào kho tiện ích của hai trình duyệt này và gõ tên các tiện ích vừa nói ở trên để cài.

2.2. Các trình duyệt khác (Edge, Safari, Opera, Yandex): tiện ích [Adguard cho trình duyệt](https://adguard.com/en/adguard-browser-extension/edge/overview.html) là tốt nhất.

**Đang vội và muốn thử ngay?** Nano Adblocker & Nano Defender

### Android
- [AdClear](https://adclear.com/en/adclear-installation.php): giả lập VPN, DNS, hỗ trợ HTTPS, có tính năng tường lửa, chưa hỗ trợ thêm bộ danh sách lọc. Mặc định không thiết lập chặn hết tất cả ứng dụng trên thiết bị mà chỉ những ứng dụng AdClear cho rằng có thể có quảng cáo, còn lại để người dùng khám phá cách bật/tắt chặn đối với **từng** ứng dụng. 

- [Blokada](https://blokada.org/): giả lập VPN, có tính năng kết nối VPN thật (cần trả phí), DNS, chưa hỗ trợ HTTPS (tác giả biết nhưng đang cân nhắc vì sự bảo mật của người dùng -> có vẻ như là rất có trách nhiệm, nên lưu ý để ủng hộ :). Hướng dẫn: [1](https://trainghiemso.vn/blokada-chan-quang-cao-tren-android/)

- [Adguard Premium](https://adguard.com/en/adguard-android/overview.html) (Trả phí): ==**Tốt nhất!**== Loại giả lập VPN duy nhất hiện tại có thể áp dụng cả 2 nguyên lý, hỗ trợ DNS, HTTPS. Hướng dẫn: [1](http://www.techrum.vn/threads/tai-ng-dung-adguard-premium-chan-quang-cao-khi-xem-phim-luot-web-tren-android.193532/), [2](https://giasutintuong.com/phan-mem/adguard-premium-v2-11-81-viet-hoa-huong-dan-cai-dat-va-cau-hinh-chi-tiet.html), [3](https://c.mi.com/thread-928981-1-0.html).

- [Adguard Content Blocker](https://adguard.com/en/adguard-content-blocker/overview.html): chỉ hỗ trợ Samsung Internet Browser và Yandex Browser, không hỗ trợ HTTPS, áp dụng 2 nguyên lý

- [Nebulo](https://play.google.com/store/apps/details?id=com.frostnerd.smokescreen): giả lập VPN, ứng dụng duy nhất trong danh sách này có hỗ trợ DNS mã hóa, chưa hỗ trợ HTTPS

- [AdAway](https://adaway.org/) (**phải root**): chặn dạng hosts, liệt kê ở đây vì đã nổi tiếng lâu đời chứ để dùng ngay thì khó.

- [Adhell3](https://gitlab.com/fusionjack/adhell3) (Trả phí): ==**Tốt nhất!**== **cho và chỉ duy nhất máy Samsung**, chèn thông tin trực tiếp vào hệ thống Knox của máy Samsung (không được Samsung hỗ trợ chính thức). Đang beta test vụ trả phí nên đến thời điểm này (29/7/2019) chưa thể mua được.

- Disconnect Pro (Trả phí): không được đánh giá cao nhưng do hơi đặc biệt nên cần nhắc tới. Có vẻ như có mối quan hệ tốt nên là ứng dụng duy nhất được Samsung chính thức cho phép can thiệp Knox, và bộ lọc của họ được trình duyệt của Mozilla, Brave sử dụng chính thức. Có phiên bản chạy dạng VPN cho các máy Android khác, tên "Disconnect Premium VPN". 

*Các ứng dụng đặc biệt*

- [YouTube Vanced](https://vanced.app/): ứng dụng chuyên chỉ để xem YouTube không quảng cáo. Hướng dẫn: [1](https://cellphones.com.vn/sforum/thu-thuat-huong-dan-su-dung-youtube-vanced-tren-android-hoan-toan-mien-phi)

- [Brave Browser](https://play.google.com/store/apps/details?id=com.brave.browser&hl=en_US)/[Firefox Focus](https://play.google.com/store/apps/details?id=org.mozilla.focus&hl=en_US): trình duyệt chuyên biệt chặn quảng cáo nên áp dụng được cả 2 nguyên lý, chặn được quảng cáo YouTube, dùng kết hợp bộ lọc của Disconnect và EasyList.

- [Firefox](https://play.google.com/store/apps/details?id=org.mozilla.firefox&hl=en_US) (bản chuẩn cho Android): do có thể cài tiện ích như bản cho máy tính nên mọi thông tin đều tương tự như phần tiện ích cho máy tính.

**Đang vội và muốn thử ngay?** AdClear (hoặc Blokada), Youtube Vanced
### iOS
1. Dạng chạy giả lập VPN
- [Surge](https://itunes.apple.com/app/surge-3/id1442620678?mt=8): bản chất là ứng dụng phân tích truy vấn mạng, nhưng được tận dụng để có thể chặn quảng cáo. Cần trả phí mới có tính năng HTTPS. Áp dụng nguyên lý 1. Hướng dẫn: [1](https://github.com/bigdargon/hostsVN/wiki/Surge)

- [Adguard](https://itunes.apple.com/app/adguard-adblock-privacy/id1047223162?mt=8): thiếu các tính năng DNS, tự tạo bộ lọc. Có phần trả phí để nâng cấp lên bản Premium. Dần dần tương lai bản này và bản Pro ở dưới sẽ có tính năng giống nhau, chỉ khác phần cách thức thanh toán. Hướng dẫn: [1](https://github.com/bigdargon/hostsVN/wiki/Adguard)

- [Adguard Pro](https://itunes.apple.com/app/apple-store/id1126386264?mt=8) (trả phí): Hoạt động tương tự Adguard Premium trên Android. Nhưng chưa hỗ trợ HTTPS. Hướng dẫn: [1](https://github.com/bigdargon/hostsVN/wiki/Adguard-Pro)

- [Quantumult](https://itunes.apple.com/app/quantumult/id1252015438?mt=8) (Trả phí): ==**Tốt nhất!**== Tương tự như Surge sau khi trả phí nâng cấp. Hướng dẫn: [1](https://github.com/bigdargon/hostsVN/wiki/Quantumult)

2. Trình duyệt riêng biệt:  [Brave Browser](https://play.google.com/store/apps/details?id=com.brave.browser&hl=en_US)/[Firefox Focus](https://play.google.com/store/apps/details?id=org.mozilla.focus&hl=en_US) như trên Android

**Đang vội và muốn thử ngay?** Surge, Adguard

### DNS
1. Như đã giới thiệu ngắn gọn ở các phần trước, DNS là định nghĩa hệ thống phân giải tên miền, mà ở đây ta cũng dùng để nói ngắn gọn phương thức chặn mà theo đó bạn thiết lập cho hệ thống/thiết bị kết nối tới hệ thống DNS khác:
- Hệ thống DNS ở xa đó sẽ đảm nhiệm việc lọc và chặn tên miền, rồi mới trả lại thông tin để thiết bị của bạn kết nối tới.
- **Có lẽ cũng là cách dễ nhất**, vì hệ thống DNS ở xa xử lý rồi nên bạn không cần cấu hình, cài đặt gì phức tạp.
- Áp dụng được trên tất cả nền tảng (do DNS là yếu tố cơ bản để một hệ thống mạng hoạt động). Ngoại trừ một số trường hợp, ví dụ như trên điện thoại thì có vẻ do quy định chung nào đó mà các nhà sản xuất không có phần cấu hình thay đổi DNS của kết nối dữ liệu di động (3G, 4G) nếu không root hoặc jailbreak.
- Trên Android, ngoài cách thủ công thì có các ứng dụng để đổi DNS cũng bằng cách chạy giả lập VPN. Vừa xung đột với ứng dụng chạy VPN khác, vừa chỉ có mỗi tính năng DNS, nên tất nhiên lời khuyên là dùng luôn các ứng dụng chặn quảng cáo có tích hợp DNS.

2. Các nhà cung cấp DNS: Adguard DNS có thể xem là tốt nhất cho đến khi thời gian gần đây đang nổi lên nextdns. Vì với Adguard DNS bạn không có tùy chọn bộ lọc theo ý mình, trong khi nextdns có lựa chọn.

3. DNS mã hóa: Một số hệ thống và ứng dụng bắt đầu hỗ trợ các loại DNS mã hóa như DNS-over-HTTPS (DoH), DNS-over-TLS (DoT). Nếu có thể, hãy luôn chọn và thiết lập sử dụng các *DNS-chặn-quảng-cáo-có-mã-hóa* này.
**Lưu ý**: Nếu bạn dùng phương thức chặn DNS mà sử dụng trình duyệt tích hợp sẵn tính năng mã hóa DNS nhưng lại kết nối tới DNS-không-có-chặn-quảng-cáo của họ, thì cần tắt tính năng mã hóa DNS này trong trình duyệt (đọc thêm ý 4 ở phần [Các bước cơ bản để chặn quảng cáo](#các-bước-cơ-bản-để-chặn-quảng-cáo))

5. Hướng dẫn:
- [Adguard DNS](https://adguard.com/en/adguard-dns/overview.html#instruction)
- [nextdns](https://www.nextdns.io/): tạo tài khoản để có thể xem hướng dẫn riêng

## Việc chặn quảng cáo liên quan như thế nào với các ứng dụng bảo mật, chống virus?
Đây là câu hỏi rất hợp lý. 

Đúng vậy, ban đầu các ứng dụng chống virus và ứng dụng chặn quảng cáo (theo đúng nghĩa chỉ chặn quảng cáo) là các ứng dụng chuyên biệt chỉ làm đúng nhiệm vụ của mình.

Nhưng khi virus, mã độc dần được phát triển theo hướng lây lan qua mạng, thì ứng dụng chặn quảng cáo, với khả năng lọc và chặn các tên miền của mình, lại vô tình có tác dụng trong việc ngăn chặn các **tên miền phân phối** virus, mã độc.

Tức ứng dụng chặn quảng cáo **không có bộ máy phân tích** để nhận diện virus, mã độc, mà chỉ ngăn chặn truy cập các tên miền có chứa các virus, mã độc đó.

Trong khi đó, các ứng dụng bảo mật, diệt virus lại thấy mảng chặn quảng cáo cũng khá hấp dẫn, có thể giúp tăng doanh thu bán sản phẩm nên họ cũng đang có xu hướng tích hợp thêm tính năng mới này.

Ngoài ra:
- Ứng dụng bảo mật thường rất cồng kềnh và nặng nề, do ít nhất phải có bộ máy phân tích nhận diện virus, mã độc.
- Ứng dụng bảo mật tốt thì thường có giá đắt hơn nhiều so với ứng dụng chặn quảng cáo.

Cho nên những người cẩn thận vẫn có thể thích cài nhiều ứng dụng cho an toàn. Nhưng riêng tác giả bài viết này hiện chỉ dùng các ứng dụng chặn quảng cáo.

## Thông tin thêm
Nếu có thông tin gì cần biết thêm hoặc chỉ đơn giản là có cảm nhận hoặc ý kiến gì về bài viết, bạn có thể gửi email cho người viết theo địa chỉ:
nmhung1985 [A CÒNG] gmail.com
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1MjQyNzgyOSwtMTczMzc4MzMyOCwtMT
E2MDYyNDMzMSw4NjEyNzEzMzQsMjc4NDEwNjI3LDgxNzYyMDQz
NCwxNTk1Mjk1NTEyLDEyNzE3NDU2MjEsMjIxMTY5OTYxLC0xNT
EyNzE1ODY3LDE4NjU3MjIxODMsNjQ3ODE3OTk0LC01MjQzNjQ2
MTEsNTYzMjEyNzU1LC02NjI1ODkzNjYsMTA4NDYwMzU5NywxND
Q5NTgzNTgxLC0yMDQ4NTIwMDgzLDE2NDU2NjA5MzMsLTIyNTg5
NjA4XX0=
-->