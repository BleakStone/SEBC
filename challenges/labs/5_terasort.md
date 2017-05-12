
<pre>
kinit zhou 
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort   ./tgen  ./tsort

17/05/12 03:17:54 INFO terasort.TeraSort: starting
17/05/12 03:17:56 INFO hdfs.DFSClient: Created token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@GORDEN2.CN, renewer=yarn, realUser=, issueDate=1494559076339, maxDate=1495163876339, sequenceNumber=1, masterKeyId=2 on 172.31.4.240:8020
17/05/12 03:17:56 INFO security.TokenCache: Got dt for hdfs://ip-172-31-4-240.us-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.4.240:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@GORDEN2.CN, renewer=yarn, realUser=, issueDate=1494559076339, maxDate=1495163876339, sequenceNumber=1, masterKeyId=2)
17/05/12 03:17:56 INFO input.FileInputFormat: Total input paths to process : 6
Spent 371ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 378ms
Sampling 10 splits of 102
Making 10 from 100000 sampled records
Computing parititions took 928ms
Spent 1308ms computing partitions.
17/05/12 03:17:57 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-4-240.us-west-1.compute.internal/172.31.4.240:8032
17/05/12 03:17:58 INFO mapreduce.JobSubmitter: number of splits:102
17/05/12 03:17:58 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494558707566_0001
17/05/12 03:17:58 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.4.240:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@GORDEN2.CN, renewer=yarn, realUser=, issueDate=1494559076339, maxDate=1495163876339, sequenceNumber=1, masterKeyId=2)
17/05/12 03:17:59 INFO impl.YarnClientImpl: Submitted application application_1494558707566_0001
17/05/12 03:17:59 INFO mapreduce.Job: The url to track the job: http://ip-172-31-4-240.us-west-1.compute.internal:8088/proxy/application_1494558707566_0001/
17/05/12 03:17:59 INFO mapreduce.Job: Running job: job_1494558707566_0001
17/05/12 03:18:09 INFO mapreduce.Job: Job job_1494558707566_0001 running in uber mode : false
17/05/12 03:18:09 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:18:20 INFO mapreduce.Job:  map 2% reduce 0%
17/05/12 03:18:22 INFO mapreduce.Job:  map 3% reduce 0%
17/05/12 03:18:24 INFO mapreduce.Job:  map 4% reduce 0%
17/05/12 03:18:25 INFO mapreduce.Job:  map 7% reduce 0%
17/05/12 03:18:28 INFO mapreduce.Job:  map 8% reduce 0%
17/05/12 03:18:29 INFO mapreduce.Job:  map 11% reduce 0%
17/05/12 03:18:30 INFO mapreduce.Job:  map 13% reduce 0%
17/05/12 03:18:34 INFO mapreduce.Job:  map 17% reduce 0%
17/05/12 03:18:38 INFO mapreduce.Job:  map 19% reduce 0%
17/05/12 03:18:39 INFO mapreduce.Job:  map 21% reduce 0%
17/05/12 03:18:40 INFO mapreduce.Job:  map 22% reduce 0%
17/05/12 03:18:41 INFO mapreduce.Job:  map 23% reduce 0%
17/05/12 03:18:43 INFO mapreduce.Job:  map 24% reduce 0%
17/05/12 03:18:44 INFO mapreduce.Job:  map 26% reduce 0%
17/05/12 03:18:46 INFO mapreduce.Job:  map 27% reduce 0%
17/05/12 03:18:47 INFO mapreduce.Job:  map 28% reduce 0%
17/05/12 03:18:48 INFO mapreduce.Job:  map 29% reduce 0%
17/05/12 03:18:51 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 03:18:52 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 03:18:53 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 03:18:54 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 03:18:56 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 03:18:57 INFO mapreduce.Job:  map 39% reduce 0%
17/05/12 03:19:01 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 03:19:03 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 03:19:04 INFO mapreduce.Job:  map 46% reduce 0%
17/05/12 03:19:05 INFO mapreduce.Job:  map 47% reduce 0%
17/05/12 03:19:07 INFO mapreduce.Job:  map 48% reduce 0%
17/05/12 03:19:09 INFO mapreduce.Job:  map 49% reduce 0%
17/05/12 03:19:11 INFO mapreduce.Job:  map 51% reduce 0%
17/05/12 03:19:12 INFO mapreduce.Job:  map 52% reduce 0%
17/05/12 03:19:13 INFO mapreduce.Job:  map 54% reduce 0%
17/05/12 03:19:14 INFO mapreduce.Job:  map 55% reduce 0%
17/05/12 03:19:15 INFO mapreduce.Job:  map 56% reduce 0%
17/05/12 03:19:16 INFO mapreduce.Job:  map 57% reduce 0%
17/05/12 03:19:18 INFO mapreduce.Job:  map 58% reduce 0%
17/05/12 03:19:19 INFO mapreduce.Job:  map 60% reduce 0%
17/05/12 03:19:20 INFO mapreduce.Job:  map 61% reduce 0%
17/05/12 03:19:21 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 03:19:23 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 03:19:25 INFO mapreduce.Job:  map 65% reduce 0%
17/05/12 03:19:27 INFO mapreduce.Job:  map 68% reduce 0%
17/05/12 03:19:28 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 03:19:29 INFO mapreduce.Job:  map 70% reduce 0%
17/05/12 03:19:30 INFO mapreduce.Job:  map 72% reduce 0%
17/05/12 03:19:33 INFO mapreduce.Job:  map 74% reduce 0%
17/05/12 03:19:35 INFO mapreduce.Job:  map 75% reduce 0%
17/05/12 03:19:38 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 03:19:39 INFO mapreduce.Job:  map 80% reduce 0%
17/05/12 03:19:40 INFO mapreduce.Job:  map 81% reduce 0%
17/05/12 03:19:43 INFO mapreduce.Job:  map 84% reduce 0%
17/05/12 03:19:47 INFO mapreduce.Job:  map 86% reduce 0%
17/05/12 03:19:48 INFO mapreduce.Job:  map 87% reduce 0%
17/05/12 03:19:49 INFO mapreduce.Job:  map 89% reduce 0%
17/05/12 03:19:50 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 03:19:51 INFO mapreduce.Job:  map 91% reduce 0%
17/05/12 03:19:52 INFO mapreduce.Job:  map 91% reduce 3%
17/05/12 03:19:53 INFO mapreduce.Job:  map 92% reduce 3%
17/05/12 03:19:54 INFO mapreduce.Job:  map 92% reduce 6%
17/05/12 03:19:57 INFO mapreduce.Job:  map 94% reduce 6%
17/05/12 03:19:58 INFO mapreduce.Job:  map 94% reduce 12%
17/05/12 03:19:59 INFO mapreduce.Job:  map 95% reduce 12%
17/05/12 03:20:00 INFO mapreduce.Job:  map 95% reduce 15%
17/05/12 03:20:01 INFO mapreduce.Job:  map 96% reduce 16%
17/05/12 03:20:02 INFO mapreduce.Job:  map 97% reduce 16%
17/05/12 03:20:03 INFO mapreduce.Job:  map 98% reduce 16%
17/05/12 03:20:04 INFO mapreduce.Job:  map 99% reduce 16%
17/05/12 03:20:05 INFO mapreduce.Job:  map 100% reduce 16%
17/05/12 03:20:07 INFO mapreduce.Job:  map 100% reduce 21%
17/05/12 03:20:09 INFO mapreduce.Job:  map 100% reduce 24%
17/05/12 03:20:10 INFO mapreduce.Job:  map 100% reduce 32%
17/05/12 03:20:12 INFO mapreduce.Job:  map 100% reduce 33%
17/05/12 03:20:13 INFO mapreduce.Job:  map 100% reduce 36%
17/05/12 03:20:14 INFO mapreduce.Job:  map 100% reduce 49%
17/05/12 03:20:15 INFO mapreduce.Job:  map 100% reduce 50%
17/05/12 03:20:16 INFO mapreduce.Job:  map 100% reduce 55%
17/05/12 03:20:17 INFO mapreduce.Job:  map 100% reduce 65%
17/05/12 03:20:19 INFO mapreduce.Job:  map 100% reduce 72%
17/05/12 03:20:20 INFO mapreduce.Job:  map 100% reduce 79%
17/05/12 03:20:21 INFO mapreduce.Job:  map 100% reduce 81%
17/05/12 03:20:22 INFO mapreduce.Job:  map 100% reduce 83%
17/05/12 03:20:23 INFO mapreduce.Job:  map 100% reduce 87%
17/05/12 03:20:25 INFO mapreduce.Job:  map 100% reduce 89%
17/05/12 03:20:27 INFO mapreduce.Job:  map 100% reduce 93%
17/05/12 03:20:29 INFO mapreduce.Job:  map 100% reduce 95%
17/05/12 03:20:30 INFO mapreduce.Job:  map 100% reduce 97%
17/05/12 03:20:33 INFO mapreduce.Job:  map 100% reduce 99%
17/05/12 03:20:35 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 03:20:35 INFO mapreduce.Job: Job job_1494558707566_0001 completed successfully
17/05/12 03:20:35 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2929232240
                FILE: Number of bytes written=5816389837
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553614994
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=336
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=20
        Job Counters 
                Launched map tasks=102
                Launched reduce tasks=10
                Data-local map tasks=101
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=921161
                Total time spent by all reduces in occupied slots (ms)=318336
                Total time spent by all map tasks (ms)=921161
                Total time spent by all reduce tasks (ms)=318336
                Total vcore-seconds taken by all map tasks=921161
                Total vcore-seconds taken by all reduce tasks=318336
                Total megabyte-seconds taken by all map tasks=943268864
                Total megabyte-seconds taken by all reduce tasks=325976064
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2873073543
                Input split bytes=14994
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2873073543
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =1020
                Failed Shuffles=0
                Merged Map outputs=1020
                GC time elapsed (ms)=17164
                CPU time spent (ms)=749230
                Physical memory (bytes) snapshot=60194099200
                Virtual memory (bytes) snapshot=175337877504
                Total committed heap usage (bytes)=69017272320
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=6553600000
        File Output Format Counters 
                Bytes Written=6553600000
17/05/12 03:20:35 INFO terasort.TeraSort: done
</pre>