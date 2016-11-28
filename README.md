# vagrant-MariaDB-Master-Master-Active-StandBy
MariaDB/MySQL HA with 2 nodes: Master-Master replication and Active/StandBy Cluster
Architecture
![mariadb-master-master-active-standby](https://cloud.githubusercontent.com/assets/23556472/20674300/62d70842-b556-11e6-98e3-87312c6b8329.png)

This Vagrant will create 2 2 CentOS/7 nodes:
1-firstnode:

      - install MariaDB(MySQL), 
      
      - install Pacemaker, 
      
      - modify /etc/hosts to have only localhost pointing to loopback IP : 127.0.0.1
        (for the replication and cluster to get up using the assigned IPs not the loopback IP)
        
      - create a DB for Zabbix,
      
      - configure remote access for MYSQL from the second node 
        (so replication would be configured while provisionning the second node)
      

1-Second node : 

      - install MariaDB(MySQL), 
      
      - install Pacemaker, 
      
      - modify /etc/hosts to have only localhost pointing to loopback IP : 127.0.0.1 
        (for the replication and cluster to get up using the assigned IPs not the loopback IP)
        
      - create a DB for Zabbix,
      
      - configure remote access for MYSQL from the first node,
      
      - Configure the 2 DB servers as MASTERS with MASTER-MASTER replication,
      
      - Configure Pacemaker as an Active/Standby cluster with a floating cluster_VIP 
      - and 2 actives MariaDB(MYSQL) instances (1 instance on each node).


