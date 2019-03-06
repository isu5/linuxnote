#### 安装redis

> 官网下载: https://redis.io/download 下边有提供方法

```
$ cd /usr/local/ 下
$ wget http://download.redis.io/releases/redis-5.0.3.tar.gz
$ tar xzf redis-5.0.3.tar.gz
$ cd redis-5.0.3     (可改为redis,版本号去掉,也可执行下一步指定目录)
$ make && make PREFIX=/usr/local/redis install  #安装到指定目录

安装完成后,路径(/usr/local/redis/src/redis-server 服务)
 小试一把,  直接redis-server 报错无法启动的话,就返回上层目录
 src/redis-server 启动  
 然后另开窗口测试:
 src/redis-cli  
127.0.0.1:6379> set foo bar
OK
127.0.0.1:6379> get foo
"bar"

(error) NOAUTH Authentication required:
需要密码

//设置密码
在nginx.conf中查找 requirepass xxx(为密码)

在进入redis时 需要密码输入 auth 密码 进入
```

#### 配置redis自启动 
```
 src/redis-server  nginx.conf  //重启

```


https://blog.csdn.net/xujialei0704/article/details/80362602




