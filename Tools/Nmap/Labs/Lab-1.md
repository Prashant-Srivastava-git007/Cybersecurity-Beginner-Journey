# Lab 1 – Host Discovery (Ping Scan)

## 🖥️ Setup:
•	Linux VM + Windows 10 VM running inside VirtualBox.
•	Both should be connected to the same VirtualBox Internal Network / Bridged Adapter so they can see each other.

## 🎯 Goal:
•	Identify live hosts on your LAN (your Linux, Windows, and router should appear).

## ⚡ Commands:

```
nmap -sn <Target-IP> 
```
This will list all the devices connedcted to your network without scaning the port.

> Note if ping (ICMP) is blocked by any device than we can use -Pn flag to scan without sending any ICMP packets.

