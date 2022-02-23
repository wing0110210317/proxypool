<h1 align="center">
  <br>Proxypool<br>
</h1>

<h5 align="center">自动抓取tg频道、订阅地址、公开互联网上的ss、ssr、vmess、trojan节点信息，聚合去重测试可用性后提供节点列表</h5>
<h5 align="center">目前最新稳定版： v0.6.1 Gravy</h5>
<h5 align="center">目前最新开发版： v0.6.2 Gravy</h5>
<p align="center">

  <a href="https://goreportcard.com/report/github.com/daycat/proxypool">
    <img src="https://goreportcard.com/badge/github.com/daycat/proxypool?style=flat-square">
  </a>

</p>

## 支持

- 支持ss、ssr、vmess、trojan多种类型
- Telegram频道抓取
- 订阅地址抓取解析
- 公开互联网页面模糊抓取
- 定时抓取自动更新
- 通过配置文件设置抓取源
- 自动检测节点可用性
- 提供clash、surge配置文件
- 提供ss、ssr、vmess、sip002订阅

## 安装

以下五选一。
### Debian | Ubuntu:
```sh
bash <(curl -Ls https://raw.githubusercontent.com/wing0110210317/proxypool/master/onekey_install_deb.sh)
```

### CentOS 7.* | RHeL 7.* :
```sh
wget https://raw.githubusercontent.com/lanhebe/proxypool/master/onekey_install.sh && chmod +x onekey_install.sh && ./onekey_install.sh
```

### 从源码编译 （不推荐，有些arch上有bug）

需要安装Golang 

```sh
$ go get -u -v github.com/daycat/proxypool
```

运行
```shell script
$ go run main.go -c ./config/config.yaml
```

编译
```
make
```

### 下载预编译程序

从这里下载预编译好的程序 [release](https://github.com/daycat/proxypool/releases)。

## 使用

运行该程序需要具有访问完整互联网的能力。

### 启动程序

#### Debian | Ubuntu:

```shell
systemctl start proxypool
```

#### CentOS | RHeL: 

使用 `-c` 参数指定配置文件路径，支持http链接

```shell
proxypool -c ./config/config.yaml
```

## Clash配置文件

远程部署时Clash配置文件访问：https://domain/clash/config

本地运行时Clash配置文件访问：http://127.0.0.1:[端口]/clash/localconfig

## 本地检查节点可用性

此项非必须。为了提高实际可用性，可选择增加一个本地服务器，检测远程proxypool节点在本地的可用性并提供配置，见[proxypoolCheck](https://github.com/Sansui233/proxypoolCheck)。

## 截图

![Speedtest](docs/speedtest.png)

![Fast](docs/fast.png)

## 声明

本项目遵循 GNU General Public License v3.0 开源，在此基础上，所有使用本项目提供服务者都必须在网站首页保留指向本项目的链接

本项目仅限个人自己使用，禁止使用本项目进行营利和做其他违法事情，产生的一切后果本项目概不负责
