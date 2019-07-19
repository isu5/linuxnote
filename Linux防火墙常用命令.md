#### (1) 启动/关闭防火墙服务
```
systemctl start firewalld.service
systemctl stop firewalld.service
systemctl restart firewalld.service
```

#### (2) 显示防火墙服务状态
```
systemctl status firewalld.service
```
#### (3) 设置开机启动/禁用防护墙服务
```
systemctl enable firewalld.service
systemctl disable firewalld.service
```
#### (4) 查看防火墙服务是否开机启动
```
systemctl is-enabled firewalld.service;echo $?
```
#### (5) 查看已启动的服务列表
```
systemctl list-unit-files | grep enabled
```
#### (6) 查看防火墙允许的端口号
```
firewall-cmd --zone=public --list-ports
```
#### (7) 允许访问80端
```
sudo firewall-cmd --zone=public --add-port=80/tcp --permanent
sudo firewall-cmd --reload
```
#### (8) 阻止访问80端口
```
sudo firewall-cmd --zone=public --remove-port=80/tcp --permanent
sudo firewall-cmd --reload
```
![avatar](./images/kurumi_test.png)
