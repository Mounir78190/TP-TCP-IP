# Lab: TCP/IP

### Table of Contents
1. Introduction
2. List of Performed Tasks
3. Issues Encountered and Solutions
4. Theoretical Analysis
5. Conclusion
6. Resources
7. Quiz

## 1. Introduction :

This lab focuses on the practical understanding of TCP/IP and UDP protocols in modern networks. The main objectives are to demonstrate configuration, troubleshooting, and analysis of communication protocols, including complementary protocols such as DHCP and ARP. This README serves as a reference for reproducing exercises and solving encountered issues.

## 2. List of Performed Tasks :

###
1. Creating Three Routers on Cisco :

* IP Addressing for Interface 0/0:
    * AD: IPv4: 192.168.1.1, Mask: 255.255.255.0
  ![image Ip-AD.](https://imgur.com/howwJE7.png)

    * TECH: IPv4: 192.168.2.1, Mask: 255.255.255.0
   ![image Ip-TECH.](https://imgur.com/079TEXS.png)

    * COMM : Ipv4 : 192.168.3.1, Mask 255.255.255.0
  ![image Ip-COMM.](https://imgur.com/BDoixxy.png)

* IP Addressing for Interface 0/1:
    * AD : Ipv4 : 10.0.0.1, Mask 255.255.255.0
  ![image Ip-AD.](https://imgur.com/Ddp01iO.png)

    * TECH : Ipv4 : 10.0.0.2, Mask 255.255.255.0
   ![image Ip-TECH.](https://imgur.com/aRuP0c3.png)

    * COMM : Ipv4 : 10.0.0.3, Mask 255.255.255.0
  ![image Ip-COMM.](https://imgur.com/sZl2oUi.png)


2. Connecting Routers Through a Switch
  
3. Creating Three Servers for Administrative, Commercial, and Technical Subnets

* Server IP Addressing:
    * AD-SRV: IPv4: 192.168.1.10, Mask: 255.255.255.0, Gateway: 192.168.1.1, DNS: 8.8.8.8
  ![image Ip-AD-SRV.](https://imgur.com/Ots3yrw.png)

    * TECH-SRV: IPv4: 192.168.2.10, Mask: 255.255.255.0, Gateway: 192.168.2.1, DNS: 8.8.8.8
  ![image Ip-TECH-SRV.](https://imgur.com/pmkclIC.png)

    * COMM-SRV: IPv4: 192.168.3.10, Mask: 255.255.255.0, Gateway: 192.168.3.1, DNS: 8.8.8.8
  ![image Ip-COMM-SRV.](https://imgur.com/1jYf489.png)

4. Creating Three Client PCs for Each Subnet with Proper Addressing

    ![image Architecture.](https://imgur.com/aH3JqG4.png)

* PC IP Addressing:
    * AD-CLI: IPv4: 192.168.1.100, Mask: 255.255.255.0, Gateway: 192.168.1.1, DNS: 8.8.8.8
  ![image Ip-AD-SRV.](https://imgur.com/Cl42WYe.png)

    * TECH-CLI: IPv4: 192.168.2.100, Mask: 255.255.255.0, Gateway: 192.168.2.1, DNS: 8.8.8.8
  ![image Ip-TECH-SRV.](https://imgur.com/ix6xobA.png)

    * COMM-CLI: IPv4: 192.168.3.100, Mask: 255.255.255.0, Gateway: 192.168.3.1, DNS: 8.8.8.8
  ![image Ip-COMM-SRV.](https://imgur.com/SWqWWGg.png)

5. Network Performance Analysis Using Cisco Simulator

![Analyse des Preformances.](https://imgur.com/TZNaNsL.png)

6. Comparative Study: TCP vs. UDP in a Simulated Environment

* Packet Transmission Simulation with TCP:
    * Performance analysis after filtering TCP packets and selecting the server address
![Analyse des Preformances TCP.](https://imgur.com/nrZV1dv.png)
![Analyse des Preformances TCP.](https://imgur.com/rNUl3yj.png)

* Packet Transmission Simulation with UDP:
    * Performance analysis after configuring a traffic generator
  ![Config trafic.](https://imgur.com/G7JSHMS.png)
  ![Analyse des performences UDP](https://imgur.com/TAoRptv.png) 

   
## 3. Issues Encountered and Solutions

### Issue 1: IP Address Conflict
* Description: IP address conflict error when configuring a static IP.
* Solution: Checked the network for other devices using the same IP address and reconfigured it with an available address.
  
### Issue 2: No Wireshark for Packet Capture
* Description: Unable to use Wireshark on Cisco.
* Solution: Used Cisco’s network simulator, which provides a visual representation of packet behavior.

## 4. Theoretical Analysis

The TCP/IP protocol is fundamental for modern networks, enabling interoperability between different systems.
* TCP ensures reliable, ordered transmission with error control, making it suitable for applications where accuracy is critical, such as web browsing and emails.
* UDP, on the other hand, offers faster, connectionless transmission, making it ideal for real-time applications like video streaming and online gaming.

## 5. Conclusion

This practical lab strengthened our understanding of TCP/IP and UDP protocols, including their configurations and troubleshooting techniques.
Hands-on experience, combined with theoretical knowledge, significantly improved our grasp of network connectivity and performance.

## 6. Resources

Cisco Documentation:
* https://www.netacad.com/resources/lab-downloads?courseLang=en-US
  
TCP/IP Protocol Suite:
* https://tools.ietf.org/html/rfc791,
* https://tools.ietf.org/html/rfc793

## 7. Quiz

1. What is the main difference between TCP and UDP?
  * A. TCP ensures reliability, UDP is faster.

2. Which layer of the TCP/IP model handles packet routing?
  * C. Internet 

3. Which protocol is used to resolve an IP address to a MAC address?
  * C. ARP 

4. What is the size of an IPv6 address?
  * C. 128 bits 

5. Which tool is used to analyze network performance by capturing packets?
  * B. Wireshark 
