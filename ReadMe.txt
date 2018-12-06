MySql初始化脚本思路
1、参数设置
	DB_USER：用户
	DB_PASS：密码
	DATA_DIR：安装目录
	三个参数可以全部写在Dockfile中传递到脚本
	现在为了方便，只将DATA_DIR写在脚本中
2、其他的参考mariadb进行的执行脚本
3、参考网址:https://gitee.com/DowneyJr./docker-training
4、创建Mysql容器
修改From enzoism/centos:7.1	(DATA_DIR:/var/lib/mysql)
添加rpm --rebuilddb &&
docker build -t enzoism/mysql:7.1 .
docker run -d -it -p 3306:3306 --name mySQL enzoism/mysql:7.1 
docker exec -it mySQL /bin/bash	#进入mySQL
mysql
show databases;
CREATE DATABASE fisrtData;
// 然后将WordPress和Mysql连接起来
ifconfig 查看公网IP：192.168.18.136
docker run -d -p 3306:3306 --name mySQL -v /var/lib/docker/vfs/dir/mydata:/var/lib/mysql enzoism/mysql:7.1 	
