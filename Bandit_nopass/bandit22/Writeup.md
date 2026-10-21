# Write-up

## Đề cho
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
## Solve
Bài này khá đơn giản.
Như bài trước ta sẽ vào thư mực `ect/cron.d`. Tiếp theo, ta sẽ xem trong `cronjob_bandit23` có gì.
```bash
cat cronjob_bandit23

@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
```
```bash
cat /usr/bin/cronjob_bandit23.sh

#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```
Nó thực thi một file mà sẽ gửi password từ `/etc/bandit_pass/$myname` (ở đây là bandit23) đến `/tmp/$target`. Và ta sẽ cần tìm `target` là gì.

Quan sát file .sh ta nhận thấy target là một string được viết dưới dạng md5. Vậy thì dễ dàng ta sẽ tìm được target
```bash
echo "I am user bandit23" | md5sum
```
Vậy ta sẽ hoàn thành bài này bằng truy cập vô thư mục /tmp/(string đã mã hóa)
## Key
`gKXDTAXnIz3OBxiPjRZ2uqutUl******`