# vagrant-MariaDB-Master-Master-Active-StandBy
MariaDB/MySQL HA with 2 nodes: Master-Master replication and Active/StandBy Cluster
Architecture
![mariadb-master-master-active-standby](https://cloud.githubusercontent.com/assets/23556472/20674300/62d70842-b556-11e6-98e3-87312c6b8329.png)

This Vagrant will :
- Create 2 CentOS/7 nodes, 
- install MAriaDB(MySQL), 
- install Pacemaker, 
- create a DB for Zabbix,
- Configure the 2 MySQL servers as MASTERS with MASTER-MASTER replication.
- Configure Pacemaker as an Active/STandby cluster with a floating cluster_VIP and 2 actives MYSQL instances(1 instance on each node)
