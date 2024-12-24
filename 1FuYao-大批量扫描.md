---
title: FuYao-大批量自动扫描漏洞
date: 2024-4-4 16:14:46
tags:
- 渗透工具推荐
categories:
- 工具推荐
---



# FuYao - Go 扶摇直上九万里 - 不再开源 维护中...

https://github.com/ExpLangcn/FuYao-Go

#### 😄 I’m ExpLang [**Twitter**](https://twitter.com/ExpLang_Cn) 欢迎关注fo～



## [问题反馈](https://github.com/ExpLangcn/FuYao-Go/issues)|[漏洞列表](https://github.com/ExpLangcn/FuYao-Go/blob/main/README.md#漏洞列表)



**自动化进行目标资产探测和安全漏洞扫描｜适用于赏金活动、SRC活动、大规模使用、大范围使用|通过使用被动在线资源来发现网站的有效子域｜使用零误报的定制模板向目标发送请求，同时可以对大量主机进行快速扫描。｜提供TCP、DNS、HTTP、FILE等各类协议的扫描，通过强大且灵活的模板，模拟各种安全检查**

[![image](https://user-images.githubusercontent.com/52586866/168596909-c0f95cff-1460-4af7-8d4a-7e5afde3f30e.png)](https://user-images.githubusercontent.com/52586866/168596909-c0f95cff-1460-4af7-8d4a-7e5afde3f30e.png)

[![image](https://user-images.githubusercontent.com/52586866/168596925-b2a50a21-df0a-433d-8424-cd2d5386b5be.png)](https://user-images.githubusercontent.com/52586866/168596925-b2a50a21-df0a-433d-8424-cd2d5386b5be.png)

## 法律免责声明



本工具仅面向合法授权的企业安全建设行为，如您需要测试本工具的可用性，请自行搭建靶机环境。 在使用本工具进行检测时，您应确保该行为符合当地的法律法规，并且已经取得了足够的授权。请勿对非授权目标进行扫描。 如果发现上述禁止行为，我们将保留追究您法律责任的权利。

如您在使用本工具的过程中存在任何非法行为，您需自行承担相应后果，我们将不承担任何法律及连带责任. 您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。

------

### 更新记录



**2022.6.6 14.59**

- 新增Hunter网络测绘扫描
- 新增 `-p` 参数 可以指定漏洞文件夹（采用xray漏洞模版,如果直接拿过来，语言name改为id ,Details改为 info,不支持cache ）

**2022.5.16 20:45**

- 发布V1.3.2版本
- 修复个别情况无法进行Shodan扫描
- 新增Quake资产获取
- 优化存活验证逻辑
- 新增端口探测（探测完子域名后会进行存活探测，存活探测的同时会进行端口探测）
- 优化输出信息
- 新增新版本检查（在启动LOGO上可以看到最新版本）

**2022.5.11 12:10**

- 发布V1.3版本
- 子域名探测效率提升
- 新增自动FoFa资产探测
- 新增自动Shodan资产探测
- 更换漏洞库和验证库 - [Afrog](https://github.com/ExpLangcn/FuYao-Go)
- 新增指纹探测识别

**2022.4.15 17:10**

- 发布V1.1版本
- 修复Windows下 file missing [file=MANIFEST-000000] 错误
- 修复Windows下 no valid templates were found 报错
- 优化扫描并发配置

**2022.4.15 12:00**

- 发布 v1.0版本

------

### 当前功能 or 未来功能



-  子域名枚举资产收集
-  批量子域名枚举资产收集
-  Chaos 资产收集
-  资产存活验证
-  批量资产存活验证
-  安全漏洞验证
-  批量安全漏洞验证
-  子域名枚举资产收集、资产存活验证、安全漏洞扫描联动
-  FoFa自动资产探测
-  Shodan自动资产探测
-  Web指纹探测识别
-  网络空间测绘资产收集
-  中间件漏洞利用例：shiro、SpringBoot等...
-  Hunter自动资产探测
-  子域名存活WebHook通知
-  安全漏洞扫描结果WebHook通知
-  待定...

**有需要什么功能的话可以在 [issues](https://github.com/ExpLangcn/FuYao-Go/issues) 提**

------

### 当前POC列表



#### [点击查看详情](https://github.com/ExpLangcn/FuYao-Go/blob/main/README.md#漏洞列表)



当前总共有：**549个POC模版**

[![image](https://user-images.githubusercontent.com/52586866/167674307-3a3e39f9-3a76-4132-ba23-7bff624307e3.png)](https://user-images.githubusercontent.com/52586866/167674307-3a3e39f9-3a76-4132-ba23-7bff624307e3.png)

------

### 使用帮助



#### 不推荐使用Windows系统！



```
./mark/FuYao_Intel/FuYao_Intel -h                                                                                                                                                                          FuYao_test
  ███████╗██╗   ██╗██╗   ██╗ █████╗  ██████╗
  ██╔════╝██║   ██║╚██╗ ██╔╝██╔══██╗██╔═══██╗
  █████╗  ██║   ██║ ╚████╔╝ ███████║██║   ██║
  ██╔══╝  ██║   ██║  ╚██╔╝  ██╔══██║██║   ██║  Version: V1.3
  ██║     ╚██████╔╝   ██║   ██║  ██║╚██████╔╝  Author: ExpLang
  ╚═╝      ╚═════╝    ╚═╝   ╚═╝  ╚═╝ ╚═════╝   Discord: ExpLang#6666
     Github:github.com/ExpLangcn/FuYao-Go
 使用FuYao前请遵守当地法律,FuYao仅提供给教育行为使用

 法律免责声明
  本工具仅面向合法授权的企业安全建设行为，如您需要测试本工具的可用性，请自行搭建靶机环境。
  在使用本工具进行检测时，您应确保该行为符合当地的法律法规，并且已经取得了足够的授权。请勿对非授权目标进行扫描。
  如果发现上述禁止行为，我们将保留追究您法律责任的权利。

  如您在使用本工具的过程中存在任何非法行为，您需自行承担相应后果，我们将不承担任何法律及连带责任.
  您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。

Usage of ./mark/FuYao_Intel/FuYao_Intel:
  -f string
        指定根域目标文件 ｜ 支持绝对路径和相对路径
```



**自动化信息搜集+漏洞扫描**(目标文件内的目标是一行一个，并且必须是主域名)

> ./FuYao -f list.txt

------

### 配置信息



```
FoFa:
  email: ""
  key: ""
Shodan:
  key: ""
```