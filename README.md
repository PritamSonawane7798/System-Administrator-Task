# System-Administraror-Task

### Create new user with a non-interactive shell
```
adduser kirsty  -s /sbin/nologin
```

### Change datetime on linux server
```
date -s "2 OCT 2006 18:00:00"
```
### Create banner for linux login
```
1. create file banner
'####################################################################################
				WELCOME TO APP SERVER
####################################################################################
2. sudo mv banner /etc/motd
```
### linux authentication create passwordless authentication from jump server to all application server
```
1. ssh to jump server
2. ssh-keygen -t rsa
enter blanks on passphrase
3. ssh-copy-id  tony@stapp01
4. ssh tony@stapp01
```
### NTP server: The Network Time Protocol is a networking protocol for clock synchronization between computer systems over packet-switched,
 variable-latency data networks
 - Install and configure NTP server on App Server
 ```
 yum install -y ntp
 ```
 - Add NTP server in configuration file 
 ```
 vi /etc/ntp.conf
 replace server details and check by following command
 cat /etc/ntp.conf |grep sg.pool
 ```
 - Check NTP daemon status  
 ```
 systemctl status ntpd
 ```
 - NTP daemon enable and check the status 
 ```
 systemctl enable ntpd
 systemctl start  ntpd
 systemctl status ntpd
 ```
 ### a. Delete all lines containing word copyright and save results in /home/BSD_DELETE.txt file. (Please be aware of case sensitivity)

### b. Replace all occurrence of word the to for and save results in /home/BSD_REPLACE.txt file.
```
1  cat /home/BSD.txt |grep copyright
2  sed '/\<copyright\>/d' /home/BSD.txt > /home/BSD_DELETE.txt
3  cat /home/BSD_DELETE.txt |grep copyright
4  cat /home/BSD.txt |grep the
5  cat /home/BSD.txt |grep  the 
6  sed 's/\bthe\b/for/g' /home/BSD.txt > /home/BSD_REPLACE.txt
7  cat /home/BSD_REPLACE.txt |grep  the
```
 
 
