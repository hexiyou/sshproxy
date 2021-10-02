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
