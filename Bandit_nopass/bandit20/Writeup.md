# Write-up

## Đề cho
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## Solve
Chạy command này trên 1 terminal
```bash
nc -l 1111
```

và 1 localhost để listen trên 1 terminal khác
```bash
./suconnect 1111
```
Quay lại bên localhost sau khi đã connect, ta gửi lại key level trước là sẽ nhận được key ở lv này. 
## Key
`bW9kBv5WC3P4yoDyf12LSdGuNz******`