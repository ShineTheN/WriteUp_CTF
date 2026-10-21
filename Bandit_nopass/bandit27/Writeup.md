# Write-up

## Đề cho
There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.


## Solve
Bài này chỉ việc clone cái repo về máy, xong mở lên là có flag. Quan trọng ta phải biết là port thường đặt ngay sau tên miền chính và trước dấu 2 chấm.
```bash
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
```
Sau khi clone nó sẽ nhảy vào thư mục hiện tại của máy, ta có thể sử dụng
```bash
mktemp -d
```
để tạo ra một thư mục tạm để chứa repo.

## Key
`y8Yd2ssKcpHpud7UvOSOxwamRM******`