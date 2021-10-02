# sshproxy
便捷创建SSH隧道wrapper脚本，对ssh -L命令的上层封装，创建本地socks或http代理隧道

## 使用说明：
请运行`sshproxy --help` 或 `sshproxy -h` 查看命令帮助及参数说明！

```
sshproxy --help
/v/bin/sshproxy

        执行autossh，自动创建SSH动态端口代理隧道.
        默认绑定端口：0.0.0.0:8989.
        参数1目的主机的为必选参数，其余为可选参数.

Usage:
        sshproxy [*hostname] [local proxy port] [kill exists process] [use http proxy or not(mustbe: nohttp)]
Example1:
        sshproxy racknerd true
Example2:
        sshproxy racknerd nohttp
Example3:
        sshproxy racknerd 7171 true
Example4:
        sshproxy racknerd 7171 nohttp
Example5:
        sshproxy racknerd 7171 true nohttp

附加用法:

        1.sshproxy kill  检测并杀死所有的代理进程
        2.sshproxy list  列出当前活动的所有代理
        3.sshproxy test  检测已有代理端口的可用性

```
---
注：默认连接SSH后创建的代理隧道类型为SOCKS类型，如果需要使用HTTP隧道，需要使用goproxy所为辅助工具将SOCKS隧道转为HTTP隧道

[goproxy Github来源](https://github.com/ooclab/goproxy)

## 操作截图
![image](https://user-images.githubusercontent.com/1593944/135702969-1b67760b-b7eb-45cd-80ef-7229b6e67942.png)


![image](https://user-images.githubusercontent.com/1593944/135702935-74bd08ab-cb3e-45d6-8c75-d3f693b14a3b.png)

![image](https://user-images.githubusercontent.com/1593944/135702947-d6649d79-fddd-4a1b-8e0e-7a8dc8b1ad21.png)

![image](https://user-images.githubusercontent.com/1593944/135702960-7ee67e98-0586-4b68-b0e5-510a8906da9a.png)



