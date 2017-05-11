<h1>Sentry</h1>

<ul>
<li> User root: <br/> 
<pre>
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-0-114.us-west-1.compute.internal:10000/default;principal=hive/ip-172-31-0-114.us-west-1.compute.internal@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-0-114.us-west-1.compute.internal:10000/default;principal=hive/ip-172-31-0-114.us-west-1.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-0-114.us-west-1.com> show tables;
INFO  : Compiling command(queryId=hive_20170510091414_866d9144-a994-451a-b378-c5ce16cf7033): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170510091414_866d9144-a994-451a-b378-c5ce16cf7033); Time taken: 0.777 seconds
INFO  : Executing command(queryId=hive_20170510091414_866d9144-a994-451a-b378-c5ce16cf7033): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170510091414_866d9144-a994-451a-b378-c5ce16cf7033); Time taken: 0.309 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.542 seconds)
</pre>
</li>
<li>User george: <br/>
<pre>
0: jdbc:hive2://ip-172-31-0-114.us-west-1.com> show tables;
INFO  : Compiling command(queryId=hive_20170511010707_6ce5abfb-2a62-49e8-821c-635000fdab42): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170511010707_6ce5abfb-2a62-49e8-821c-635000fdab42); Time taken: 0.091 seconds
INFO  : Executing command(queryId=hive_20170511010707_6ce5abfb-2a62-49e8-821c-635000fdab42): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511010707_6ce5abfb-2a62-49e8-821c-635000fdab42); Time taken: 0.125 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
</pre>
</li>

<li>User ferdinand<br/>
<pre>
0: jdbc:hive2://ip-172-31-0-114.us-west-1.com> show tables;
INFO  : Compiling command(queryId=hive_20170511010808_32132e08-2d25-4c09-81d1-fd9d083409c9): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170511010808_32132e08-2d25-4c09-81d1-fd9d083409c9); Time taken: 0.079 seconds
INFO  : Executing command(queryId=hive_20170511010808_32132e08-2d25-4c09-81d1-fd9d083409c9): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511010808_32132e08-2d25-4c09-81d1-fd9d083409c9); Time taken: 0.125 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.302 seconds)
</pre>
</li>
</ul>