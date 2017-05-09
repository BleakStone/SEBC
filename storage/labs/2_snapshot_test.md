<h1>Test HDFS throughput</h1>
<ul>

<li> Put File: <br/>
<pre>
hadoop fs -mkdir previous
hadoop fs -put SEBC-Shanghai.zip  ./previous
</pre>
</li>

<li>Allow Snapshot: <code>sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/gorden2/previous</code> <br/>
Result: <code>Allowing snaphot on /user/gorden2/previous succeeded</code></li>


<li>Create SnapShot: <code>hdfs dfs -createSnapshot /user/gorden2/previous sebc-hdfs-test</code><br/>
Result: <code>Created snapshot /user/gorden2/previous/.snapshot/sebc-hdfs-test</code></li>

<li>Remove Directory: <code>hadoop fs -rm -r ./previous</code> <br/>
Result: <code>rm: Failed to move to trash: hdfs://ip-172-31-0-114.us-west-1.compute.internal:8020/user/gorden2/previous: The directory /user/gorden2/previous cannot be deleted since /user/gorden2/previous is snapshottable and already has snapshots</code>
</li>

<li>Remove File: <code>hadoop fs -rm  ./previous/SEBC-Shanghai.zip</code> <br/>
Result: <code>17/05/09 08:08:58 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-0-114.us-west-1.compute.internal:8020/user/gorden2/previous/SEBC-Shanghai.zip' to trash at: hdfs://ip-172-31-0-114.us-west-1.compute.internal:8020/user/gorden2/.Trash/Current/user/gorden2/previous/SEBC-Shanghai.zip</code>
</li>

<li>Remove File <code>hdfs dfs -cp  /user/gorden2/previous/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip /user/gorden2/previous</code> <br/>
Result: <br/>
<pre>
hadoop fs -ls ./previous
Found 1 items
-rw-r--r--   3 gorden2 supergroup     474957 2017-05-09 08:16 previous/SEBC-Shanghai.zip</pre>
</li>





</ul>
