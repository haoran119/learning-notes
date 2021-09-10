# 学习笔记之Docker

* [Docker 官网](http://www.docker.com)
  * Docker is the company driving the container movement and the only container platform provider to address every application across the hybrid cloud. Today’s businesses are under pressure to digitally transform but are constrained by existing applications and infrastructure while rationalizing an increasingly diverse portfolio of clouds, datacenters and application architectures. Docker enables true independence between applications and infrastructure and developers and IT ops to unlock their potential and creates a model for better collaboration and innovation.
  * [Docker Documentation | Docker Documentation](https://docs.docker.com/)
* [Docker_百度百科](https://baike.baidu.com/item/Docker/13344470?fr=aladdin)
  * Docker 是一个开源的应用容器引擎，让开发者可以打包他们的应用以及依赖包到一个可移植的容器中，然后发布到任何流行的 Linux 机器上，也可以实现虚拟化。容器是完全使用沙箱机制，相互之间不会有任何接口。
* [Docker (software) - Wikipedia](https://en.wikipedia.org/wiki/Docker_(software))
  * Docker is a computer program that performs operating-system-level virtualization also known as containerization. It is developed by Docker, Inc. Docker is primarily developed for Linux, where it uses the resource isolation features of the Linux kernel such as cgroups and kernel namespaces, and a union-capable file system such as OverlayFS and others to allow independent "containers" to run within a single Linux instance, avoiding the overhead of starting and maintaining virtual machines (VMs). The Linux kernel's support for namespaces mostly isolates an application's view of the operating environment, including process trees, network, user IDs and mounted file systems, while the kernel's cgroups provide resource limiting for memory and CPU. Since version 0.9, Docker includes the libcontainerlibrary as its own way to directly use virtualization facilities provided by the Linux kernel, in addition to using abstracted virtualization interfaces via libvirt, LXC and systemd-nspawn.
  * A very limited Windows version of Docker is also available.
* [Docker 教程 | 菜鸟教程](http://www.runoob.com/docker/docker-tutorial.html)
  * 容器是完全使用沙箱机制，相互之间不会有任何接口（类似 iPhone 的 app）,更重要的是容器性能开销极低。
  * Docker 使用客户端-服务器 (C/S) 架构模式，使用远程API来管理和创建Docker容器。Docker 容器通过 Docker 镜像来创建。容器与镜像的关系类似于面向对象编程中的对象与类。
  * [Docker 资源汇总 | 菜鸟教程](http://www.runoob.com/docker/docker-resources.html)

## RESOURCES

* [Docker入门教程 - Linux学习](https://mp.weixin.qq.com/s/hjSXVcxZp9jm8huW3cVRhw)
  * https://waylau.com/ahout-docker/
* [把 Docker讲清楚](https://mp.weixin.qq.com/s/MYdA-W6CdteTp5KNrcHp_g)
  * https://blog.csdn.net/wuzhiwei549/article/details/106032491
  * https://mp.weixin.qq.com/s/BrhiUanV7TE-elBGRuyRKg
  * http://jartto.wang/2020/07/04/learn-docker/
* [什么是Docker？干货文章](https://mp.weixin.qq.com/s/Aa9asvZJU7g0Kj0DCzWXjQ)
* [快速把你拉入Docker 的门里 | 原力计划](https://mp.weixin.qq.com/s/CXUwpTbAVoXEeB7EcrCjAw)
  * https://blog.csdn.net/ljk126wy/article/details/104275624
* [上手 Docker 容器，不应该是个问题 (qq.com)](https://mp.weixin.qq.com/s?__biz=Mzg4MjYzMjI1MA==&mid=2247517547&idx=2&sn=c8a3a2a60194314ee3ac29b38ce2a9a1&source=41#wechat_redirect)
* [8 个步骤，学会这个 Docker 命令终极教程](https://mp.weixin.qq.com/s/3VyDhtMLJavUAb-79SkW_Q)
  * https://medium.com/better-programming/the-ultimate-docker-command-list-d98ef300fe6d
* [关于 Docker ，你必须了解的核心](https://mp.weixin.qq.com/s/noaTjDLkdxcWiYmS5mthCw)
  * https://blog.csdn.net/fysuccess/article/details/105653802
* [详解容器技术架构、网络和生态](https://mp.weixin.qq.com/s/3ZKmVmbVusGdRULSwB7CuQ)
* [Docker 搭建你的第一个 Node 项目到服务器](https://mp.weixin.qq.com/s/QLEHt4ZHJZhFc3saZex6Nw)
* [Docker 容器资源管理，你真的学会了吗？](https://mp.weixin.qq.com/s/Xt0_7hUpwTiZYQmvf5agEw)
* [一文搞定 Docker 端口绑定](https://mp.weixin.qq.com/s/WeaWj2s307d8NpoUOHb6kQ)
  * https://medium.com/better-programming/how-does-docker-port-binding-work-b089f23ca4c8
* [Docker-Compose 基础与实战，看这一篇就够了 | 原力计划](https://mp.weixin.qq.com/s/TdKakv5xqnjyxND_chLD8A)
* [开源 Docker 工具分享](https://mp.weixin.qq.com/s/dt7E0KLKcyg3N-4QBGRiYQ)
  * https://dzone.com/articles/5-docker-utilities-you-should-know
* [机器学习开发的灵药—Docker容器](https://mp.weixin.qq.com/s/igFxiuUZ_8i9dGDeF694vA)
