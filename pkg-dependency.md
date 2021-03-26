# 下载项目依赖包

* 在当前项目执行`go get -d -u ./...`，可以下载所有关联当前项目的包。默认下载到$GOPATH/src下面，如果没有配置GOPATH则默认到`～/go/src`,附加`-v`可以在下载的同时查看具体的包列表。
* 在当前项目执行`go get -d golang.org/x/text@v0.3.2`,可以升/降级某个依赖包
注意：`go get`命令会检查当前文件夹或父目录下的go.mod,并更新在go.mod里的模块依赖。然后构建并安装命令行列出的包。

* 在当前项目执行`go mod download`会读取go.mod的内容，下载所有相关包并保存到module cache即$GOPATH/pkg/mod文件夹下。
* 下载指定版本：`go mod download golang.org/x/mod@v0.2.0` 
