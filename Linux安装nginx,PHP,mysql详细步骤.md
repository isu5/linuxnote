### nginx安装

 https://blog.csdn.net/t8116189520/article/details/81909574

> 1.安装依赖包
```
//一键安装上面四个依赖
yum -y install gcc zlib zlib-devel pcre-devel openssl openssl-devel
```
> 2.下载并解压安装包
```
//创建一个文件夹
cd /usr/local
mkdir nginx
cd nginx
//下载tar包 http://nginx.org/download/ 可以根据自己需要选择版本
wget http://nginx.org/download/nginx-1.15.12.tar.gz
//解压
tar -xvf nginx-1.15.12.tar.gz
```
> 3.安装nginx
```
//进入nginx目录
cd /usr/local/nginx/nginx解压目录
//执行命令
./configure
//执行make命令 可以直接执行 make && make install
make
//执行make install命令
make install
```
> 4.配置nginx.conf
```
# 打开配置文件
vi /usr/local/nginx/conf/nginx.conf

```

1.将端口号改成8090(端口自定义)，因为可能apeache占用80端口，apeache端口尽量不要修改，我们选择修改nginx端口。

2.localhost修改为你服务器ip地址。

![avatar](https://images2015.cnblogs.com/blog/1095329/201703/1095329-20170328193900029-2024017752.png)

> 5.启动nginx
```
/usr/local/nginx/sbin/nginx -s reload
```

- > 无法启动报错:  nginx: [error] open() "/usr/local/nginx/logs/nginx.pid" failed (2: No such file or directory)
- > 解决方法: 
```
/usr/local/nginx/sbin/nginx -c /usr/local/nginx/conf/nginx.conf
```
使用nginx -c的参数指定nginx.conf文件的位置
```
[root@localhost nginx]# cd logs/
[root@localhost logs]# ll
总用量 12
-rw-r--r-- 1 root root 1246 12月 9 18:10 access.log
-rw-r--r-- 1 root root 516 12月 10 15:39 error.log
-rw-r--r-- 1 root root 5 12月 10 15:38 nginx.pid
```
看nginx.pid文件已经有了。


查看nginx进程是否启动：
```
ps -ef | grep nginx
```

> (本地机)6.若想使用外部主机连接上虚拟机访问端口192.168.131.2，需要关闭虚拟机的防火墙：

centOS6及以前版本使用命令： systemctl stop iptables.service

centOS7关闭防火墙命令： systemctl stop firewalld.service

随后访问该ip即可看到nginx界面。



























