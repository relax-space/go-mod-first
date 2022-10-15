# repository

依赖`mod`,以及更新版本

关键词: `edit`, `download`, `tidy`, `go get`


## v1
1. init: 初始化mod
``` shell
$ cd repo1
$ go mod init go-mod-first/2.repository/repo1
```
2. 下载依赖
``` shell
$ go get -d github.com/relax-space/go-a8@v1.0.0

```
等价于
``` shell
# 增加或者修改go.mod文件
$ go mod edit -require github.com/relax-space/go-a8@v1.0.0
# 下载代码
$ go mod download github.com/relax-space/go-a8@v1.0.0
# 新增或修改go.sum文件
$ go mod tidy

```

## v2
1. init: 新增go.mod文件
``` shell
$ cd repo2
$ go mod init go-mod-first/2.repository/repo2
```
2. 下载依赖


``` shell
$ go get -d github.com/relax-space/go-a8/v2@v2.0.0

```
等价于
``` shell
# 增加或者修改go.mod文件
$ go mod edit -require github.com/relax-space/go-a8/v2@v2.0.0
# 下载代码
$ go mod download github.com/relax-space/go-a8/v2@v2.0.0
# 新增或修改go.sum文件
$ go mod tidy

```



## go get
1. x.y.z: x代表主要版本, y代表次要版本, z代表修订版本
2. 升级为修订版本 `go get -u=patch`
``` shell
$ go get -u=patch
go: downloading github.com/relax-space/go-a8 v1.0.1
go: upgraded github.com/relax-space/go-a8 v1.0.0 => v1.0.1
```
3. 升级为次要版本 `go get -u`
``` shell
$ go get -u
go: downloading github.com/relax-space/go-a8 v1.1.1
go: upgraded github.com/relax-space/go-a8 v1.0.1 => v1.1.1
```

4. 升级主要版本
- 路径后面添加版本号,例如 xxx/v2, 引用的时候也需要加上v2
```go
$ go mod edit -require github.com/relax-space/go-a8/v2@v2.0.0
$ go mod download github.com/relax-space/go-a8/v2@v2.0.0
$ go mod tidy
```

### go-a8的所有版本信息
```
v1.0.0
v1.0.1
v1.1.0
v1.1.1
v2.0.0
v2.0.1
v2.0.2
```