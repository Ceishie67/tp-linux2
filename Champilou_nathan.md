# Rendu

## Nathan Champilou ;)

### installation faites sur la machine ;D

## Nginx
```
root@debian:~# sudo apt update
Hit:1 http://deb.debian.org/debian bookworm InRelease
Get:2 http://deb.debian.org/debian bookworm-updates InRelease [55.4 kB]
Get:3 http://security.debian.org/debian-security bookworm-security InRelease [48.0 kB]
Get:4 http://security.debian.org/debian-security bookworm-security/main Sources [130 kB]
Get:5 http://security.debian.org/debian-security bookworm-security/main amd64 Packages [216 kB]
Fetched 450 kB in 0s (1009 kB/s)
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
All packages are up to date.
root@debian:~# sudo apt upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
root@debian:~# sudo apt install nginx
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  nginx-common
Suggested packages:
  fcgiwrap nginx-doc ssl-cert
The following NEW packages will be installed:
  nginx nginx-common
0 upgraded, 2 newly installed, 0 to remove and 0 not upgraded.
Need to get 640 kB of archives.
After this operation, 1696 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://deb.debian.org/debian bookworm/main amd64 nginx-common all 1.22.1-9 [112 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 nginx amd64 1.22.1-9 [527 kB]
Fetched 640 kB in 0s (6877 kB/s)
Preconfiguring packages ...
Selecting previously unselected package nginx-common.
(Reading database ... 37496 files and directories currently installed.)
Preparing to unpack .../nginx-common_1.22.1-9_all.deb ...
Unpacking nginx-common (1.22.1-9) ...
Selecting previously unselected package nginx.
Preparing to unpack .../nginx_1.22.1-9_amd64.deb ...
Unpacking nginx (1.22.1-9) ...
Setting up nginx-common (1.22.1-9) ...
Created symlink /etc/systemd/system/multi-user.target.wants/nginx.service -> /lib/systemd/system/nginx.service.
Setting up nginx (1.22.1-9) ...
Upgrading binary: nginx.
Processing triggers for man-db (2.11.2-2) ...
```

## UFW

```
root@debian:~# apt install -y ufw
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  iptables libip6tc2 libnetfilter-conntrack3 libnfnetlink0
Suggested packages:
  firewalld rsyslog
The following NEW packages will be installed:
  iptables libip6tc2 libnetfilter-conntrack3 libnfnetlink0 ufw
0 upgraded, 5 newly installed, 0 to remove and 0 not upgraded.
Need to get 603 kB of archives.
After this operation, 3606 kB of additional disk space will be used.
Get:1 http://deb.debian.org/debian bookworm/main amd64 libip6tc2 amd64 1.8.9-2 [19.4 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 libnfnetlink0 amd64 1.0.2-2 [15.1 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 libnetfilter-conntrack3 amd64 1.0.9-3 [40.7 kB]
Get:4 http://deb.debian.org/debian bookworm/main amd64 iptables amd64 1.8.9-2 [360 kB]
Get:5 http://deb.debian.org/debian bookworm/main amd64 ufw all 0.36.2-1 [168 kB]
Fetched 603 kB in 0s (6234 kB/s)
Preconfiguring packages ...
Selecting previously unselected package libip6tc2:amd64.
(Reading database ... 37547 files and directories currently installed.)
Preparing to unpack .../libip6tc2_1.8.9-2_amd64.deb ...
Unpacking libip6tc2:amd64 (1.8.9-2) ...
Selecting previously unselected package libnfnetlink0:amd64.
Preparing to unpack .../libnfnetlink0_1.0.2-2_amd64.deb ...
Unpacking libnfnetlink0:amd64 (1.0.2-2) ...
Selecting previously unselected package libnetfilter-conntrack3:amd64.
Preparing to unpack .../libnetfilter-conntrack3_1.0.9-3_amd64.deb ...
Unpacking libnetfilter-conntrack3:amd64 (1.0.9-3) ...
Selecting previously unselected package iptables.
Preparing to unpack .../iptables_1.8.9-2_amd64.deb ...
Unpacking iptables (1.8.9-2) ...
Selecting previously unselected package ufw.
Preparing to unpack .../archives/ufw_0.36.2-1_all.deb ...
Unpacking ufw (0.36.2-1) ...
Setting up libip6tc2:amd64 (1.8.9-2) ...
Setting up libnfnetlink0:amd64 (1.0.2-2) ...
Setting up libnetfilter-conntrack3:amd64 (1.0.9-3) ...
Setting up iptables (1.8.9-2) ...
update-alternatives: using /usr/sbin/iptables-legacy to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-legacy to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/iptables-nft to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-nft to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/arptables-nft to provide /usr/sbin/arptables (arptables) in auto mode
update-alternatives: using /usr/sbin/ebtables-nft to provide /usr/sbin/ebtables (ebtables) in auto mode
Setting up ufw (0.36.2-1) ...

Creating config file /etc/ufw/before.rules with new version

Creating config file /etc/ufw/before6.rules with new version

Creating config file /etc/ufw/after.rules with new version

Creating config file /etc/ufw/after6.rules with new version
Created symlink /etc/systemd/system/multi-user.target.wants/ufw.service -> /lib/systemd/system/ufw.service.
Processing triggers for libc-bin (2.36-9+deb12u9) ...
Processing triggers for man-db (2.11.2-2) ...
```
```
root@debian:~# apt install fail2ban
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  python3-pyinotify python3-systemd whois
Suggested packages:
  mailx system-log-daemon monit sqlite3 python-pyinotify-doc
The following NEW packages will be installed:
  fail2ban python3-pyinotify python3-systemd whois
0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.
Need to get 589 kB of archives.
After this operation, 2901 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://deb.debian.org/debian bookworm/main amd64 fail2ban all 1.0.2-2 [451 kB]
Get:2 http://deb.debian.org/debian bookworm/main amd64 python3-pyinotify all 0.9.6-2 [27.4 kB]
Get:3 http://deb.debian.org/debian bookworm/main amd64 python3-systemd amd64 235-1+b2 [39.3 kB]
Get:4 http://deb.debian.org/debian bookworm/main amd64 whois amd64 5.5.17 [70.8 kB]
Fetched 589 kB in 0s (6173 kB/s)
Selecting previously unselected package fail2ban.
(Reading database ... 37873 files and directories currently installed.)
Preparing to unpack .../fail2ban_1.0.2-2_all.deb ...
Unpacking fail2ban (1.0.2-2) ...
Selecting previously unselected package python3-pyinotify.
Preparing to unpack .../python3-pyinotify_0.9.6-2_all.deb ...
Unpacking python3-pyinotify (0.9.6-2) ...
Selecting previously unselected package python3-systemd.
Preparing to unpack .../python3-systemd_235-1+b2_amd64.deb ...
Unpacking python3-systemd (235-1+b2) ...
Selecting previously unselected package whois.
Preparing to unpack .../whois_5.5.17_amd64.deb ...
Unpacking whois (5.5.17) ...
Setting up whois (5.5.17) ...
Setting up fail2ban (1.0.2-2) ...
Created symlink /etc/systemd/system/multi-user.target.wants/fail2ban.service -> /lib/systemd/system/fail2ban.service.
Setting up python3-pyinotify (0.9.6-2) ...
Setting up python3-systemd (235-1+b2) ...
Processing triggers for man-db (2.11.2-2) ...
```
```
ufw et fail2ban ont été trouvés grâce à des internet voici mes sources :

https://doc.ubuntu-fr.org/ufw

et 

https://doc.ubuntu-fr.org/fail2ban
```

## I firewall (ufw) :D

```
root@debian:~# sudo ufw status
Status: inactive
root@debian:~# ^C
root@debian:~# ufw allow ssh
Rules updated
Rules updated (v6)
root@debian:~# ufw allow 'Nginx Full'
Rules updated
Rules updated (v6)
root@debian:~# ufw enable
Command may disrupt existing ssh connections. Proceed with operation (y|n)? y
Firewall is active and enabled on system startup
root@debian:~# ufw status
Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere
Nginx Full                 ALLOW       Anywhere
22/tcp (v6)                ALLOW       Anywhere (v6)
Nginx Full (v6)            ALLOW       Anywhere (v6)
```

## fail to ban (fail2ban) :)

```
root@debian:~# nano /etc/fail2ban/jail.local
root@debian:~# cat /etc/fail2ban/jail.local
[sshd]
enabled = true
port = ssh
logpath = /var/log/secure
maxretry = 3
root@debian:~#
```