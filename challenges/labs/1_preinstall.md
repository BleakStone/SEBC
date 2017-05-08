<h1>Challenge 1</h1>

<ol>
<li> Check vm.swappiness on all your nodes  
<code>
# sysctl vm.swappiness  <br />
vm.swappiness = 60  
# sysctl vm.swappiness=1  
vm.swappiness = 1
</code>
</li>


<li>
Show the mount attributes of your volume(s) <br/>
<code>
# cat /proc/mounts  
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
</code>
</li>

</ol>
