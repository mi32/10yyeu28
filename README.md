# 10yyeu28
## 路由表：
目标网络ID：目标IP所在网络的ID  
接口：本设备要发送数据包到目标，从哪个接口发送出来，才能到达
网关：到达目标网络需要将数据交给下一个路口那个接口的对应的IP  
  
IP地址&ensp;&ensp;称为逻辑地址&ensp;&ensp;MAC地址&ensp;&ensp;称为物理地址  
MAC&ensp;&ensp;48位&ensp;&ensp;前24是商家固定&ensp;&ensp;&ensp;后24是分配  
网络ID是&ensp;&ensp;&ensp;IP地址&ensp;&ensp;与&ensp;&ensp;子掩网码与得出  
  
67是服务器端口号&ensp;&ensp;68是客户端口号  
  
vim&ensp;&ensp;/etc/hosts  
  
vim&ensp;&ensp;/etc/nsswitch.conf&ensp;&ensp;hosts那行&ensp;&ensp;可以改优先级  
  
vim&ensp;&ensp;/etc/sysconfig/network&ensp;&ensp;&ensp;centos6改主机名字&ensp;&ensp;&ensp;exec&ensp;&ensp;bash&ensp;显示了就  
hostnamectl&ensp;set-hostname&ensp;&ensp;centos7.localdomain&ensp;&ensp;&ensp;把名字改成7  
打开改文件&ensp;&ensp;vim&ensp;&ensp;/etc/hosts&ensp;&ensp;&ensp;&ensp;第一行最后边加centos7.localdomain  
exec&ensp;&ensp;bash&ensp;&ensp;显示了就  
modprobe&ensp;&ensp;-r&ensp;e1000&ensp;&ensp;删除e1000这个驱动  
打开&ensp;centos6&ensp;输入modprobe&ensp;&ensp;e1000安装驱动  
  
route命令  
route&ensp;add&ensp;添加路由  
route&ensp;&ensp;add&ensp;&ensp;-host&ensp;&ensp;仅主机路由&ensp;一台电脑  
route&ensp;add&ensp;&ensp;-net&ensp;&ensp;一个网络  
route&ensp;add&ensp;default&ensp;默认路由  
gw&ensp;&ensp;网关  
  
删除网卡&ensp;列如  
ifconfig&ensp;&ensp;virbr0&ensp;&ensp;down  
  
centos6&ensp;&ensp;关&ensp;&ensp;重置  
service&ensp;NetworkManager&ensp;restart  
service&ensp;NetworkManager&ensp;stop  
service&ensp;&ensp;network&ensp;restart&ensp;&ensp;----重置  
systemctl&ensp;restart&ensp;network&ensp;&ensp;重置网络7  
  
echo&ensp;1&ensp;>&ensp;/proc/sys/net/ipv4/ip_forward  
