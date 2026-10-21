# Write-up

## Đề cho
The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Solve
cd về server chứa toàn bộ dữ liệu trên cd bằng 2 lần `cd ..`

Sau đó ta find theo đề yêu cầu
```bash
find . -type f -size 33c -user bandit7 -group bandit6
```

ta sẽ tìm được 1 dòng dẫn tới file bandit7.password `./var/lib/dpkg/info/bandit7.password`

```
cat /var/lib/dpkg/info/bandit7.password
``` 
## Key
`Bmnnvf82KzQlfxgAI2d1zYbr1u******`