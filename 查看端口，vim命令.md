### 查看一下redis的进程
> ps auxf | grep redis-server 

==启用6380端口==
> src/redis-server --port 6380&


### 查看端口
> netstat -ntlp   //查看当前所有tcp端口·

> netstat -ntulp |grep 80   //查看所有80端口使用情况·

> netstat -an | grep 3306   //查看所有3306端口使用情况·

> netstat -an | grep 6380 //查看redis6380端口使用情况


```
[root@localhost redis]# netstat -an | grep 6380
tcp        0      0 0.0.0.0:6380            0.0.0.0:*               LISTEN     
tcp        0      0 127.0.0.1:59532         127.0.0.1:6380          TIME_WAIT  
tcp        0      0 127.0.0.1:59550         127.0.0.1:6380          ESTABLISHED
tcp        0      0 127.0.0.1:6380          127.0.0.1:59550         ESTABLISHED
tcp        0      0 127.0.0.1:59574         127.0.0.1:6380          ESTABLISHED
tcp        0      0 127.0.0.1:6380          127.0.0.1:59574         ESTABLISHED
tcp        0      0 127.0.0.1:6380          127.0.0.1:59544         ESTABLISHED
tcp        0      0 127.0.0.1:59536         127.0.0.1:6380          ESTABLISHED
tcp        0      0 127.0.0.1:6380          127.0.0.1:59536         ESTABLISHED
tcp        0      0 127.0.0.1:59544         127.0.0.1:6380          ESTABLISH
```

### vim 命令
> i 或者 a 进入插入模式； 按esc 退出 ； 

> 按冒号：输入命令 q!（不保存退出）;  wq! （保存退出）

> 搜索：命令模式下，输入：/字符串
