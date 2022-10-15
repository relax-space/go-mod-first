# replace

如果c引用b, b引用a@v1.0.0, 如果c希望b使用a@v1.0.1,那么可以通过`replace`实现

## 开始
``` shell

# 1.正常依赖
$ cd 3.replace
$ go mod init go-mod-first
$ go get -d github.com/relax-space/go-b10@v1.0.0
$ go run main.go
hello a10 v1.0.0

# 2.替换依赖
# 表示当引入 v1.0.0 时其实找到的是 v1.0.1
$ go mod edit -replace github.com/relax-space/go-a10@v1.0.0=github.com/relax-space/go-a10@v1.0.1
$ go mod tidy
$ go run main.go
hello a10 v1.0.1

# 3.删除替换, 又变回到原来的样子
$ go mod edit -dropreplace github.com/relax-space/go-a10@v1.0.0
$ go mod tidy
$ go run main.go
hello a10 v1.0.0

```