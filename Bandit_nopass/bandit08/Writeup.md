# Write-up

## Đề cho
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
## Solve
```bash
sort data.txt | uniq -u
```
## Lesson
## 1. `sort` — Sắp xếp dòng

| Command | Chức năng |
|---|---|
| `sort file.txt` | Sắp xếp theo thứ tự từ điển |
| `sort -r file.txt` | Sắp xếp ngược |
| `sort -n file.txt` | Sắp xếp theo giá trị số |
| `sort -u file.txt` | Sắp xếp và loại bỏ dòng trùng |
| `sort -f file.txt` | Không phân biệt chữ hoa/thường |
| `sort -k2 file.txt` | Sắp xếp theo cột thứ 2 |
| `sort -t: -k3n file.txt` | Dùng `:` làm dấu phân cách, sắp xếp cột 3 theo số |

## 2. `uniq` — Xử lý dòng trùng

| Command | Chức năng |
|---|---|
| `uniq file.txt` | Loại các dòng trùng liền kề |
| `uniq -c file.txt` | Đếm số lần xuất hiện của mỗi nhóm dòng |
| `uniq -d file.txt` | Chỉ in các dòng trùng liền kề |
| `uniq -u file.txt` | Chỉ in các dòng không trùng liền kề |
| `uniq -i file.txt` | Không phân biệt chữ hoa/thường |

> **Lưu ý:** `uniq` chỉ xử lý các dòng trùng đứng cạnh nhau. Thường kết hợp với `sort` để xử lý toàn bộ file.

## 3. Kết hợp thường dùng trong CTF

### Loại bỏ dòng trùng

```bash
sort file.txt | uniq
```
## Key
`EjmOSvuAu7sGAHqHVcBDPirRe9******`