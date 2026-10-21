# Write-up

## Đề cho
There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
## Solve
Phần này sau khi xem README.md, ta biết mình cần phải push lên flag.txt. Nhưng việc push cần email và name. Vậy nó kiếm đâu ra?
Lúc này ta phải biết vào ssh bandit31 để tìm được user và password.
```bash
bandit31@bandit:~$ cat .gitconfig 
[user]
        email = bandit31@overthewire.org
        name = bandit31
```
bài này chỉ khó chỗ này, còn đâu lại dễ.

## Key
`pWuj5jBQ6IgV0NXwiH6g1pXRF8******`