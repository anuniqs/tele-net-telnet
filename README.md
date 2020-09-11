### On Windows - 

Control Panel\Programs\Programs and Features - Turn windows features on or off - Check Telnet Client

C:\Users\anup.mondal>telnet towel.blinkenlights.nl

__On CentOS - __

__Connect internet__

[anup@localhost ~]$ su -  

[root@localhost ~]# dhclient -v  

__Install Telnet - __
[root@localhost ~]# rpm -qa | grep telnet
[root@localhost ~]# yum install telnet-server telnet

Add the service to firewalld - 
[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public
[root@localhost ~]# firewall-cmd --add-service=telnet --zone=public --permanent

Telnet service - 
[root@localhost ~]# systemctl start telnet.socket
[root@localhost ~]# systemctl status telnet.socket
[root@localhost ~]# systemctl restart telnet.socket
[root@localhost ~]# systemctl reload telnet.socket

[root@localhost ~]# systemctl enable telnet.socket
[root@localhost ~]# systemctl disable telnet.socket

[root@localhost ~]# telnet localhost

On Ubuntu - 

Installation - 
anup@megatron:~$ sudo apt-get update
anup@megatron:~$ sudo apt-get install telnetd

Telnet service -
anup@megatron:~$ sudo systemctl status inetd

anup@megatron:~$ telnet localhost
