#### mysql 命令行导出

> 在linux服务器上直接使用 mysqldump -u用户名 -p密码 数据库名 > 服务器地址/数据库名.sql
```
mysqldump -u root -p books > /www/wwwroot/books.sql
```
#### mysql 命令行导入
```
use securityonion_db; 

set names utf8; 

source /路径/db.sql;
```