#### go

###### 读取文件

```go
f, err := os.Open(`./tmp_fix_pc_1109.csv`)
if err != nil {
    log.Fatal(err)
}
defer f.Close()
scanner := bufio.NewScanner(f)
for scanner.Scan() {
    fmt.Println(scanner.Text())
}
if err := scanner.Err(); err != nil {
    log.Fatal(err)
}
```