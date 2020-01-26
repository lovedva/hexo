---
title: Linux
---
## Linux笔记
### 常用命令
从当前screen切换到主窗口  
按下 Crl+A+D  

screen -R starbound  

chkconfig --list  可以用 service xxxx stop 来停止。 xxx表示相关服务  
sysv-rc-conf  

cp -v A/a1 B/   
chmod -R 755 /home/user  
chown www:www -R /home/wwwroot/test.nocryplay.com/  
chmod -R 777 /home/wwwroot/www.nocryplay.com/  

删除 rm -rf  删除当前目录所有文件 rm -rf $PWD  

进程查看：  
查看： ps -ef | grep 程序名  
关闭：kill -15 进程号（查看时会显示出对应的进程号，15不行换9-强制关闭）  

开机启动：  
sudo nano /etc/rc.local  
python /home/pi/myscript.py &   

### Debian配置无线网络
重启无线网络 ：重启网络  sudo /etc/init.d/networking restart

Buffalo-G-2A30 d3rcsxrf4ka7e
SPWN_N34_370b4b 1d92a7b5d2866

### root登录SSH以及密码设置
设置root密码：sudo passwd root  
今天安装了Ubuntu  Server 14.04   发现配置了root密码后  
竟然不能ssh登陆，但是su root正常！  why？  

原来新版本里面sshd_config里面有了限制  
```
#vim /etc/ssh/sshd_config

# Authentication:
LoginGraceTime 120
#PermitRootLogin without-password    #找到这里，把它注释
PermitRootLogin yes                  #改为yes  然后重启ssh
StrictModes yes
#service ssh restart
```
## 程序相关
### lnmp
LNMP 1.2及更高版本防跨目录功能使用.user.ini，该文件在网站根目录下，可以修改open_basedir的值来设置限制目录的访问。  
.user.ini文件无法直接修改，而且是隐藏文件可能在winscp下可能无法看到，建议使用vim编辑器或nano编辑器进行修改。  
如要修或删除需要先执行：chattr -i /网站目录/.user.ini  
修改完成后再执行：chattr +i /网站目录/.user.ini  
.user.ini不需要重启一般5分钟左右生效。  
如果要更改网站目录必须要按上述方法修改防跨目录的设置，否则肯定报错！！  

#### 伪静态管理
LNMPA或LAMP可以直接使用网站根目录下放.htaccess 来设置伪静态规则(具体规则可以去程序官网网站找google百度)，但是在LNMP下，需要使用Nginx伪静态规则。
伪静态可以随时添加或删除，如果添加完虚拟主机后忘记或没有添加伪静态，可以通过修改配置文件来添加伪静态。
虚拟主机配置文件在：/usr/local/nginx/conf/vhost/域名.conf

伪静态规则文件需要放在/usr/local/nginx/conf/ 下面。
编辑虚拟主机配置文件，可以使用vi、nano或winscp，后2个工具对新手来说简单些。

例如前面我们添加的虚拟主机，打开后前半部分配置会显示如下：
![](assets/1/20180502-90cb14f1.png)  
在root /home/wwwroot/www.vpser.net;  这一行下面添加：  
include wordpress.conf;
上面的wordpress.conf为伪静态文件，如需要其他伪静态文件自己创建个并上传到/usr/local/nginx/conf/ 下面并include 伪静态.conf; 加完保存，执行：/etc/init.d/nginx restart 重启生效，如果报错可能是添加有误或伪静态规则有误。

### pygame模块
https://elinux.org/RPi_Debian_Python3#PyGame_Module  
尽量使用Raspbian完整版，精简版有各种莫名其妙的问题♂

###　VIM键盘图
![](assets/1/20181022-a629b666.png)  
