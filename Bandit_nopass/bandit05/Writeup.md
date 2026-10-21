# Write-up

## Đề cho
1 in-here dictionary.

File cần tìm có dạng:

- human-readable
- 1033 bytes in size
- not executable
## Solve
Ban đầu tôi định sử dụng du -ah nhưng nhận ra kiểu dữ liệu nó không chính xác

Vậy nên ta sẽ dùng hàm find chuyên dụng để làm luôn

ta có 1033 bytes in size sẽ là -size 1033c


```bash
find inhere -type f -size 1033c -exec cat {} \;
```
## Lesson
Ta biết thêm được về command find

syntax
`find [path] [options] [expression]`

VD:

- -type f/d là tìm file hoặc dictionary
- user bandit7
- -size 10M hoặc +10M: file dung lượng bằng 10M(c = bytes, K = MB, M = MB, G = GB)
- -executable ||! -executable
- -name "*.txt"
- -readable
## Key

`pXa26xhMWaC2SvDotA4r9EgZku******`
