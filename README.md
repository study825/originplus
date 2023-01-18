originplus 游戏服务器引擎简介
==================


originplus 是一个由 Go 语言（golang）编写的分布式开源游戏服务器引擎。originplus适用于各类游戏服务器的开发，包括 H5（HTML5）游戏服务器。该框架是基于duanhf2012/origin框架基础上开发，在之上，增加许多功能且优化了代码逻辑，更适合云原生时代使用。

originplus 解决的问题：
* originplus总体设计如go语言设计一样，总是尽可能的提供简洁和易用的模式，快速开发。
* 能够根据业务需求快速并灵活的制定服务器架构。
* 利用多核优势，将不同的service配置到不同的node，并能高效的协同工作。
* 将整个引擎抽象三大对象，node,service,module。通过统一的组合模型管理游戏中各功能模块的关系。
* 有丰富并健壮的工具库。
* 配置etcd注册中心

Hello world!
---------------
下面我们来一步步的建立originplus服务器,先下载[originplus引擎](https://github.com/study825/originplus "originplus引擎"),或者使用如下命令：
```go
go get -v -u  github.com/study825/originplus
```
于是下载到GOPATH环境目录中,在src中加入main.go,内容如下：
```go
package main

import (
	"github.com/study825/originplus/node"
)

func main() {
	node.Start()
}
```