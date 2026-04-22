Nmap Lab  

Purpose  
This lab shows different Nmap scans against legal targets (scanme.nmap.org) and localhost. It demonstrates basic scanning, OS detection, service/version detection, and running NSE scripts.  

What I did / learned  
- Ran basic and aggressive Nmap scans to find open ports and services  
- Used OS detection and version detection to learn about hosts  
- Tried NSE (Nmap Scripting Engine) scripts to gather extra information  
- Practiced scanning only allowed/legal targets like scanme.nmap.org and my lab hosts  

Tools I used  
- Nmap (CLI)  
- Zenmap (GUI mode)  
- Kali Linux (attacker VM)  

Example Nmap commands used  
- Simple port scan:  
  nmap scanme.nmap.org = scans common ports to find open services  

- TCP SYN (fast) scan:  
  nmap -sS scanme.nmap.org = performs a fast, stealthy SYN scan  

- OS detection + version detection:  
  nmap -A scanme.nmap.org = detects OS, service versions, and runs default scripts  

- Aggressive scan with service/version detection:  
  nmap -sS -sV -O scanme.nmap.org = SYN scan with service version and OS detection  

- Run NSE scripts (example):  
  nmap --script vuln scanme.nmap.org = runs vulnerability detection scripts  

Safety / Rules  
I only scanned targets that are allowed for testing, such as scanme.nmap.org and my own lab machines. I did not scan random external systems without permission.  

What I learned (SOC perspective)  
- A high number of SYN packets with little response can indicate scanning activity  
- Scans reveal open ports and services that should be monitored and secured  
- IDS/monitoring tools can help detect unusual scanning patterns  

How I did the lab  
- Started Kali Linux VM  
- Ran the Nmap commands listed above on scanme.nmap.org and local lab targets  
- Saved the output and screenshots in the repository folder  

Notes  
The output and screenshots are included in the repo for reference.  
