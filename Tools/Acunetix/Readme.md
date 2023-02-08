### 工具介绍

Acunetix Web Vulnerability Scanner（简称AWVS）是一个自动化的web漏洞扫描工具，它可以扫描任何通过web浏览器访问和遵循HTTP/HTTPS规则的web站点。

AWVS原理是基于漏洞匹配方法，通过网络爬虫测试你的网站安全，检测流行安全漏洞。

AWVS可以通过SQL注入、XSS、目录遍历、代码执行等漏洞来审核web应用程序的安全性并输出扫描报告。相对于手动测试的复杂和耗时，它能快速的发现漏洞来提高效率和漏洞覆盖面。

### AWVS功能介绍

- WebScanner ：核心功能，web安全漏洞扫描 (深度，宽度 ，限制20个)
- Site Crawler：站点爬行，遍历站点目录结构
- Target Finder ：主机发现，找出给定网段中开启了80和443端口的主机
- Subdomian Scanner ：子域名扫描器，利用DNS查询
- Blind SQL Injector ：盲注工具
- Http Editor http：协议数据包编辑器
- HTTP Sniffer ： HTTP协议嗅探器 （fiddler，wireshark,bp）
- HTTP Fuzzer： 模糊测试工具 (bp)
- Authentication Tester ：Web认证破解工具

### 使用介绍

- 平台地址：https://your-host:3443
- 账号：`admin@acu.com`
- 密码：`Passw0rd!`

### 平台截图

软件界面:

[![awvs 15.2 docker版本 | acunetix cracked](https://www.ddosi.org/wp-content/uploads/2022/12/20103958.webp)](https://www.ddosi.org/wp-content/uploads/2022/12/20103958.webp)

[![awvs 15.2 docker版本 | acunetix cracked](https://www.ddosi.org/wp-content/uploads/2022/12/20104039.webp)](https://www.ddosi.org/wp-content/uploads/2022/12/20104039.webp)

扫描测试:

[![awvs 15.2 docker版本 | acunetix cracked](https://www.ddosi.org/wp-content/uploads/2022/12/20104545.webp)](https://www.ddosi.org/wp-content/uploads/2022/12/20104545.webp)

###  工具来源

[https://www.ddosi.org/awvs-15-2-docker/](https://www.ddosi.org/awvs-15-2-docker/)