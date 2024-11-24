# DAY 2
## Network Security NAT and Firewalls
- NAT-share intrrnet from one nic to another nic
- Network Address Translation 
- NAT converts between private(internal) IP address and one or more public-facing (external) address

## IP Address Translation
* private IP address space in the organization
    * One external IP address,multiple internal address

* NAT - Translation Table
    * Map source address:port in outgoing IP requests to a unique external address:port 
    * Inverse mapping for incoming requests
* A NAT-enabled router looks like a single device with one IP address


## Private Address 
* We cannot use IP address of valid external hosts locally 
    how will we dinsinguish local vs.external hosts? 

* RFC 1918: Address Allocation for private internets 
    * Defines unregisterd,non-routable address for internal networks

# Private IP Address Ranges

The table below lists the private IP address ranges, the number of addresses within each range, and their corresponding CIDR notation.

| Address Range            | Number of Addresses | IP Address Block |
|--------------------------|---------------------|------------------|
| 10.0.0.0 - 10.255.255.255 | 16,777,216         | 10.0.0.0/8       |
| 172.16.0.0 - 172.31.255.255 | 1,048,576         | 172.16.0.0/12    |
| 192.168.0.0 - 192.168.255.255 | 65,536           | 192.168.0.0/16   |

These ranges are reserved for private networks and are defined by [RFC 1918](https://datatracker.ietf.org/doc/html/rfc1918).

## Advantages of NAT 
* Internal address space can be mch larger than the addresses allocated by the ISP 
* No need to change internal addresses if ISP changes your address
* Enhanced security 
    * A computer on an external network cannot contact an internal computer\
        \...unless the internal computer initiated the communication  
      Even then- it can only contact the computer on that specific port


# Firewalls
## Network Security Goals
* Confidentiality: sensitive data 
* .
* .
## Firewall 
* Separate your local Network form the internet
    * Protect the border between trusted internal networks and the untrusted internet 

### Approaches 
* Packet filters
* Application proxies 
* Intrusion detection / Intrusion protection systems

## First Generation Firewalls:
### Packet filters
* **Border router (gateway router)**
    * router between the internal networks and external networks
    * Any traffic between internal and external networks passes through the border router

* **Screen router = packet filter**
    * Allow or deny packets based on 
        * incoming and outgoing interfaces 
        * Sources and destination IP addresses 
        * Protocol (e.g, TCP,UDP,ICMP,IGMP,RDVP,etc.)
        * Source and destination TCP/UDP ports, ICMP command

* **Filter Chaining** 
    * An IP packet entering a router in matche against a set of rules: access control list(ACL) or chain 

    * Each rule contains criteria and an action 
        * Criteria: Packet screening rule 
        * Actions: 
            * Accpet-and stop processing additional rules
            * Drop-discard the packet and stop processing additional rules 
            * Reject-and send an error to the sender (ICMP destination Unreachable) 

            Also
            * Route-route packets
            * Nat-perform network address transiation 
            * Log-record the activity

what is internet and intranet


* **Network Ingress Filtering: incoming packets**
* Basic firewalling principle 
    * **No direct inbound connections from external systems (Internet) to any internal host -all traffic must flow through a firewall and be inspected** 

    * Determine which services you want to expose to the internet 
    * Create a list of services and allow only inbound ports and protocols to the machines hosting the services 
        * Examples
            * Web Server: 10.0.0.10 TCP port 80, TCP port 443
            * Mail Server: 10.0.0.12 TCP port 587

    * **Default Deny** Model - by default,deny all 
        * Anything not specifically permitted is dropped 
        * May want to log denies to identify who is attempting access

* **Network Engress Filtering(Outbound)**
    * Usually, we don't worry about Outbound traffic 
        * Communication form a higher security network (internal) to a lower security netowrk (internet) is usually fine 

    * Why might we want to restrict it?
        * Consider: if a computer is compromised and all outbound traffic is allowed,it can connect to an external server and download more malicious code
                
            \... or launch a DoS attack on the internal network 
        * Also,log which servers are trying to access external addresses
     
   

## Server Machine: 
* IP : 192.168.206.134
* GW : 192.168.206.2
* DNS : 192.168.206.2


nmtui-network manager text mode interface
TUI

Edit a connection
select the interface ens32

Once you added the connection activate the connection deactivated the connection and activated again

* On Server machine
    * imtui 
    * ifconfig ens33
    * route -n 
    * cat /etc/resolv.conf
    * host google.com 


both machine are connected in nat adapter

on client machine
sudo dhclient -r
sudo dhclient -to assign the dhcp ip agian

daemon -> service 


Firewalld & Firewall-cmd:

##  Configuration
* RunTime
* Permanent

## MUST BE ACTIVATED
* systemctl status firewalld
* systemctl start firewall
* firewall-cmd --get-zones

## [THEY ALL HAVE PREDEFINED SET OF RULES]

1. **block** 

	[All incoming conn are rejected & only outgoing conn are allowed]

2. **dmz** 

	[Used for systems located in Demilitarized zone, only selected incoming conn are allowed in this zone]

3. **drop** 

	[All incoming conn are dropped without notify, only outgoing conn are allowed]

4. **external** 

	[Used for external networks with NAT masquerading enabled when our syatem acts as a gateway or router, here only selected incoming conn are allowed]

5. **home** 

	[Other systems in n/w are generally trusted and only selected incoming conn are allowed]

6. **internal** 

	[Used in internal network when your system acts as gateway or router, select incoming conn are alllowed]

7. **public** 

	[Used for the untrusted public areas, do not trust other systems on the network but you can allow selected incoming conn]

8. **trusted**

	[All n/w conn are accepted]

9. **work**

	[All systems in n/w generally trusted and only selected incoming conn are allowed]






Which is the default zone:
```bash 
firewall-cmd --get-default-zone
```



What are the rules for the default zone:
```bash 
firewall-cmd --list-all
```






If you want to see the rule for other zones:
```bash 
firewall-cmd --zone=dmz --list-all
```









If you want to connect the inetrface to 'dmz' from 'public', then the interface will move from 'public' to 'dmz' & and 'dmz' will active:
```bash 
firewall-cmd --zone=dmz --change-interface=ens33
firewall-cmd --zone=dmz --add-interface=ens33 
```
[will only change for runtime]



```bash 
firewall-cmd --zone=public --list-all [To check]
firewall-cmd --zone=dmz --list-all [To check]
```
If you reload the firewall and check the 'dmz', interface will set back to 'public' zone, because of the 'realtime' changes:
```bash 
firewall-cmd --reload
firewall-cmd --zone=dmz --list-all [To check]
firewall-cmd --list-all [To check]
```

To make it permanent 
```bash 
firewall-cmd --zone=dmz --change-interface=ens160 --permanent
firewall-cmd --reload
```
To check all the services to add in 'public' zone:
```bash 
firewall-cmd --get-services
```

NOTE: All the services have their individual XML files, are located /usr/lib/firewalld/services

If you want to deny access of SSH on the machine, so you just need to remove SSH service from the public(or current) zone:
```bash 
firewall-cmd --zone=public --remove-service=ssh --permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```

To add any service:
```bash 
firewall-cmd --zone=public --add-service=ssh --permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```
To remove port number:
```bash 
firewall-cmd --zone=public --remove-port=8080/tcp
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```

To add port number
```bash 
firewall-cmd --zone=public --add-port=2020/tcp --permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-all
```


