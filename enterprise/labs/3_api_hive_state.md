<h1>Hive API</h1> 
<ul>
<li>Stop Command: <br/>
<code>curl -X POST -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive/commands/stop"</code>
<br/>
<pre>
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-0-228.us-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-0-228.us-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "STALE",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}
</pre>
</li>
<li>Start Command: <br/>
<code>curl -X POST -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive/commands/start"</code>
<br/>
<pre>
{
  "id" : 696,
  "name" : "Stop",
  "startTime" : "2017-05-10T04:14:11.340Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
</pre>
</li>
<li>check Command: <br/>
<code>curl -X GET -u gorden2:cloudera "http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v12/clusters/cluster/services/hive"</code>
<br/>
<pre>
{
  "id" : 699,
  "name" : "Start",
  "startTime" : "2017-05-10T04:14:42.661Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
</pre>
</li>
</ul>