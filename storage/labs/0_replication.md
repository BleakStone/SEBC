<h1>Replicate to another cluster</h1>
<ul>
<li>
Start with create teragenFile <code>hadoop jar hadoop-examples.jar teragen  5000000 /user/gorden2/gorden2Data </code>
</li>
<li>
Change the hosts: Add new host
<pre>
34.208.80.199 ip-172-31-37-12.us-west-2.compute.internal
35.161.179.128 ip-172-31-37-146.us-west-2.compute.internal
52.40.130.144 ip-172-31-41-227.us-west-2.compute.internal
</pre>
</li>
<li>
Move Data <code>
sudo -u hdfs hadoop distcp hftp://ec2-35-161-179-128.us-west-2.compute.amazonaws.com:50070/user/littlecong/teragen  hdfs://ec2-54-193-126-200.us-west-1.compute.amazonaws.com:8020/user/gorden2 </code>
</li>
<li>
Check result: 
<code>sudo -u hdfs hdfs fsck /user/gorden2/ -files -blocks</code> <br/>
<pre>
Connecting to namenode via http://ip-172-31-0-114.us-west-1.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.0.228 for path /user/gorden2/ at Tue May 09 07:11:23 UTC 2017
/user/gorden2/ <dir>
/user/gorden2/.Trash <dir>
/user/gorden2/.Trash/Current <dir>
/user/gorden2/.Trash/Current/tmp <dir>
/user/gorden2/.staging <dir>
/user/gorden2/gorden2Data <dir>
/user/gorden2/gorden2Data/_SUCCESS 0 bytes, 0 block(s):  OK

/user/gorden2/gorden2Data/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-359824052-172.31.0.114-1494295739360:blk_1073742693_1869 len=134217728 Live_repl=3
1. BP-359824052-172.31.0.114-1494295739360:blk_1073742696_1872 len=115782272 Live_repl=3

/user/gorden2/gorden2Data/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-359824052-172.31.0.114-1494295739360:blk_1073742692_1868 len=134217728 Live_repl=3
1. BP-359824052-172.31.0.114-1494295739360:blk_1073742695_1871 len=115782272 Live_repl=3

/user/gorden2/teragen <dir>
/user/gorden2/teragen/_SUCCESS 0 bytes, 0 block(s):  OK

/user/gorden2/teragen/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-359824052-172.31.0.114-1494295739360:blk_1073743111_2289 len=134217728 Live_repl=3
1. BP-359824052-172.31.0.114-1494295739360:blk_1073743114_2292 len=127926272 Live_repl=3

/user/gorden2/teragen/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-359824052-172.31.0.114-1494295739360:blk_1073743110_2288 len=134217728 Live_repl=3
1. BP-359824052-172.31.0.114-1494295739360:blk_1073743113_2291 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    1024288000 B
 Total dirs:    7
 Total files:   6
 Total symlinks:                0
 Total blocks (validated):      8 (avg. block size 128036000 B)
 Minimally replicated blocks:   8 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          5
 Number of racks:               1
FSCK ended at Tue May 09 07:11:23 UTC 2017 in 3 milliseconds


The filesystem under path '/user/gorden2/' is HEALTHY
</pre>
</li>
</ul>