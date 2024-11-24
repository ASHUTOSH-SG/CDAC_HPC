# Day 3
We can use this attribute to allow or deny a specific system/ip to use the service we have in the current zone 

```bash 
	firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.91.102/32" reject' --permanent 
	firewall-cmd --reload
	firewall-cmd --zone=public --list-all 

```


If you want to allow the IP to use some of these services:

```bash 
	firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.91.102/32" service name="ssh" accept' --permanent 
	firewall-cmd --reload
	firewall-cmd --zone=public --list-all 

```

To reject icmp,tcp and udp  protocol
```bash
firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.206.130/32" protocol value="icmp" reject' permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-all 
```
###  firewall only setup reule for trasport and network protocol it cannot setup rules for application layer protocols

To remove rich rules
```bash
firewall-cmd --zone=public --remove-rich-rule='rule family="ipv4" source address="192.168.16.131/32" service name="ssh" accept' --permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-rich-rules
```


To install apacehe web server 
```bash
dnf install httpd
cd /var/www/html/
cat>index.html
<h1>Web Server for HPCSA</h1>

```

to automate set firewall service
```bash
sudo nano ~/.bashrc 

fireup() 
{
	firewall-cmd --zone=public --add-service="$1" --permanent
	firewall-cmd --reload
}

fireup() 
{
	firewall-cmd --zone=public --remove-service="$1" --permanent
	firewall-cmd --reload
}

source ~/.bashrc

fireup http 
firedown http
```



# Lab Task 1
1.To prevent A form doing telnet to Machine B
* Implementation 
	The following commnad is used to implement the firewall  for the task objective 



```bash 
firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.16.131/32" service name="telnet" reject' --permanent 
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```
# Lab Task:2 

To prevent A form doing SSH to Machine B 
* Implementation

The following commnad is used to implement the firewall for the task objective
must write the firewall-cmd rule command 

* Verification

The Verification is start the ssh from machine A to machine B. The following command is used 

ssh 172.16.0.4

The command result a connection timeout since the tcp packet from machine A to machine B is dropped by the iptables firewall at machine A. 

```bash 
firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.16.131/32" service name="ssh" reject' --permanent 
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```

## NMAP - Network Mapper
```bash
nmap- network mapper 
apt-get install nmap -y
```
### Syntax
```bash      
nmap -<attrib> <target>

targets
192.168.206.100
192.168.206.100 192.168.206.121
192.168.206.100-200
192.168.206.100-200 --exclude 192.168.206.101
192.168.206.0/24
192.168.206.0/24 192.168.10.0/24


domain.tls

-p 80
-p 80,22,9090
-p 80-85

TCP Scan: 
nmap -sT target -p 80,22,9090 --reason 

-s: Scan
-T: TCP Scan


SYN Scan: 

nmap -sS target -p 80,22,9090 --reason
-s: Scan 
-S: SYN Scan


```

# Firewalld bypass by Idle Scan NMAP: 
* Block a Service: 
	* firewalld-cmd --zone=public --add-rich-rule='rule' family="ipv4" source address="192.168.91.102/32" service name="http" drop' --permanent 
	* firewall-cmd --reload 


* Nmap idle scan: 
	* nmap -sI zombinehost x.x.x.x -p 80 --reason 



