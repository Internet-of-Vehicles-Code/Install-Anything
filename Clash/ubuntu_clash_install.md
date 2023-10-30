# Ubuntu clash配置

## 1.下载安装包
执行 cd && mkdir clash 在用户目录下创建 clash 文件夹。

下载 Clash v1.8.0 或更早的版本 二进制文件并解压重命名为 clash

一般个人的64位电脑下载 clash-linux-amd64.tar.gz 即可。

[clash Releases](https://github.com/Dreamacro/clash/releases)
![Alt text](./images/image00.png)
![Alt text](./images/image-01.png)
![Alt text](./images/image-02.png)

## 2.初始化配置
在终端 cd 到 Clash 二进制文件所在的目录，执行 wget -O config.yaml 'https://www.mzkxzsubs.us/link/gv7GIwJRKmRgfC2G?clash=1&log-level=info' 下载 Clash 配置文件

![Alt text](./images/image-03.png)

这里有问题，这里需要换成你自己的clash订阅链接（链接放在单引号中，注意后面有```&log-level=info```）。重新配置一遍。

![Alt text](./images/image.png)

## 3.加载配置
执行```./clash -d . ```即可启动 Clash，同时启动 HTTP 代理和 Socks5 代理。

如提示权限不足，请执行 chmod +x clash

![Alt text](./images/image-1.png)

## 4.端口访问

访问 [Clash Dashboard](https://clash.razord.top/#/proxies) 可以进行切换节点、测延迟等操作。

![Alt text](./images/image-2.png)

选择一个节点

![Alt text](./images/image-4.png)

## 5.启动代理
以 Ubuntu 18.04 为例，打开系统设置，选择网络，点击网络代理右边的 ⚙ 按钮，选择手动，填写 HTTP 和 HTTPS 代理为 127.0.0.1:7890，填写 Socks 主机为 127.0.0.1:7891，即可启用系统代理。

![Alt text](./images/image-5.png)

开启科学上网...

![Alt text](./images/image-6.png)

如果关掉了终端，下次启动记得进入clash然后再终端输入```./clash -d . ```

github clone的速度似乎并不快... 不知道是不是因为本身网络的原因

