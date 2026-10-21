# Write-up

Đề kêu sử dụng password đã tìm thấy ở level trước để login vào SSH bằng user bandit1 

Ta ls, thấy có file `-`

Nếu chỉ dùng cat thông thường thì nó sẽ hiểu là đang đọc input và chờ nhập dữ liệu từ bàn phím (Có thể kết thúc khúc này bằng Ctrl + D)

Vậy solve chúng ta sẽ là dùng

```bash
cat /.-
``` 
## Lesson
Du trong linux là viết tắt của Disk usage
du -ah xem dung lượng tất cả các file
Sử dụng `./` trước cat để chỉ đường dẫn tuyệt đối nếu không muốn nhầm lẫn với kí hiệu trong linux
## Key level 2

`PK8fYLZg2hnHSz83plBL1iEPKd******`