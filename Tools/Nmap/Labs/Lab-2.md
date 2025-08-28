# Lab 2 – TCP Connect vs. SYN Scan

## 🖥️ Setup:
•	Linux scans Windows 10 machine

## 🎯 Goal:
•	Notice **same open ports**, but **speed + technique differs**.


## ⚡ Commands:

```
TCP Connetct - nmap -sT <Target-IP>
```

### 🕵️‍♀️ Observation 

> It commplete full 3 Way Handshake to scan the open port of taget which can be easiy detected by any firewall or IDS present and also it take less time.

```
SYN Scan - nmap -sS <Target-IP>
```

### 🕵️‍♀️ Observation

> It did not compelte the full 3 Way handshake here first the SYN packet is sent then when it recieved the SYN+ACK which means port is opened it immideatily sent a RST which make it more stealthy. 
