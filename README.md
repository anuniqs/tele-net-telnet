### On Windows — 

Control Panel\Programs\Programs and Features - Turn windows features on or off - Check Telnet Client

C:\Users\anup.mondal>telnet towel.blinkenlights.nl


  
### On CentOS  —

__Connect internet__

[anup@localhost ~]$ su -  

[root@localhost ~]# dhclient -v  


__Install Telnet  —__  

[root@localhost ~]# rpm -qa | grep telnet  

[root@localhost ~]# yum install telnet-server telnet  


__Add the service to firewalld  —__    

[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public  

[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public --permanent  


__Telnet service  —__  

[root@localhost ~]# systemctl start telnet.socket  

[root@localhost ~]# systemctl status telnet.socket  

[root@localhost ~]# systemctl restart telnet.socket  

[root@localhost ~]# systemctl reload telnet.socket  

[root@localhost ~]# systemctl enable telnet.socket  

[root@localhost ~]# systemctl disable telnet.socket  


__Try Telnet —__  

[root@localhost ~]# telnet localhost  


  
### On Ubuntu  —   

__Installation  —__   

anup@megatron:~$ sudo apt-get update  

anup@megatron:~$ sudo apt-get install telnetd  


__Telnet service  —__  

anup@megatron:~$ sudo systemctl status inetd  


__Try Telnet —__

anup@megatron:~$ telnet localhost  



### On RedHat  —

[root@localhost ~]# rpm -ivh telnet-0.17-64.el7.x86_64.rpm

[root@localhost ~]# rpm -ivh telnet-server-0.17-64.el7.x86_64.rpm

[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public

[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public --permanent

[root@localhost ~]# systemctl start telnet.socket

[root@localhost ~]# systemctl enable telnet.socket

[root@localhost ~]# ip a

[root@localhost ~]# telnet localhost
