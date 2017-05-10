<h1>Hive API</h1> 
<ul>
<li>Stop Command: <code>curl -X POST -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive/commands/stop"</code></li>
<li>Start Command: <code>curl -X POST -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive/commands/start"</code></li>
<li>check Command: <code>curl -X GET -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive"</code></li>
</ul>