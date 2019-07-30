Quên ko hỏi rõ của bạn là AC66U hay là AC66U**-B1**. Tạm thời mình viết cho loại thường, KO PHẢI B1 nhé.

1. 
- Đầu tiên là cần có 1 cái USB dành riêng cho router, sẽ gắn liền với router suốt. Dung lượng thì yêu cầu rất ít (512MB), nhưng usb dung lượng cỡ này thì thường đời cũ, có thể lại chậm (?!). Nói chung là trừ khi bạn nắm rõ thông số usb, còn ko thì có thể post mẫu usb bạn có lên đây để mọi người xem có ok ko.
- Chương trình để thao tác dòng lệnh ssh trong router. Tải [putty.exe]("https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html") là gọn nhẹ nhất.
- Bộ lọc sẽ dùng là hostsVN của Big Dargon. Mình đánh giá là bộ lọc ổn nhất cho VN hiện tại, vì tác giả dùng pi-hole để lọc và hiện vẫn thường xuyên tương tác với mọi người để sửa lỗi. Bạn có thể vào trao đổi tại [topic này]("https://tinhte.vn/threads/huong-dan-chan-quang-cao-trong-ung-dung-bang-surge-adguard-pro-shadowrocket-va-adblock.2844988/").

2. Log vào trang quản lý router. Giả sử IP 192.168.1.1 nhé.
a) Ở LAN> DHCP Server, phần IP Pool Starting Address. Nếu bạn đã từng chỉnh rồi thì thôi, còn bình thường mặc định là 192.168.1.2 thì bạn chỉnh lên vài số, nói chung nên là 192.168.1.10, tránh ko để thiết bị nào dùng IP 192.168.1.2-192.168.1.9.
b) Ở Administration> System chỉnh:
Enable JFFS custom scripts and configs: Yes
Format JFFS partition at next boot: Yes
Enable SSH: Yes
Allow SSH access from WAN: No (chỉ cho login từ LAN/internal cho an toàn)
Timezone: GMT + 7 Bangkok Hanoi Jakarta

**Apply **cho router **reboot**.

3. Dùng putty để đăng nhập vào router thông qua ssh. Mở router lên, ở ngay giao diện mặc định ban đầu, nhập IP của router của bạn vào ô Host name (or IP address) rồi Open. Dùng tên đăng nhập như trang quản lý. Khi nói tới gõ lệnh là mặc định nói tới dùng trong putty.

4. Trừ khi bạn đã biết format usb sang dạng ext2 của Linux. Còn ko thì thường sẽ là fat32, ntfs. Khi đó chúng ta sẽ format lại usb như sau.
a) Cắm USB vào, thường thì router sẽ tự nhận. Tại putty, gõ lệnh
**mount** 
để xem. Nhớ để ý của bạn là **a, a1-2-3, hay b, b1-2-3** để làm cho đúng các bước sau nhé. Ví dụ của mình:

    **/dev/sda1 on /tmp/mnt/PpA** type ext2 (rw,nodev,relatime,barrier=1,data=writeback)
    **/dev/sdb on /tmp/mnt/PpB** type tntfs (rw,nodev,relatime,uid=0,gid=0,umask=00 v.v...)

b) unmount/eject usb để chuẩn bị format. Gõ lệnh:
umount -f /dev/sda1

c) Nếu là a1-2-3, b1-2-3 thì không làm bước này. Còn nếu là a,b (không số) thì chạy thêm các lệnh sau:

dd count=1 bs=512 if=/dev/zero of=/dev/sda && sync
fdisk /dev/sda
nhấn **o** để tạo table phân vùng
nhấn **n** để tạo phân vùng
nhấn **p** để thiết lập phân vùng này là primary
nhấn **1** để thiết lập làm phân vùng đầu tiên
nhấn **Enter** hai lần để dùng thông số mặc định
nhấn **w** để thật sự xử lý và ghi thay đổi vào USB

Từ đây USB của bạn sẽ được nhận là a1-2-3, b1-2-3, vd /dev/sda## 1

d) Gõ lệnh sau để format thành ext2 và đặt tên cho ổ:
mke2fs /dev/sda## 1 -t ext2 -L **Tên-Ổ-USB**

e) **Reboot** router và vào putty check lại sẽ thấy. Gõ lệnh:
**mount**
    **/dev/sda1 on /tmp/mnt/Tên-Ổ-USB** type ext2
    

5. Cài đặt Entware (bộ công cụ Linux tối giản cho router). Tiếp tục vẫn ở putty, chạy các lệnh, lưu ý cả **./** này nọ nhé:
    cd /tmp
    wget -c -O entware-ngu-setup.sh https://hqt.ro/files/entware-ng/universal/entware-ngu-setup.sh
    chmod +x ./entware-ngu-setup.sh
    ./entware-ngu-setup.sh

Script bắt đầu cài, sẽ hỏi nên cài vào đâu, thì bạn chọn số tương ứng. Nếu làm như từ đầu tới giờ thì sẽ gõ **1**.
    Info: like /tmp/mnt/sda1/jffs_scripts_backup.tgz Info: Looking for available partitions...
    [1] --> /tmp/mnt/sda1
    => Please enter partition number or 0 to exit
    [0-1]:

Hỏi dung lượng swap, chọn 512MB số **2**.
    Router model
    RT-AC66U
    ---------
    SWAP FILE
    ---------
    Choose swap file size (Highly Recommended)
    1. 256MB
    2. 512MB (recommended)
    3. 1024MB
    4. Skip this step, I already have a swap file / partition
       or I don't want to create one right now
    Enter your choice [ 1 - 4 ]

Enter một hai lần nữa là sẽ xong.

6. Cài bộ script quản lý chung. Trong putty gõ tiếp lệnh:
`/usr/sbin/curl -Os https://raw.githubusercontent.com/decoderman/amtm/master/amtm && sh amtm`

Script này đơn giản nên cũng chỉ cần Enter hay Yes là xong.

7. Dùng script quản lý chung kia để bắt đầu cài Diversion và pixelserv-tls - chính là bộ công cụ chặn quảng cáo. Trong putty, gõ:
**amtm**
- Menu sẽ hiện lên, chọn **1** để bắt đầu cài Diversion.
- Đầu tiên sẽ cho bạn lựa chọn giao diện, màu sắc, chọn cái nào vừa mắt bạn, mặc định là **1**.
- Chọn phiên bản, chúng ta sẽ chọn Diversion *Standard* bằng số **2**.
- Sẽ hiện tiếp một số thông tin về việc chọn IP ảo cho pixelserv-tls (đó là lí do vì sao chúng ta nãy sửa cái dải IP ở LAN> DHCP). Cơ bản là gán cho pixelserv-tls một IP *chưa bị dùng* bởi thiết bị nào khác và *không thuộc* dải IP được cấp phát, ví dụ 192.168.1.2.
- Hỏi có cần log để tra cứu. Thường thì chọn **2** để ko log cho nhẹ.
- Cài xong có thể sẽ hiện lên giao diện Diversion. Bạn cứ nhấn **e** (nghĩa là Exit) (có thể nhiều lần) để thoát hết ra lại dòng lệnh của router.

8. Cập nhật pixelserv-tls lên bản mới. Gõ lại lệnh:
**amtm**
- Chọn **4**.
- Chọn tiếp **2** để cài bản statiscally linked.
- Chọn **2** để cài bản cho mipsel (AC66U thường).
- Gõ **yes** để tiến hành cài.
- Cài xong lại **e**, **e**, **e** hết để thoát hết về lại dòng lệnh router.

9. Chạy Diversion để chọn dùng bộ lọc cho Việt Nam.
a) Để mở Diversion, có 2 cách:
- Chạy lệnh: **diversion**
- Chạy lệnh: **amtm** rồi chọn **1**.

b) Chọn bộ lọc Việt Nam: Sau khi Diversion chạy menu lên rồi thì tiếp tục
- chọn **b** (blocking file)
- chọn **1** (Change composition)
- chọn **2** (Customize hosts list)
- chọn **1** (Customize primary list Standard) -> Nếu ko có thì cứ làm tiếp
- chọn **2** (Remove hosts list) và làm theo hướng dẫn để xoá hết list trong đó. (Mặc định thì chỉ cần chọn **1** (enter line number) một lần).
- xong rồi chọn **1** (Add hosts list) và dán link của hostsVN:
`https://raw.githubusercontent.com/bigdargon/hostsVN/master/hosts`
- Chọn **e** (Exit). Diversion sẽ hỏi cập nhật ko, chọn **1** (Yes).

10. **Reboot **router một lần cuối cùng để mọi thứ mượt mà! :beauty:

Thông tin thêm:
- Diversion là trình chặn quảng cáo chính, tổng hợp và tạo danh sách bộ lọc dạng hosts rồi đưa qua dnsmasq xử lý. Pixelserv-tls thì là một web server mini nhỏ gọn để hỗ trợ chặn các trang mã hóa https.
- Vào [url]http://192.168.1.2/servstats[/url] để xem thống kê của pixelserv-tls. Tất nhiên thay 192.168.1.2 bằng IP ảo mà bạn đã cài.
- Nếu tò mò, thích tìm hiểu, bạn chạy Diversion, chọn **l** để bật log, rồi sau đó chọn **f** rồi **2** để xem Diversion chặn những gì trong nhà. Nếu nhà nhiều thiết bị thì nhìn rất phê :D Còn lại nói chung nên tắt log để giảm tải.
- Tác giả Diversion bàn luận ở đây. Forum này cũng là forum chuyên về bàn luận router của Asus và Merlin firmware.
[url]https://www.snbforums.com/threads/diversion-the-router-ad-blocker.48538/page-71#post-447604[/url]
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMjI2MzQ0MjcsNzMwOTk4MTE2XX0=
-->