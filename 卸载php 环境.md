#### 卸载Mysql

> 1 查找以前是否装有mysql
```
命令：rpm -qa|grep -i mysql
```

> 可以看到mysql的包：
```
mysql-3.23.58-9
php-mysql-4.3.4-11
mod_auth_mysql-20030510-4.1
mysql-server-3.23.58-9
```

> 2 删除mysql
```
删除命令：rpm -e --nodeps 包名

rpm -ev mysql-server-3.23.58-9
```

说明：rpm –qa | grep mysql 命令是为了把mysql相关的包都列出来，卸载都从最下面的一个包开始，直到卸载掉第一个为止。执行rpm -q php，如果返回php版本，则是rpm安装；不返回php版本则是二进制安装。

> 3 删除老版本mysql的开发头文件和库
```
rm -fr /usr/lib/mysql

rm -fr /usr/include/mysql
```
注意：卸载后/var/lib/mysql中的数据及/etc/my.cnf不会删除，如果确定没用后就手工删除
```
　　rm -f /etc/my.cnf

　　rm -fr /var/lib/mysql
```

#### 卸载Apache

> 1 查找以前是否装有httpd
```
rpm -qa|grep -i httpd
```
得到以下安装包
```
httpd-manual-2.2.9-4.i386
httpd-tools-2.2.9-4.i386
httpd-devel-2.2.9-4.i386
httpd-2.2.9-4.i386
```
> 2 删除apache
```
　　rpm -e --nodeps httpd-2.2.9-4.i386
　　rpm -e --nodeps httpd-devel-2.2.9-4.i386
　　rpm -e --nodeps httpd-tools-2.2.9-4.i386
　　rpm -e --nodeps httpd-manual-2.2.9-4.i386
```

#### 卸载PHP
```
rpm -qa|grep -i php
```
得到以下包
```
php-odbc-4.3.4-11
php-4.3.4-11
php-mysql-4.3.4-11
php-pear-4.3.4-11
php-ldap-4.3.4-11
php-pgsql-4.3.4-11
```

卸载方法跟上面相同

注意：卸载的时候如果卸载不掉，系统一般会提示包的依赖关系，并且列出依赖的包的名称，先卸载提示依赖的包就可以了。

如果实在实在有卸载不掉的包，可以加—nodeps这个参数来卸载，比如我们卸载php-4.3.4-11，实在卸不掉了。就用：
rpm -e php-4.3.4-11 --nodeps（或 rpm -e --nodeps php-4.3.4-11）
命令很强硬，应该行的。

rpm –e mod_auth_mysql为普通卸载