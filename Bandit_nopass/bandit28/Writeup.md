# Write-up

## Đề cho
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
Không khác gì bài trước nhưng bài này sẽ giúp ta ôn lại thêm kiến thức về git trong những level đầu
## Solve
Sau khi đã vô được `/repo`, ta sẽ mò trong log để mò lại xem có thay đổi gì không vì trong README không cho ta bất cứ manh mối nào
```bash
git log
```
Khi này ta thấy có 1 log rất kì lạ như sau
```git
commit de09b8205d8d115e2749670df21bf1882bc98e34 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sat Sep 26 21:54:43 2026 +0000

    fix info leak
```
Hoặc ta cứ `git show -a` mà vã
```bash
git show de09b8205d8d115e2749670df21bf1882bc98e34
```
## Key
`Em7eGtqaMySwNFjCpwzzHhLhos******`