---
title: "Network Analysis"
excerpt: "My final project in Network Analysis at Hocking College"
collection: portfolio
---


# Network Traffic Analysis Report

## Executive Summary

  
  Throughout the four PCAPs there were different attacks, such as port scanning and DDoS, as well as some potential policy violations. Some of these attacks were perpetrated from an external source while others were completed from an internal source. 
  
  DDos attacks are arguably the most dangerous of them all, this attack uses a botnet to repeatedly send a lot of false traffic to a network, overwhelming its systems and causing the network to malfunction while also potentially allowing the attacker to send traffic through a now malfunctioning security system. Port scanning is ultimately less malicious, more of an exploratory attack that should be monitored. This attack sees people sending traffic to multiple different ports, testing which one is open, if any, and then further exploiting the open port.

  In the case of a DDoS attack, it is best to simply shut down the server that is being attacked so it cannot be further exploited, and then reconfigured to fix whatever issue was wrong with it, unfortunately, keeping it open can cause the attacker to gain access to potentially very private information, as such shutting it down it best. Port scanning is a different story, figuring out what port is open is a valuable asset, constant monitoring of the threat is helpful, and when the attacker does find an open port, shut it down. 

## Network Environment Overview
	
  In the captures, both internal and external traffic is used. Primarily, internal traffic is used in the case of a policy violation as more often than not, an employee will not be orchestrating a DDoS attack on the servers they manage, though I suppose it can happen. External traffic is where you see the majority of malicious traffic such as port scanning, DDoS, and other attacks.

  There are numerous different devices. From endpoint computers to cloud servers. Most of the DDoS attacks are attacking servers to webservices, which shuts down the service, causing a loss of business. 

  Typical traffic sees endpoint devices connecting to one another or a server via a protocol and a port, in the case of the TCP protocol a TCP handshake is accomplished before access is granted, which can take some time before accomplishing or even be interrupted due to connection issues. Other major protocols include HTTP, UDP, NDMS, and DNS.

## Baseline Traffic Analysis

  As mentioned, major protocols include TCP, HTTP, and NDMS. NDMS is responsible for data transfer from primary to secondary storage devices as such, there is not much that can be expected out of this protocol and it is not typically used in any attacks. 
  
  TCP traffic is responsible for primarily handling email and data transfer from endpoint to endpoint in a secure method. The TCP handshake ensures a stable connection between the two, and ensures that they are ready to send and receive transmissions. TCP is mainly used in DDoS and port scanning attacks as it is an easy to send, easy to falsify protocol that can be sent in rapid succession.
  
  HTTP traffic is responsible for the world wide web, without it, we would not have internet access like we do today. This protocol allows transfer of hypermedia documents between client and server. HTTP can also be used to download files to a server and can be used to install malicious files that can run shell scripts. 

## Identified Anomalies or Malicious Activity
   
  In the packets, as mentioned, there were numerous different attacks, including DDoS, port scanning, and potentially an on-path attack. We have, in some instances, a lot of TCP packets being sent to a singular IP address, which is a tell-tale sign of DDoS followed by some traffic being allowed to go through that would otherwise be filtered and blocked. We also have a repeated attempt to access an IP address via multiple different ports, and multiple source ports as well in some cases. The man in the middle attack is a maybe as there were instances of TCP ACK duplication which could be a sign that the handshake is seeing an additional party, however I do not know much about man in the middle attacks to make a firm case on this. 
  
  This of course is all concerning, all are attacks and all can be detrimental to the day to day functions of a business, the most dangerous of these however are DDoS and on-path infiltration. DDoS can completely halt business operations by disabling the normal functions of a server, and an on-path attack, if unnoticed, can cause you to accidentally leak confidential business information, and you would have no idea it occurred.

## Evidence and Indicators

  In the case of the DDoS attack, it was fairly obvious, hundreds of TCP packets with no ACK to complete the handshake were being sent to a single IP address, likely the server, and in between the sending of these TCP packets, HTTP requests were sent to access illicit websites.It is likely that the overflow of the TCP packets caused the server to not be able to catch the requests in its security protocols due to the attack.
  
  The port scanning attack too was fairly easy to catch, a specific IP was sending dozens of TCP requests to different ports to another IP, including some known, common ports as well as some high end, rarely used ports as well. 
  
  The on-path attack is a strange one compared to the other two. Two devices are communicating with each other, focusing primarily on IP address 10.5.31.182, and every now and again the system simply creates duplicate TCP packets and does nothing with them, which I find strange enough. This occurs later with the exact same IP address communicating with a different IP address, which leads me to believe that this computer is infected and should be disconnected and analyzed for any malicious activity.

## Analyst Assessment and Recommendation
  
  As with everything, you should take proper caution and follow protocol as best you can when dealing with any issue, document how the attack happened, what were its entrance points, how can you avoid it, followed promptly by eradication. 
  
  In the case of the port scanning and the DDoS attack, these are confirmed attacks, all of the patterns are there and there is not a doubt in my mind. The first steps in the DDoS attack would be removing the access of the attacker, seeing as they are manipulating the system to gain access to websites that they should otherwise not have access to. After that it is a matter of filling in the hows and whys. The port scanning attack is similar, figure out what port is open, and close it. There is no entrance point in this case as it would be the, now closed, port. This of course should still be monitored.
  
  With the on-path attack, I cannot say it is a confirmed attack, however it certainly appears to be malicious in nature. Monitoring the traffic, especially from the previously mentioned IP address would be necessary, potentially commandeering the end device in order to avoid any confidential information from being leaked during the course of the investigation as well as an analysis of the computer for any hidden malware. 
