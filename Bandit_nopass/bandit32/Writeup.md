# Write-up

## Đề cho
After all this git stuff, it’s time for another escape. Good luck!
## Solve
Khi ssh tới level, nó tự động mở một trình shell, mà mọi lệnh ta nhập đều bị in hoa. Nên chương trình sẽ không chạy được. Nhưng vẫn cho phép một số biến đặc biệt như `$0` vốn là để hiện ra tên chương trình. Nhưng khi ta nhập vào thì chương trình chạy lại và tự động văng ra shell bth.
```bash
0$
# Văng ra real shell
whoiam ## -> bandit33
cat /etc/bandit_pass/bandit33
```
## Key
`u4P2CyPOwPGLe94RdD9Uo2FxFw******`