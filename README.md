### On Windows - 

Control Panel\Programs\Programs and Features - Turn windows features on or off - Check Telnet Client

C:\Users\anup.mondal>telnet towel.blinkenlights.nl

__On CentOS  —__

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

__On Ubuntu  —__   

__Installation  —__   

anup@megatron:~$ sudo apt-get update  

anup@megatron:~$ sudo apt-get install telnetd  

__Telnet service  —__  

anup@megatron:~$ sudo systemctl status inetd  

anup@megatron:~$ telnet localhost  
