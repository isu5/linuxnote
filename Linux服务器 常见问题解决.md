### 问题1：Xshell 客户端无法连接Linux服务器 

报错描述

Connection established.
To escape to local shell, press 'Ctrl+Alt+]'.
Connection closing...Socket close.Connection closed by foreign host.
Disconnected from remote host(本地CentOS6.8) at 10:38:08. 

#### 解决方案：
[Xshell 客户端无法连接Linux服务器](https://blog.csdn.net/qq_21405949/article/details/52539686/)

### 问题2：su 无法切换到其他用户 

su: cannot set groups: Operation not permitted 

#### 解决方案：
 
chmod a+s /bin/su 

查看 ll /bin/su






 
