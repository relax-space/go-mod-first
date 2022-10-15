# multi_mod

## 一个版本库对应一个mod

``` shell
$ cd 4.multi_mod/r1
$ go get -d github.com/relax-space/go-a12@v1.0.1
$ go run main.go
r1 v1.0.1
r2 v1.0.1
```


## 一个版本库对应多个mod


``` shell
$ cd 4.multi_mod/r2
$ go get -d github.com/relax-space/go-a13/m1@v1.0.3
$ go get -d github.com/relax-space/go-a13/m2@v1.0.6
$ go run main.go
m1 v1.0.3
m2 v1.0.6
```