```json
{
  "date": "2021.02.02 20:40",
  "tags": ["Docker&K8s"],
  "musicId":"475254758",
  "description":"Docker打包Go项目,在docker中启动"  
}
```
# Docker概述
Docker 是一个开源项目，诞生于 2013 年初，最初是 dotCloud 公司内部的一个业余项目。它基于 Google 公司推出的 Go 语言实现。 项目后来加入了 Linux 基金会，遵从了 Apache 2.0 协议，项目代码在 GitHub 上进行维护。

Docker 自开源后受到广泛的关注和讨论，以至于 dotCloud 公司后来都改名为 Docker Inc。Redhat 已经在其 RHEL6.5 中集中支持 Docker；Google 也在其 PaaS 产品中广泛应用。

Docker 项目的目标是实现轻量级的操作系统虚拟化解决方案。 Docker 的基础是 Linux 容器（LXC）等技术。

在 LXC 的基础上 Docker 进行了进一步的封装，让用户不需要去关心容器的管理，使得操作更为简便。用户操作 Docker 的容器就像操作一个快速轻量级的虚拟机一样简单。

### 在任何地方开发、部署和运行任何应用
* Docker是一款针对程序开发人员和系统管理员来开发、部署、运行应用的一款虚拟化平台。
* Docker 可以让你像使用集装箱一样快速的组合成应用，并且可以像运输标准集装箱一样，尽可能的屏蔽代码层面的差异。Docker 会尽可能的缩短从代码测试到产品部署的时间。

### Docker 组件

* The Docker Engine – Docker Engine 是一个基于虚拟化技术的轻量级并且功能强大的开源容器引擎管理工具。它可以将不同的 work flow 组合起来构建成你的应用。
* Docker Hub 可以分享和管理你的images镜像的一个 Saas 服务。
### 快速交付应用程序
* 我们希望你的开发环境能够更好的提高你的工作效率。Docker容器能够帮助开发人员、系统管理员、QA和版本控制工程师在一个生产环节中一起协同工作。我们制定了一套容器标准，而这套容器标准能够使系统管理员更改容器的时候，程序员不需要关心容器的变化，而更专注自己的应用程序代码。从而隔离开了开发和管理，简化了开发和部署的成本。
* 我们使应用的构建方式更加简单，可以快速的迭代你的应用，并且可以可视化的来查看应用的细微更改。这能够帮助组织里边的成员来更好的理解一个应用从构建到运行的过程。
* Docker 是一个轻量级的容器，所以它的速度是非常快的，而容器的启动时间只需要一秒钟，从而大大的减少了开发、测试和部署的时间。轻松部署和扩展
* Docker 容器可以运行在大多数的环境中，你可以在桌面环境、物理主机、虚拟主机再到数据中，私有或者公有云中部署。
* 因为 Docker 可以从多平台下运行。你可以很容器的迁移你的应用程序。如果需要，你可以非常简单的将应用程序从测试环境迁移到云，或者从云迁移到测试环境。
* Docker 是一个轻量级的容器，因此它可以在很短的时间内启动和关闭。当你需要的时候，你可以启动多个容器引擎，并且在不需要使用他们的时候，可以将他们全部关闭。

Docker的容器本身不需要额外创建虚拟机管理系统，因此你可以启动多套Docker容器，这样就可以充分发挥主机服务器的物理资源，也可以降低因为采购服务器licenses而带来的额外成本。

### 快速构建 轻松管理
* 因为Docker上述轻便，快速的特性。可以使您的应用达到快速迭代的目的。每次小的变更，马上就可以看到效果。而不用将若干个小变更积攒到一定程度再变更。每次变更一小部分其实是一种非常安全的方式。

# Docker 安装
## Windows 安装
首先到官网上下载对应版本的Docker Hub [windowns官网地址](https://docs.docker.com/docker-for-windows/install/) 下载安装完成之后登录Docker ID, 按住Win + R 然后输入"cmd", 进入命令管理界面之后, 运行```docker version```.版本号显示正确说明Docker安装成功
## Mac 安装
Mac有两种安装方式一种是到官网上下载官方的Docker包, [Mac 官网地址](https://docs.docker.com/docker-for-mac/install/) 下载完成之后解压，并拖入到Applications 中。打开之后会在右上角显示Docker图标如下所示
![](../../../images/Mac-docker.png)
然后点击登录,输入你的Docker ID 和密码，如果没有可以新建一个，如下图所示
![](../../../images/Mac-docker-login.png)
从上图也可以看出Docker is running，打开终端，输入```docker version```可以看出Docker版本
![](../../../images/docker-version.png)
输出成功说明Docker安装成功。

<font color=red>安装错误解决方法</font>

如果遇到没有```hyperkit```,需要自己做个软连接，在```/Applications/Docker.app/Contents/Resources/bin/com.docker.hyperkit``` 软连接到```/usr/local/bin/hyperkit```

如果遇到没有```vpnkit```,需要自己做个软连接，在```Applications/Docker.app/Contents/Resources/bin/com.docker.vpnkit``` 软连接到```/usr/local/bin/vpnkit```

## Linux 安装
请到网上自行百度，Linux上安装教程还是比较多的

# Docker 打包Go项目镜像

