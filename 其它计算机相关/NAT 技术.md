NAT 是 Network Address Translation 网络地址转换的缩写。 NAT 是将私有 IP 地址通过边界路由转换成外网 IP 地址，在边界路由的 NAT 地址转换表记录下这个转换映射记录，
当外部数据返回时，路由使用 NAT 技术查询 NAT 转换表，再将目标地址替换成内网用户 IP 地址。 

三种 NAT 技术：

1. 静态 NAT：静态 NAT 就是一对一映射，内部有多少私有地址需要和外部通信，就要配置多少外网 IP 地址与其对应。
2. 动态 NAT：动态 NAT 是在路由器上配置一个外网 IP 地址池，当内部有计算机需要和外部通信时，就从地址池里动态的取出一个外网IP，并将他们的对应关系绑定到 NAT 表中，通信结束后，这个外网 IP 才被释放，可供其他内部 IP 地址转换使用，这个 DHCP 租约 IP 有相似之处。
3. PAT（Port Address Translation，端口地址转换，也叫端口地址复用）：这是最常用的 NAT 技术，也是 IPv4 能够维持到今天的最重要的原因之一，它提供了一种多对一的方式，对多个内网 IP 地址，边界路由可以给他们分配一个外网 IP，利用这个外网 IP 的不同端口和外部进行通信。

参考：<https://www.zhihu.com/question/31332694/answer/145043395>
