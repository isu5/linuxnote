1.配置文件权限
将文件 file1.txt 设为所有人皆可读取 :
`
chmod ugo+r file1.txt
`
将文件 file1.txt 设为所有人皆可读取 :
`
chmod a+r file1.txt
`
将文件 file1.txt 与 file2.txt 设为该文件拥有者，与其所属同一个群体者可写入，但其他以外的人则不可写入 :
`
chmod ug+w,o-w file1.txt file2.txt
`
将 ex1.py 设定为只有该文件拥有者可以执行 :
`
chmod u+x ex1.py
`
将目前目录下的所有文件与子目录皆设为任何人可读取 :
`
chmod -R a+r *
`
此外chmod也可以用数字来表示权限如 :
`
chmod 777 file
`
语法为：

`
chmod abc file
`

其中a,b,c各为一个数字，分别表示User、Group、及Other的权限。

r=4，w=2，x=1
若要rwx属性则4+2+1=7；
若要rw-属性则4+2=6；
若要r-x属性则4+1=5。
`
chmod a=rwx file
`
和
`
chmod 777 file
`
效果相同
`
chmod ug=rwx,o=x file
`
和
`
chmod 771 file
`
效果相同