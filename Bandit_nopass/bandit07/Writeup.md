# Write-up

## Đề cho
The password for the next level is stored in the file data.txt next to the word millionth
## Solve
```bash
grep -n "millionth" data.txt 
```
## Lesson
Grep: syntax
``` 
grep [OPTIONS] PATTERN [FILE...]
```
| Lệnh | Tác dụng |
|---|---|
| `grep "abc" file.txt` | Tìm dòng chứa `abc` |
| `grep -i "abc" file.txt` | Không phân biệt chữ hoa/thường |
| `grep -n "abc" file.txt` | Hiển thị số dòng |
| `grep -v "abc" file.txt` | Hiển thị các dòng không chứa `abc` |
| `grep -r "abc" folder/` | Tìm đệ quy trong thư mục |
| `grep -l "abc" *` | Chỉ hiển thị tên file có kết quả |
| `grep -w "abc" file.txt` | Tìm từ nguyên vẹn `abc` |
| `grep -E "abc|xyz" file.txt` | Tìm dòng chứa `abc` hoặc `xyz` |
| `grep -rn "abc" .` | Tìm đệ quy, hiển thị số dòng |
## Key
`VR1ljMayciFxbnUokuQmJFw6QC******`