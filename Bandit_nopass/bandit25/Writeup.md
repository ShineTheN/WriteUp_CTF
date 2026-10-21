# Write-up

## Đề cho
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

NOTE: if you’re a Windows user and typically use Powershell to ssh into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.

## Solve
- Đầu tiên ta vào thử bandit, ls thấy một file privatekey. Dùng nó để đăng nhập vô lv 26 thì bị đá văng ra
- Ta vào ssh bandit25 tìm hiểu thì hint nằm ở 
```bash
cat /etc/passwd | grep bandit26
```
Sau đó ta cat thử file đó
```bash
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

exec more ~/text.txt
exit 0
```
Đây là dòng quan trọng
```bash
exec more ~/text.txt
```
- Khi có exac nếu nó hiện ra hết thì nó sẽ tắt luôn chương trình, còn khi có more, nếu chương trình không hiện hết thì nó sẽ thêm more, lúc này ta sẽ làm được bước kế tiếp. 
Mở Vim từ bên trong `more`

Khi đang dừng ở `--More--`, gõ:

Đây là phím tắt của `more` để mở nội dung đang xem bằng Vim. Vim chạy với quyền của bandit26.

Trong Vim, gõ:
```bash
    :set shell=/bin/bash
```
rồi nhấn **Enter**.

Gõ tiếp:
```bash
    :shell
```
rồi nhấn **Enter** lần nữa. Lệnh này mở một shell thật (`/bin/bash`) dựa trên shell mặc định vừa đổi ở bước 6, chạy với quyền bandit26.

Lấy mật khẩu level tiếp theo
```bash
    cat /etc/bandit_pass/bandit26
```
Vậy là xong level: shell giới hạn dựa trên pager (`more`) đã bị bẻ gãy bằng cách gọi Vim từ bên trong `more`, sau đó đổi shell mặc định của Vim và mở một shell thật từ đó.
## Key
`jHdv2ELQhT22BkprMNDjybZDAk******`