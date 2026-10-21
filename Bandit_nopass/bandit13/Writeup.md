# Write-up

## Đề cho
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14.
## Solve
``` bash
ls
cat sshkey.private
exit
nano bandit14.key
chmod 600 bandit14.key
ssh -i bandit14.key bandit14@bandit.labs.overthewire.org -p 2220
```

Using SSH with the -i option allows us to specify the private key file and log in directly as bandit14, gaining access to the next level.
## Key
`aaWecNkG4FhxJQxz07uiwzVP6b******`
