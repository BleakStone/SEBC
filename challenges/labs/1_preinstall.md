<h1>Preinstall</h1>

<ol>
<li> Check vm.swappiness on all your nodes  <br/>
Command: <code># sysctl vm.swappiness</code>  <br/>
vm.swappiness = 60  <br/>
<code># sysctl vm.swappiness=1  </code>  <br/>
vm.swappiness = 1 
</li>

<br/>

<li>
Show the mount attributes of your volume(s) <br/>
Command: <code># cat /proc/mounts</code>
<p>Result: /dev/xvde / ext4</p>
<pre>
rootfs / rootfs rw 0 0  
proc /proc proc rw,relatime 0 0  
sysfs /sys sysfs rw,seclabel,relatime 0 0  
devtmpfs /dev devtmpfs rw,seclabel,relatime,size=7674908k,nr_inodes=1918727,mode=755 0 0  
devpts /dev/pts devpts rw,seclabel,relatime,gid=5,mode=620,ptmxmode=000 0 0  
tmpfs /dev/shm tmpfs rw,seclabel,relatime 0 0  
/dev/xvde / ext4 rw,seclabel,relatime,barrier=1,data=ordered 0 0  
none /selinux selinuxfs rw,relatime 0 0  
devtmpfs /dev devtmpfs rw,seclabel,relatime,size=7674908k,nr_inodes=1918727,mode=755 0 0  
/proc/bus/usb /proc/bus/usb usbfs rw,relatime 0 0  
none /proc/sys/fs/binfmt_misc binfmt_misc rw,relatime 0 0  
</pre>
</li>

<br/>

<li>
list the reserve space setting <br/>
Command: <code># tune2fs -l /dev/xvde</code>
<code># resize2fs /dev/xvde </code>
<p>
Result:  Reserved block count:     104857
</p>
<pre>
tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   centos_root
Last mounted on:          /
Filesystem UUID:          44d27f92-d3df-4207-80ea-22830afccf03
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash 
Default mount options:    (none)
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              524288
Block count:              2097152
Reserved block count:     104857
Free blocks:              1897885
Free inodes:              509067
First block:              0
Block size:               4096
Fragment size:            4096
Reserved GDT blocks:      511
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         8192
Inode blocks per group:   512
Flex block group size:    16
Filesystem created:       Tue Feb  4 23:38:21 2014
Last mount time:          Mon May  8 06:10:15 2017
Last write time:          Tue Feb  4 23:40:03 2014
Mount count:              3
Maximum mount count:      -1
Last checked:             Tue Feb  4 23:38:21 2014
Check interval:           0 (<none>)
Lifetime writes:          814 MB
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
First inode:              11
Inode size:               256
Required extra isize:     28
Desired extra isize:      28
Journal inode:            8
Default directory hash:   half_md4
Directory Hash Seed:      21a3ffda-3d91-4393-b173-60a625eae109
Journal backup:           inode blocks
</pre>
</li>

<br/>

<li>
Disable transparent hugepage support <br/>
<code>
# egrep 'trans|thp' /proc/vmstat
<code> <br/>
<p>Result: It has been disabled</p>
<pre>
nr_anon_transparent_hugepages 0
thp_fault_alloc 0
thp_fault_fallback 0
thp_collapse_alloc 0
thp_collapse_alloc_failed 0
thp_split 0
</pre>
</li>

<br/>

<li>
List your network interface configuration <br/>
<code># ifconfig </code> <br/>
<pre>
eth0      Link encap:Ethernet  HWaddr 06:FA:FA:A0:02:F2  
          inet addr:172.31.7.124  Bcast:172.31.15.255  Mask:255.255.240.0
          inet6 addr: fe80::4fa:faff:fea0:2f2/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1120 errors:0 dropped:0 overruns:0 frame:0
          TX packets:999 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000 
          RX bytes:114824 (112.1 KiB)  TX bytes:169915 (165.9 KiB)
          Interrupt:24 

lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0 
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

</pre>

</li>

<br/>

<li>
forward and reverse host lookups are correctly resolved <br/>
Command: <code># nslookup</code><br/>
<p>Result: </p>
<pre>
> ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Address: 172.31.7.124
> ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Address: 172.31.7.124
> ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Address: 172.31.7.124
> ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Address: 172.31.7.124
> ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-54-219-134-223.us-west-1.compute.amazonaws.com
Address: 172.31.7.124
</pre>
</li>

<br/>

<li>
Show the nscd service is running <br/>
<code>
# service nscd status
</code><br/>
nscd (pid 4516) is running...
</li>

<br/>

<li>
Show the ntpd service is running <br/>
<code> 
# service ntpd status
</code>
<br/>
ntpd (pid  4593) is running...
</li>

<li>
Commands Notes: Initialize the server
<ul>
<li><code>sysctl vm.swappiness=1</code></li>
<li><code>resize2fs /dev/xvde</code></li>
<li>Network: <code>setenforce 0</code></li>
<li><code>service iptables stop</code></li>
<li>Nscd: <code>yum install nscd</code></li>
<li><code>service nscd start</code></li>
<li>Ntpd: <code>yum install ntp</code></li>
<li><code>service ntpd start</code></li>
<li>MySQL Connector:<code>mkdir -p /usr/share/java</code></li>
<li><code>cd /usr/share/java</code></li>
<li><code>ln -s mysql-connector-java-5.1.42-bin.jar mysql-connector-java.jar</code></li>

</li>

</ol>





