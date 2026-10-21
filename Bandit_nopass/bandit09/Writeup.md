# Write-up

## Đề cho
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
## Solve
```bash
grep --text -E "==+" data.txt
```
## Key
`B0s2khmbT9u0geKuOoVGW3JZKh******`
