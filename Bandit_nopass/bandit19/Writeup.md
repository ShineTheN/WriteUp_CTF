# Write-up

## Đề cho
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Solve
Đề cho một file là setuid binary. File này sau khi ta chạy
```bash
bandit19@bandit:~$ ./bandit20-do 
Run a command as another user.
Example: ./bandit20-do whoami
```

```bash
./bandit20-do whoami
bandit20
```

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Key
`4pIjcunZ0fK2vmp3IwfG8Vf7Vh******`