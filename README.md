# go-mod-first

## 正常流程
1. 第一次下载依赖
```
1. go mod init xxx
2. go get -d github.com/xxx
3. go run main.go
```

2. 提交代码之前
```
1. go mod tidy
```

3. 更新依赖
```
1. go get -u 或者 go get -u=patch
```

4. 替换依赖版本
```
1. go mod edit -replace github.com/xxx@old=github.com/xxx@new
```