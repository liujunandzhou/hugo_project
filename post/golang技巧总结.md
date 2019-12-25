---
title: "golang 那些年我们一起用过的效率工具"
date: 2019-12-24T15:17:42+08:00
tags: ["golang","编程技巧"]
categories: ["golang","编程技巧"]
author: "铁血执着的青春"
draft: true
---

一.开发环境.
基于devnet的资源云,以容器化的方式,提供了一整套远程开发环境。
集成了idea,clion,goland,pycharm等工具(目前公司已付费)。目前已经有50+团队接入使用。
可以自定持续迭代自己的开发环境,研发效率持续提升。
http://km.oa.com/group/29048/articles/show/382016

二.开发工具.
1)sql2go 用于将sql语句转换为golang的struct.
http://stming.cn/tool/sql2go.html
2)toml2to 用于将编码后的toml文本转换问golang的struct./
https://xuri.me/toml-to-go/
3)curl2go 用来将curl命令转化为具体的golang代码.
https://mholt.github.io/curl-to-go/
4)json2go 用于将json文本转换为struct.
https://mholt.github.io/json-to-go/
5)mysql转ES工具.
http://www.ischoolbar.com/EsParser/
6)golang模拟模板的工具,在支持泛型之前,可以考虑实用。
https://github.com/cheekybits/genny
7)查看某一个库的依赖情况,类似于go list功能.
https://github.com/KyleBanks/depth
8)一个好用的文件压缩和解压工具,集成了zip,tar等多种功能,主要还有跨平台.
https://github.com/mholt/archiver
9)go 内置命令.
go list 可以查看某一个包的依赖关系.
go vet 可以检查代码不符合golang规范的地方.
7)热编译工具.
https://github.com/silenceper/gowatch
8)golang代码质量检测工具 revive.
https://github.com/mgechev/revive
9)golang的代码调用链图工具. Go Callvis
https://github.com/TrueFurby/go-callvis
10)开发流程改进工具 Realize
https://github.com/oxequa/realize
11)自动生成测试用例工具,Gotests.
https://github.com/cweill/gotests
三.调试工具.
1)perf代理工具,支持内存,cpu,堆栈查看,并支持火焰图.
perf工具和go-torch工具,快捷定位程序问题.
https://github.com/uber-archive/go-torch
https://github.com/google/gops
2)dlv远程调试. 
基于goland+dlv可以实现远程调式的能力.
https://github.com/uber-archive/go-torch
3)网络代理工具.
goproxy代理,支持多种协议,支持ssh穿透和kcp协议.
https://github.com/snail007/goproxy
4)抓包工具. 
go-sniffer工具,可扩展的抓包工具,可以开发自定义协议的工具包. 现在只支持了http,mysql,redis,mongodb.
基于这个工具,我们开发了qapp协议的抓包。
https://github.com/40t/go-sniffer
5)反向代理工具,快捷开放内网端口.
ngrok 可以让内网服务外部调用.
https://ngrok.com/
https://github.com/inconshreveable/ngrok
6)高效翻墙代理.
x2ray 自己搭建翻墙工具,从未如此简单.
https://github.com/v2ray/v2ray-core
7)配置化生成证书.
从根证书,到业务侧证书一键生成.
https://github.com/cloudflare/cfssl
8)免费的证书获取工具.
基于acme协议,从letsencrypt生成免费的证书,有效期1年,可自动续期。
https://github.com/Neilpang/acme.sh
9)开发环境管理工具,单机搭建可移植工具的利器。支持多种虚拟机后端。
vagrant常被拿来同docker相比,值得拥有。
https://github.com/hashicorp/vagrant
10)轻量级容器调度工具.
nomad 可以非常方便的管理容器和传统应用,相比k8s来说,简单不要太多.
https://github.com/hashicorp/nomad
11)敏感信息和密钥管理工具.
https://github.com/hashicorp/vault
12)高度可配置化的http转发工具。基于etcd配置.
https://github.com/gojek/weaver
13).进程监控工具 supervisor.
https://www.jianshu.com/p/39b476e808d8
14).基于procFile进程管理工具. 相比supervisor更加简单.
https://github.com/ddollar/foreman
15)基于http,https,websocket的调试代理工具,配置功能丰富。在线教育的nohost web调试工具,基于此开发.
https://github.com/avwo/whistle
15).分布式调度工具.
https://github.com/shunfei/cronsun/blob/master/README_ZH.md
https://github.com/ouqiang/gocron
16)轻量级的容器编排工具,相比k8s搭建和使用非常简单.
https://github.com/hashicorp/nomad
17)自动化运维平台.Gaia.
https://github.com/gaia-pipeline/gaia
18)http压力测试工具
https://github.com/tsenart/vegeta
19)类似于uuid的字典序唯一id
https://github.com/oklog/ulid
20)类似于top的命令行工具,可以看到历史趋势:
https://github.com/cjbassi/gotop
21)覆盖网络虚拟专用网实现.
https://github.com/slackhq/nebula
22)httpbin.org优秀的二进制调试工具.
https://httpbin.org/
23)KONG一个优秀的apigate way程序.
https://konghq.com/careers/#positions
24)好用的goproxy软件,可以实现http代理功能. 支持http,https等功能,通过支持多种handler注册功能,实现高效转发。
https://github.com/elazarl/goproxy
25)跨平台好用的http代理服务。
https://github.com/caddyserver/caddy
26)快速生长证书的工具
https://github.com/square/certstrap

四.网络工具.
|序号|功能分类|命令名|功能描述|
|------|------|-----|-----|
|1|网络状态|netstat|用来查看网络状态的工具.用来查看网络状态的工具.|
|2|网络状态|ping|用来验证机器是否可达和网络延时的工具.|
|3|网络状态|tcping|可以代替ping的功能,当对方服务器禁ping的时候,就缺不了这个工具.|
|4|网络状态|telnet |用来验证某一个端口是否监听.|
|5|网络状态|ss |是可以查看系统中socket的状态的工具,可以替代netstat的部分功能,性能更好。|
|6|网络状态|iftop|流量异常飙高,快速排查出哪个进程的锅的工具.|
|7|网络状态|nmon|查看内存,网络,cpu占用的综合性工具.|
|8|网络状态|route |用于查看和配置机器的路由.|
|9|链路追踪|traceroute|进行路由查看和检测的工具.|
|10|链路状态|mtr  |Linux中有一个非常棒的网络连通性判断工具,它结合了ping,traceroute,nslookup的相关特性|
|11|主机配置|ifconfig|查看和配置机器网卡的功能.|
|12|主机配置|ethtool |用于查询及设置网卡参数的命令|
|13|抓包工具|tcpdump |Linux下功能强大的网络抓包工具.|
|14|发包工具|nc 有瑞士军刀之称的工具,可以作为tcp|udp服务器,或者作为工具,模拟发送tcp,udp包. 作为聊天或者文件传输工具也是没有问题的.|
|15|发包工具|curl |这个就不说了,模拟http请求工具.|
|16|域名解析|dig |实现dns解析的功能.|
|17|域名解析|nslookup|实现dns解析的功能.|
|18|流量控制|trickle |是一款轻量级的用户空间带宽控制管理的工具.|
|19|流量控制|tc|流量控制控制,可以实现后台网络环境的模拟.|
|20|端口扫描|hping3|一款路由追踪和端口探测工具。|
|21|端口扫描|Nmap|主机侦测,端口扫描,类似的工具.|

五.常用网站.
go百科全书:  https://awesome-go.com/
json解析:  https://www.json.cn/
出口IP:  https://ipinfo.io/
redis命令:  http://doc.redisfans.com/
ES命令首页:   https://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html
UrlEncode:  http://tool.chinaz.com/Tools/urlencode.aspx
Base64:  https://tool.oschina.net/encrypt?type=3
Guid:  https://www.guidgen.com/
常用工具:  http://www.ofmonkey.com/
六.golang常用库.
日志
https://github.com/Sirupsen/logrus
https://github.com/uber-go/zap
配置
兼容json,toml,yaml,hcl等格式的日志库.
https://github.com/spf13/viper
存储
mysql  https://github.com/go-xorm/xorm
es   https://github.com/elastic/elasticsearch
redis   https://github.com/gomodule/redigo
mongo  https://github.com/mongodb/mongo-go-driver
kafka   https://github.com/Shopify/sarama
数据结构
https://github.com/emirpasic/gods
命令行
https://github.com/spf13/cobra
框架
https://github.com/grpc/grpc-go
https://github.com/gin-gonic/gin
并发
https://github.com/Jeffail/tunny
https://github.com/benmanns/goworker
现在我们框架在用的,虽然star不多,但是确实好用,当然还可以更好用.
https://github.com/rafaeldias/async
工具
定义了实用的判定类,以及针对结构体的校验逻辑,避免业务侧写复杂的代码.
https://github.com/asaskevich/govalidator
https://github.com/bytedance/go-tagexpr
protobuf文件动态解析的接口,可以实现反射相关的能力.
https://github.com/jhump/protoreflect
表达式引擎工具:
https://github.com/Knetic/govaluate
https://github.com/google/cel-go
字符串处理:
https://github.com/huandu/xstrings
ratelimit工具:
https://github.com/uber-go/ratelimit
https://blog.csdn.net/chenchongg/article/details/85342086
https://github.com/juju/ratelimit
分布式ratelimit库,参考了KONG的实现:
https://github.com/RussellLuo/slidingwindow

golang熔断的库
熔断除了考虑频率限制,还要考虑qps,出错率等其他东西.
https://github.com/afex/hystrix-go
https://github.com/sony/gobreaker
表格:
https://github.com/chenjiandongx/go-echarts
tail工具库:
https://github.com/hpcloud/tail
实用工具:
自动换行库:
https://github.com/muesli/reflow
golang脚本语言:
与golang可以结合的胶水语言比较多:
golang原生:
https://github.com/mattn/anko
https://github.com/d5/tengo
https://awesome-go.com/
golang的lua+php+lisp+python+javascript
https://github.com/alexeyco/binder
https://github.com/sbinet/go-python
https://github.com/deuill/go-php
好用的tengo库
https://github.com/d5/tengo
https://tengolang.com/?s=0c8d5d0d88f2795a7093d7f35ae12c3afa17bea3