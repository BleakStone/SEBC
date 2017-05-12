1. 
<pre>
[root@ip-172-31-4-240 ~]# time sudo -u zhou hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen  -Ddfs.blocksize=67108864 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.job.maps=6  65536000 ./tgen
17/05/12 02:34:25 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-4-240.us-west-1.compute.internal/172.31.4.240:8032
17/05/12 02:34:26 INFO terasort.TeraSort: Generating 65536000 using 6
17/05/12 02:34:26 INFO mapreduce.JobSubmitter: number of splits:6
17/05/12 02:34:26 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494554833982_0003
17/05/12 02:34:27 INFO impl.YarnClientImpl: Submitted application application_1494554833982_0003
17/05/12 02:34:27 INFO mapreduce.Job: The url to track the job: http://ip-172-31-4-240.us-west-1.compute.internal:8088/proxy/application_1494554833982_0003/
17/05/12 02:34:27 INFO mapreduce.Job: Running job: job_1494554833982_0003
17/05/12 02:34:33 INFO mapreduce.Job: Job job_1494554833982_0003 running in uber mode : false
17/05/12 02:34:33 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 02:34:44 INFO mapreduce.Job:  map 5% reduce 0%
17/05/12 02:34:45 INFO mapreduce.Job:  map 10% reduce 0%
17/05/12 02:34:46 INFO mapreduce.Job:  map 21% reduce 0%
17/05/12 02:34:47 INFO mapreduce.Job:  map 22% reduce 0%
17/05/12 02:34:48 INFO mapreduce.Job:  map 25% reduce 0%
17/05/12 02:34:49 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 02:34:50 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 02:34:51 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 02:34:52 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 02:34:53 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 02:34:55 INFO mapreduce.Job:  map 41% reduce 0%
17/05/12 02:34:56 INFO mapreduce.Job:  map 42% reduce 0%
17/05/12 02:34:57 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 02:34:58 INFO mapreduce.Job:  map 46% reduce 0%
17/05/12 02:34:59 INFO mapreduce.Job:  map 47% reduce 0%
17/05/12 02:35:00 INFO mapreduce.Job:  map 48% reduce 0%
17/05/12 02:35:01 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 02:35:02 INFO mapreduce.Job:  map 52% reduce 0%
17/05/12 02:35:04 INFO mapreduce.Job:  map 56% reduce 0%
17/05/12 02:35:05 INFO mapreduce.Job:  map 59% reduce 0%
17/05/12 02:35:07 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 02:35:08 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 02:35:10 INFO mapreduce.Job:  map 67% reduce 0%
17/05/12 02:35:11 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 02:35:13 INFO mapreduce.Job:  map 71% reduce 0%
17/05/12 02:35:14 INFO mapreduce.Job:  map 74% reduce 0%
17/05/12 02:35:16 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 02:35:17 INFO mapreduce.Job:  map 79% reduce 0%
17/05/12 02:35:19 INFO mapreduce.Job:  map 81% reduce 0%
17/05/12 02:35:22 INFO mapreduce.Job:  map 85% reduce 0%
17/05/12 02:35:25 INFO mapreduce.Job:  map 89% reduce 0%
17/05/12 02:35:28 INFO mapreduce.Job:  map 93% reduce 0%
17/05/12 02:35:32 INFO mapreduce.Job:  map 96% reduce 0%
17/05/12 02:35:34 INFO mapreduce.Job:  map 97% reduce 0%
17/05/12 02:35:35 INFO mapreduce.Job:  map 99% reduce 0%
17/05/12 02:35:37 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 02:35:37 INFO mapreduce.Job: Job job_1494554833982_0003 completed successfully
17/05/12 02:35:37 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=741090
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=511
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters 
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=320383
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=320383
                Total vcore-seconds taken by all map tasks=320383
                Total megabyte-seconds taken by all map tasks=328072192
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=511
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1030
                CPU time spent (ms)=119350
                Physical memory (bytes) snapshot=1960886272
                Virtual memory (bytes) snapshot=9387859968
                Total committed heap usage (bytes)=1969225728
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=6553600000

real    1m14.828s
user    0m6.493s
sys     0m0.775s

</pre>

2.
<pre>
[root@ip-172-31-4-240 ~]# hdfs dfs -ls /user/zhou/tgen
Found 7 items
-rw-r--r--   3 zhou beijing          0 2017-05-12 02:35 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:35 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:35 /user/zhou/tgen/part-m-00001
-rw-r--r--   3 zhou beijing 1092266600 2017-05-12 02:35 /user/zhou/tgen/part-m-00002
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:35 /user/zhou/tgen/part-m-00003
-rw-r--r--   3 zhou beijing 1092266700 2017-05-12 02:35 /user/zhou/tgen/part-m-00004
-rw-r--r--   3 zhou beijing 1092266600 2017-05-12 02:35 /user/zhou/tgen/part-m-00005
</pre>