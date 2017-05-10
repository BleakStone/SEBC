<h1>Upgrade CM</h1>
<ul>
<li>
Report the latest available version of the API <code>http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/version</code>
<br/>
v16
</li>

<li>
Report the CM version <code>http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v16/cm/version</code>
<br/>
<pre>
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1249",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}
</pre>
</li>

<li>
List all CM users <code>http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v16/users</code>
<br/>
<pre>
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "gorden2",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
</pre>
</li>

<li>
Report the database server in use by CM: <code>http://ec2-54-215-192-38.us-west-1.compute.amazonaws.com:7180/api/v16/cm/scmDbInfo</code>
<br/>
<pre>
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
</pre>
</li>
</ul>