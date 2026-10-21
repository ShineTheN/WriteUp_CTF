# Write-up

## Đề cho

## Solve
```bash
nmap -sV -p 31000-32000 localhost
```
-sV dò phiên bản dịch vụ cổng
```bash
openssl s_client -connect localhost:31790
```

```bash
openssl s_client -connect localhost:31790 -quiet
```

Sau đó làm tương tự như lv 14 - lv15 khi đã có private key
```bash
nano 1.txt
chmod 700 1.txt
ssh -i 1.txt -p 2220 bandit17@bandit.labs.overthewire.org
``` 
## Key
`pWXMAZoxGC8JmDMfmT5MGEsobM******`
