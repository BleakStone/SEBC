<h1>Cloudera Manager Install</h1>
<ol>
<li>
install using CM 5.9.x <br/>
<ul>
<li>Install JDK: <code>yum install oracle-j2sdk1.7</code></li>
<li>Download Repos: <code>wget https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5.9.2/RPMS/x86_64/cloudera-manager-server-5.9.2-1.cm592.p0.3.el6.x86_64.rpm</code></li>
<li>Install Deamon: <code>yum --nogpgcheck localinstall cloudera-manager-daemons-*.rpm</code></li>
<li>Install Server: <code>yum --nogpgcheck localinstall cloudera-manager-server-*.rpm</code></li>
<li>Prepare Database: <code>./scm_prepare_database.sh mysql scm  root 123456</code></li>
<li>Enable Root Full Access: 
<pre>
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' 
    IDENTIFIED BY '123456' 
    WITH GRANT OPTION;
    FLUSH PRIVILEGES;
</pre></li>
</ul>
</li>

</ol>

