---
title: 产品定位
---

![](https://github.com/KoolCore/wiki.ikoolcore.com/blob/main/pic/R1-banner-2023.jpg?raw=true)

### 1⃣️开源家庭路由/防火墙（Open-source Router/Firewall）

随着过去10来年国内互联网的高速发展，黑客攻击和广告追踪，越来越影响我们的日常冲浪体验。借助硬酷R1，用户可安装pfsense、OPNsense、iKuai、OpenWRT等主要防火墙和流控的开源路由系统，轻松实现家庭网络的安全掌控。更有极客玩家安装ROS系统、Panabit（`不支持UEI启动，需借助虚拟机`）等系统。在硬酷R1和各种开源的路由系统的加持下，我们可以轻松实现：

- 家庭网络去广告；
- 自建DNS服务；
- 动态公网解析（`需有动态公网IP`）；
- 搭建私人内网VPN——方便远程管理家庭内网设备
- 搭建BT/PT下载服务器——借助Transmission, Qbtorrent等
- 搭建多媒体娱乐服务器——借助Alist, 阿里云盘WebDAV等

方便我们的日常数码生活，大大完善我们的网络体验。



### 2⃣️虚拟机（Hpervisor）

硬酷R1基于通用x86架构设计，你可以安装运行 VMware ESXi、Proxmox 、XCP-ng、Citrix Hypervisor等虚拟机。前两种是中国大陆消费者较为常用的两种底层虚拟机。{.notice}

对于奋斗在互联网一线的码农和网工群体来说，拥有一台完全属于自己的多网口服务器是一件非常棒的事情，那么借助硬酷R1，这些小伙伴们就可以在家折腾上虚拟机，一种可以基于底层虚拟环境，可以部署多种操作系统且互不干扰的系统。一台物理机可以部署多种操作系统，以解决自己的不同需求，是多么的奈斯的一件事：

- **路由系统：** 用户可以根据自己的喜好，安装任何开源的路由器系统(`OpenWRT, pfsense, OPNSense, iKuai, Panabit, ROS等`)负责家里的网络出口，不同的开源路有系统有其不同的特点，需要用户根据其实际使用需求和喜好进行选择；
  - `OpenWRT`：中国大陆消费者因其可以托管各种私有的跨网协议而备受用户青睐
  - `iKuai爱快`：因其属于中国内地公司开发和拥有，具有强大的流控功能而备受部分用户喜爱
  - `pfsense/OPNSense`：国际上使用较为广泛的由Netgate开源的路由系统。OPNSense为从pfsense分出去的不同分支。
- **Linux系统：** 建议根据用户自己熟悉的系统进行选择。
  - [Debian](https://www.debian.org/distrib/): 推荐使用这个 **[镜像](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/current/amd64/iso-dvd/)** 文件，可长期作为内网服务器运行docker，宝塔，青龙🐉等服务。
  - [Ubuntu](https://ubuntu.com/): 最多入门用户选择的Linux系统。
  - [CentOS](https://www.centos.org/)：Community Enterprise Operating System）是Linux发行版之一，它是来自于Red Hat Enterprise Linux（RHEL）依照开放原始码规定释出的原始码所编译而成。
  - 其他Linux分支：Fedora, PopOS, Manjora, Kali, openSUSE等。

基于我个人喜好，推荐使用 **[Debian最新版本系统](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/current/amd64/iso-dvd/)**。{.notice}

- **Windows系统：** 可以作为一台内网下载服务器，接受7 x 24 小时日常挂各种云盘和迅雷种子下载，低功耗而无需为电费担心。如果有动态公网IP，还可以配合DDNS加端口号实现在公司即可远程使用微软远程桌面程序连接位于家里的这台电脑，抛弃各种商业的远程操控软件。

### 3⃣️远程办公（Remote Office）

前提：有公网IP，且拥有一个可用于解析DDNS服务的域名。{.notice}

在疫情期间，远程办公逐渐兴起。借助DDNS+端口转发，可以实现人在异地，远程通过Microsoft Remote Desktop工具登陆办公电脑，实现远程操控，体验比免费的商业试用远控系统更流畅，响应更丝滑。

### 4⃣️Docker宿主机：(基于虚拟机之上玩各种套娃Docker服务)

可以物理直装Linux系统，并安装docker服务，借助docker实现各种各样的微服务。也可以基于虚拟机之下的Linux系统上安装docker跑各种个性化需求的微服务。

  - `Portainer`——Docker图形化管理工具

  - `Alist` —— 超好用的在线网盘挂载工具

  - `LibreSpeed`——内外网测速工具

  - `OpenSpeedTest`——高颜值内外网测速工具

  - `Squoosh`——GoogleChromeLab团队出品的开源图片压缩工具

  - `PhotoPrism `—— 优秀的相册管理工具

  - `TrwebOCR`——OCR在线识别工具

具体以默认系统部分信息为准。{.notice}

### 5⃣️下载机

可以直装Windows当各种云网盘的下载机，也可以借助docker安装各种pt下载工具（transmission/qbittorrent等），轻松玩转PT/BT。同时也可以基于PVE/ESXi/Unraid等虚拟机下安装开源NAS系统，通过直通USB硬盘设备作为存储盘 。

可行，但不推荐。R1产品定位没有为NAS场景考虑。{.notice}

### 6⃣️家庭多媒体服务器

借助诸如`jellyfin`, `Plex`, `alist`等docker工具，轻松扮演家庭内网的媒体服务器。如果你家里有Apple TV，配合Infuse即可享受各种云盘内的高清数字资源。

下单购买 **硬酷R1** 的小伙伴，可加微信`iKOOLCORE` 主动提供`订单编号`，邀请进入专属售后群，老司机带你玩转家庭多媒体服务器。{.notice}


![](https://github.com/KoolCore/wiki.ikoolcore.com/blob/main/pic/banner_01.jpg?raw=true)