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
