<h1>MySQL replica</h1>
<ol>
<li>Download and implement the official MySQL repo <br/>
<p>Choose mysql55 in mysql-community.repo</p>
<pre>
# wget http://repo.mysql.com/mysql57-community-release-el6-11.noarch.rpm
# rpm -ivh mysql57-community-release-el6-11.noarch.rpm
# vi /etc/yum.repos.d/mysql-community.repo 
# yum install mysql
# yum install mysql-server
</pre>
</li>


<li> SHOW MASTER STATUS <br/>
<code>mysql> SHOW MASTER STATUS; </code> <br/>
<pre>
+------------------+----------+--------------+------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+------------------+----------+--------------+------------------+
| mysql-bin.000001 |     1240 |              |                  |
+------------------+----------+--------------+------------------+
1 row in set (0.00 sec)
</pre>
</li>


<li> Configure Slave and Master <br/>
<code>mysql> SHOW MASTER STATUS; </code> <br/>
<code>GRANT REPLICATION SLAVE ON *.* TO 'root'@'ip-172-31-0-114.us-west-1.compute.internal' IDENTIFIED BY '123456';</code> <br/>
<code>CHANGE MASTER TO MASTER_HOST='ip-172-31-0-228.us-west-1.compute.internal', MASTER_USER='root', MASTER_PASSWORD='123456', MASTER_LOG_FILE='mysql-bin.000001', MASTER_LOG_POS=1240;</code> <br/>
<pre>
+------------------+----------+--------------+------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+------------------+----------+--------------+------------------+
| mysql-bin.000001 |     1240 |              |                  |
+------------------+----------+--------------+------------------+
1 row in set (0.00 sec)
</pre>
</li>

<li> Show result <br/> 
<code> mysql> SHOW SLAVE STATUS \G </code> <br/>
<pre>
*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: ip-172-31-0-228.us-west-1.compute.internal
                  Master_User: root
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysql-bin.000001
          Read_Master_Log_Pos: 1240
               Relay_Log_File: mysqld-relay-bin.000003
                Relay_Log_Pos: 253
        Relay_Master_Log_File: mysql-bin.000001
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB: 
          Replicate_Ignore_DB: 
           Replicate_Do_Table: 
       Replicate_Ignore_Table: 
      Replicate_Wild_Do_Table: 
  Replicate_Wild_Ignore_Table: 
                   Last_Errno: 0
                   Last_Error: 
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 1240
              Relay_Log_Space: 410
              Until_Condition: None
               Until_Log_File: 
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File: 
           Master_SSL_CA_Path: 
              Master_SSL_Cert: 
            Master_SSL_Cipher: 
               Master_SSL_Key: 
        Seconds_Behind_Master: 0
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error: 
               Last_SQL_Errno: 0
               Last_SQL_Error: 
  Replicate_Ignore_Server_Ids: 
             Master_Server_Id: 1
1 row in set (0.00 sec)
</pre>
</li>
</ol>
