上网工具
===

修改 Hosts
---

对于和我一起只选择使用 Google 的用户来说，这是一种**安全**、**可靠**的上网方法。

你可以从下面的地址：https://raw.githubusercontent.com/racaljk/hosts/master/hosts

获得一个可用的 Google IP，而从最近的趋势来看，这个 IP 列表更新得有点频繁。

除此，还应该在境外拥有一个自己的服务器。目前除了我的博客，还有两个额外的服务器是用来上网的。

自建 SSH 隧道
---

> SSH 会自动加密和解密所有 SSH 客户端与服务端之间的网络数据。但是，SSH 还同时提供了一个非常有用的功能，这就是端口转发。它能够将其他 TCP 端口的网络数据通过 SSH 链接来转发，并且自动提供了相应的加密及解密服务。这一过程有时也被叫做“隧道”（tunneling），这是因为 SSH 为其他 TCP 链接提供了一个安全的通道来进行传输而得名。

只需要形如下的命令即可：

```
ssh -N -D 127.0.0.1:3128 xxx@xx.x.xx.xx
```

随后在客户端上设置代理即可。

自建 OpenConnect
---

AnyConnect 为思科推出的便利上网的客户端，目前已有 Windows、Android、iOS、OS X、Ubuntu、WebOS 等操作系统的客户端。AnyConnect主要作用是方便员工在任何设备上安全地办公.

而 OpenConnect 则可以提供一个 AnyConnect 的服务端，那么我们只需要在 APP Store 下载 AnyConnect 即可。

在 Ubuntu 上执行下面的命令即可：

```
apt install ocserv
```

再做一些复杂的配置：https://www.logcg.com/archives/994.html

Ubuntu Server 安装 ShadowSocks
---

直接使用命令安装即可：

```
apt update
apt install shadowsocks
```

然后修改 `/etc/shadowsocks/config.json` 的配置：

```
{
    "server":"hosts",
    "server_port":8848,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"password",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false,
    "workers": 1
}
```

接着修改 `/etc/rc.local` 设为开机启动：

```
/usr/bin/ssserver -c /etc/shadowsocks/config.json
```

然后，让这货在后台运行即可：

```
nohup ssserver -c /etc/shadowsocks/config.json > log &
```
