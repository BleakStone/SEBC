<h1>Treasure Hunt</h1>
<ul>
	<li>
		<p>What is ubertask optimization? </p>
		<p>ubertask optimization runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.</p>
	</li>
	<li>
		<p>Where in CM is the Kerberos Security Realm value displayed?</p>
		<p>Administration-> Setting -> Kerberos</p>
	</li>
	<li>
		<p>Which CDH service(s) host a property for enabling Kerberos authentication?</p>
		<p>Hive;Zookeeper;Hue;Oozie;HDFS;Yarn;CM services</p>
	</li>
	<li>
		<p>How do you upgrade the CM agents?</p>
		<p>Cluster -> Upgrade Cluster</p>
	</li>
	<li>
		<p>Give the tsquery statement used to chart Hue's CPU utilization?</p>
		<p>SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-HUE_SERVER-b3d2790c92070f4d31a16d2ca98365bc" AND category = ROLE</p>
	</li>
	<li>
		<p>Name all the roles that make up the Hive service</p>
		<p>Hive Metastore Server;WebHCat Server;HiveServer2;Gateway</p>
	</li>
	<li>
		<p>What steps must be completed before integrating Cloudera Manager with Kerberos?</p>
		<ul>
		<li>Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.</li>
		<li>The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. </li>
		<li>OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.</li>
		<li>Cloudera Manager needs an account that has permissions to create other accounts in the KDC.</li>
		</ul>
	</li>
</ul>
