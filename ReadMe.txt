MySql��ʼ���ű�˼·
1����������
	DB_USER���û�
	DB_PASS������
	DATA_DIR����װĿ¼
	������������ȫ��д��Dockfile�д��ݵ��ű�
	����Ϊ�˷��㣬ֻ��DATA_DIRд�ڽű���
2�������Ĳο�mariadb���е�ִ�нű�
3���ο���ַ:https://gitee.com/DowneyJr./docker-training
4������Mysql����
�޸�From enzoism/centos:7.1	(DATA_DIR:/var/lib/mysql)
���rpm --rebuilddb &&
docker build -t enzoism/mysql:7.1 .
docker run -d -it -p 3306:3306 --name mySQL enzoism/mysql:7.1 
docker exec -it mySQL /bin/bash	#����mySQL
mysql
show databases;
CREATE DATABASE fisrtData;
// Ȼ��WordPress��Mysql��������
ifconfig �鿴����IP��192.168.18.136
docker run -d -p 3306:3306 --name mySQL -v /var/lib/docker/vfs/dir/mydata:/var/lib/mysql enzoism/mysql:7.1 	
