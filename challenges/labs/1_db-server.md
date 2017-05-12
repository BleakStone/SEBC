1_db-server.md
1. ip-172-31-9-140.us-west-1.compute.internal
2. 
<pre>
[root@ip-172-31-9-140 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper
</pre>
3. 
<pre>
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
</pre>