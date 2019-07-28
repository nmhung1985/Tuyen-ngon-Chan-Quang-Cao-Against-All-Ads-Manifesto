# Tuyên ngôn Chặn Quảng Cáo



Có nhiều phương thức và ứng dụng chặn quảng cáo, bài viết này sẽ cố gắng tổng hợp tất cả các loại để giúp bạn chọn phương thức và ứng dụng tốt nhất cho mình.

## Tại sao cần chặn quảng cáo
Bạn chắc hẳn đã trải qua cảm giác mất hứng khi đang xem phim đến đoạn hay trên TV thì nhà đài cho dừng một lúc để quảng cáo? Cũng như xem YouTube được một chút thì gặp video quảng cáo cả vài phút?

Bạn có biết gói data 4G của bạn bị hết dung lượng sớm vì bị quảng cáo chiếm tới 80% không?

Nói chung quảng cáo thường chiếm trung bình khoảng 50% trên các hệ thống hay thiết bị kết nối mạng của bạn, vừa làm tốn dung lượng và khiến thông tin bạn cần bị tải chậm hơn, vừa gây ảnh hưởng tới việc bạn tận hưởng các nội dung thú vị.

Do đó, áp dụng phương thức chặn quảng cáo hiệu quả sẽ khiến hệ thống hoặc thiết bị của bạn luôn tải đúng thông tin cần thiết, không ngầm tải hoặc thể hiện các thông tin rác rưởi và độc hại.

## Cấp độ chặn quảng cáo
#### 1. Cấp 1, mà ta tạm coi là "nguyên lý", "tiên đề" có 2 phương thức:

1.1.  Các tên miền quảng cáo không thể truyền dữ liệu nào đến hệ thống của bạn (lọc mạng - network filter): đây là cách rất hiệu quả trong việc không để băng thông hệ thống bị quảng cáo chiếm dụng, tuy nhiên hạn chế hay được nhắc tới là hầu như không thể chặn quảng cáo của YouTube.

1.2. Hệ thống của bạn vẫn tải dữ liệu từ các tên miền quảng cáo, nhưng sẽ không hiển thị cho bạn thấy (lọc trang trí - cosmetic filter): băng thông vẫn bị quảng cáo chiếm dụng, nhưng bạn không phải nhìn thấy hay bị làm phiền, cũng như ưu điểm thường thấy là có thể chặn quảng cáo của YouTube.

#### 2. Cấp 2, phân loại theo phương thức:

2.1. Hosts/Tường lửa: 
- danh sách chặn được ghi trực tiếp vào hệ thống nội tại của thiết bị, được chính hệ thống nội tại chính chủ xử lý (tập tin hosts trên máy tính, hệ thống đa ứng dụng Knox trên điện thoại Samsung)
- áp dụng nguyên lý 1.1

2.2. DNS:
- thiết lập hệ thống hoặc thiết bị dùng DNS-có-tính-năng-chặn-quảng-cáo, DNS từ xa kia sẽ chịu trách nhiệm kiểm tra thông tin chặn
- người dùng Việt Nam có thể cảm thấy chậm, nhưng không quá khác biệt
- áp dụng nguyên lý 1.1

2.3. VPN:
- chạy một VPN giả lập nội bộ để đọc các kết nối và đưa ra quyết định chặn hay không
- phổ biến trên điện thoại
- thường áp dụng nguyên lý 1.1 (có ngoại lệ)

2.4. Tiện ích (addon/extension) cho trình duyệt:
- tiện ích riêng đảm nhiệm chặn quảng cáo cho trình duyệt
- chủ yếu cho máy tính
- áp dụng kết hợp được cả 2 nguyên lý

#### 3. Cấp 3, phân loại theo độ phủ:

3.1. Cấp độ Mạng Nội Bộ: 
- chỉ cần thiết lập trên một thiết bị có chức năng quản lý hệ thống mạng trong nhà như Router (hay được gọi bình dân là "cục modem", "cục wifi") hoặc máy tính PC có cài hệ thống tường lửa đặc biệt (pfSense v.v...).
- toàn bộ các thiết bị khác kết nối cùng mạng nội bộ này sẽ không cần làm gì thêm mà vẫn được chặn quảng cáo
- chủ yếu áp dụng nguyên lý 1.1 (ngoại trừ cách hệ thống kiểu pfSense)

3.2. Cấp độ Thiết bị: 
- thiết lập trên từng thiết bị muốn chặn quảng cáo
- toàn bộ các phần mềm, ứng dụng trên thiết bị đó sẽ được chặn quảng cáo
- chủ yếu áp dụng nguyên lý 1.1 (tất nhiên cũng có ngoại lệ sẽ đề cập ở dưới)

3.3. Cấp độ Trình duyệt:
- chỉ hoạt động trên trình duyệt được thiết lập hoặc sử dụng trình duyệt chuyên chặn quảng cáo (ví dụ Brave)
- thường áp dụng được cả 2 nguyên lý

Từ các cách phân loại này, ngoài việc các chương trình và ứng dụng trên các nền tảng áp dụng riêng rẽ hoặc kết hợp các phương thức, thì bản thân chúng ta cũng có thể chọn áp dụng riêng rẽ hoặc kết hợp các chương trình và ứng dụng. Điều này khiến chúng ta có nhiều lựa chọn khá là phong phú :)

## Vậy chặn như thế nào?
Bạn có thể cũng đã từng nghe qua hoặc được chỉ cài phần mềm này, ứng dung kia để chặn. Nhưng sau khi cài rồi bạn thấy hình như không hiệu quả lắm. Đó là vì:
1. Chương trình, phần mềm là để xử lý.
2. Ngoài ra còn bộ lọc/danh sách chặn (filters list/hosts) phù hợp với khu vực, quốc gia thì mới tối ưu. (Do phần mềm là của nước ngoài nên mặc định họ thường sẽ không kích hoạt bộ lọc cho Việt Nam)
3. Do đó, bạn lưu ý 2 bộ lọc dành cho Việt Nam tốt nhất hiện nay:
3.1 HostsVN của BigDargon
3.2 ABPVN của Nhóm ABPVN

## Hướng dẫn tổng quan

|[Mạng nội bộ](#mạng-nội-bộ)|[Máy tính (Windows/Mac)](#máy-tính)|[Android](#android)  |[iOS](#ios)|
|:-:|:-:|:-:|:-:|

### Mạng nội bộ
Đây là cấp độ khó nên người nào biết thiết lập cho cấp độ này thường là tay chuyên và không cần đọc bài viết này. Do đó, phần này sẽ không có nhiều thông tin.
Tuy nhiên, đối với dòng Router Asus vẫn có cách thiết lập khá dễ cho người có kiến thức máy tính trung bình. Mời bạn xem ở đây.

### Máy tính

1. Adguard (Trả phí, Windows, Mac): phần mềm chặn cho toàn bộ máy tính (cấp độ 3.2) tốt nhất. Cũng đa dạng nhất hiện nay khi có gần như đầy đủ phiên bản phủ hết các cấp độ trình bày ở trên.
2. Tiện ích cho trình duyệt: Cách tốt nhất không bị quảng cáo YouTube trên máy tính và đều miễn phí. Có rất nhiều, ví dụ Adguard vừa nói ở trên cũng có phiên bản riêng, Adblock Plus, Adblock, Adblocker v.v...
- uBlock Origin: tiện ích phổ biến nhất, nhưng lời khuyên là nên dùng 2 tiện ích ở dưới
- Nano Adblocker & Nano Defender: Nano Adblocker là bản fork của uBlock Origin với một số tối ưu, nên dùng kết hợp Nano Defender để tránh bị các trang web nhận diện là đang dùng trình chặn quảng cáo.
3. DNS: Xem trong bài hướng dẫn chung


### Android
1. Adhell3 (Trả phí): tốt nhất, nhưng **chỉ hoạt động trên máy Samsung**. Chèn thông tin trực tiếp vào hệ thống Knox của máy Samsung. Không hỗ

2. Adaway (**Root**, miễn phí): chặn dạng hosts.
3. Disconnect Pro (Trả phí): ứng dụng duy nhất được Samsung chính thức cho phép kết nối với Knox.

*Ngoại trừ 2 app trên, còn lại tất cả app ở dưới đều chạy dạng VPN nội bộ*

3. Adguard (Trả phí): loại giả lập VPN duy nhất hiện tại có thể áp dụng cả 2 nguyên lý, hỗ trợ cả cách DNS

4. AdClear (Miễn phí): giả lập VPN, DNS, hỗ trợ HTTPS

5. Blokada (




Phải sửa thử nhiều cái. Thử nhánh master. Sync StackEdit

You can use the [editor on GitHub](https://github.com/nmhung1985/Tuyen-ngon-Chan-Quang-Cao-Against-All-Ads-Manifesto/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/nmhung1985/Tuyen-ngon-Chan-Quang-Cao-Against-All-Ads-Manifesto/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTIyNDQyMjc1OSwtMTQ0Nzc2ODE1OCwxMj
AxMTA2NDQ4LDIwMDEwMTIwMSw4MjY1ODI5MiwtMTI4ODYzMzcx
OCwtODIxNDc5MTk1LC03OTgyNzk5OTQsLTQ1ODQ4NTM5NSwtMT
A5NTc5MjI2LDE2NDkzMzY5MzMsNDMzNTI0NzgyLDE1MTUwODMw
NDIsNjY3NTE0NTksODc0NjIwMzMwLC05NTg2NDU5NDIsLTc3Mz
g2NDgyMl19
-->