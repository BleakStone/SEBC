<h1>Test HDFS throughput</h1>
<ul>
<li>
teragen <code>time hadoop jar hadoop-examples.jar teragen  -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432  100000000 /user/gorden2/gorden2DataBig  </code>
Result:
<pre>
17/05/09 07:35:51 INFO mapreduce.Job: Job job_1494303558603_0009 completed successfully
17/05/09 07:35:51 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494168
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters 
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=491017
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=491017
                Total vcore-seconds taken by all map tasks=491017
                Total megabyte-seconds taken by all map tasks=502801408
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1799
                CPU time spent (ms)=155600
                Physical memory (bytes) snapshot=925028352
                Virtual memory (bytes) snapshot=6243196928
                Total committed heap usage (bytes)=851443712
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=10000000000
real    2m27.946s
user    0m5.741s
sys     0m0.722s

</pre>
</li>

<li>
terasort <code>time hadoop jar hadoop-examples.jar terasort /user/gorden2/gorden2DataBig /user/gorden2/gorden2DataBigSort  </code>
Result:
<pre>
17/05/09 07:46:51 INFO mapreduce.Job: Job job_1494303558603_0010 completed successfully
17/05/09 07:46:51 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4508731301
                FILE: Number of bytes written=8921605388
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000048000
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=906
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters 
                Launched map tasks=300
                Launched reduce tasks=2
                Data-local map tasks=299
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=3532576
                Total time spent by all reduces in occupied slots (ms)=356713
                Total time spent by all map tasks (ms)=3532576
                Total time spent by all reduce tasks (ms)=356713
                Total vcore-seconds taken by all map tasks=3532576
                Total vcore-seconds taken by all reduce tasks=356713
                Total megabyte-seconds taken by all map tasks=3617357824
                Total megabyte-seconds taken by all reduce tasks=365274112
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375125545
                Input split bytes=48000
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375125545
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =600
                Failed Shuffles=0
                Merged Map outputs=600
                GC time elapsed (ms)=34697
                CPU time spent (ms)=1503950
                Physical memory (bytes) snapshot=139950211072
                Virtual memory (bytes) snapshot=472166813696
                Total committed heap usage (bytes)=170772135936
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=10000000000
        File Output Format Counters 
                Bytes Written=10000000000
17/05/09 07:46:51 INFO terasort.TeraSort: done
real    6m6.390s
user    0m9.089s
sys     0m0.931s
</pre>
</li>
</ul>

