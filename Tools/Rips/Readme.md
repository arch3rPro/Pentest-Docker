## RIPS代码审计工具

RIPS是一个用 PHP 编写的源代码分析工具，它使用了静态分析技术，能够自动化地挖掘 PHP 源代码潜在的安全漏洞

----

### Pull镜像

```
    docker pull  docker pull vuldocker/rips
```

* Docker Hub链接[https://hub.docker.com/r/vuldocker/rips/](https://hub.docker.com/r/vuldocker/rips/)

### 启动容器

```
    docker run -d -p 8080:80 --name rips  vuldocker/rips

```

*   -d 后台启动 ， -p 指定映射的端口 rips为指定容器名
*   如果需要容器开机自启，可以加上 --restart always 选项


### 访问目标

访问 `http://a.b.c.d:8080/` 访问目标地址

* `a.b.c.d`为docker容器服务器的域名/IP地址

![rips](https://raw.githubusercontent.com/arch3rPro/vuldocker/master/base/rips/PNG/rips.png)

### 文件管理

本容器使用`B374k Webshell` 作为文件管理器

访问 `http://a.b.c.d:8080/manager.php`,输入密码b374k，即可进入

![b374k](https://raw.githubusercontent.com/arch3rPro/vuldocker/master/base/rips/PNG/b374k.png)

### 教程

* Rips详细使用教程请参考[PHP代码审计工具——Rips详细使用教程](https://www.jianshu.com/p/cd1cb66e4d7d)

* B374k Webshell详细使用教程请参考____
