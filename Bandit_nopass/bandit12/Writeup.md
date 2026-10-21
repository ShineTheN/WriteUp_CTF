# Write-up

## Đề cho
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Solve
Copy file qua `/tmp/` để bắt đầu điều tra
```bash
xxd -r data.txt > /tmp/a/hex.txt
```
(Không dùng cp vì sẽ file không ra)
Sau đó, lặp đi lặp lại `file`, `gzip -d`, `tar -xf`, `gz2 -d`

là ta được file kết quả 
## Key
`qQYQiHOBPR8zR61qxYqX45quvi******`