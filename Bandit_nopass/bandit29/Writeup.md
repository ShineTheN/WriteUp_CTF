# Write-up

## Đề cho
There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.
(Y chang bài trước)
## Solve
C1 Show hết mọi thứ
```bash
git show -a
```
C2
Ta sẽ check từng branch và xem file README.md có khác gì không.
Cuối cùng README.md được đọc bởi dev sẽ ra flag
```bash
git branch -a
git checkout dev
cat README.md
```
## Key
`jq9Dfg2rXsfYsWMgFuKlXhphjd******`
