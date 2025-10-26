Nmap Lab

Purpose

This lab shows different Nmap scans against legal targets (scanme.nmap.org) and localhost. It demonstrates basic scanning, OS detection, service/version detection, and running NSE scripts.

What I did / learned

- Ran basic and aggressive Nmap scans to find open ports and services.
- Used OS detection and version detection to learn about hosts.
- Tried NSE (Nmap Scripting Engine) scripts to gather extra info.
- Practiced scanning only allowed/legal targets (scanme.nmap.org) and lab hosts.

Tools i used 

- Nmap (CLI)
- zenmap GUI mode
- Kali Linux (attacker VM)

Example Nmap commands used

- Simple port scan:
  nmap scanme.nmap.org
- TCP SYN (fast) scan:
  nmap -sS scanme.nmap.org
- OS detection + version detection:
  nmap -A scanme.nmap.org
- Aggressive scan with service/version detection:
  nmap -sS -sV -O scanme.nmap.org
- Run NSE scripts (example):
  nmap --script vuln scanme.nmap.org

Safety / Rules

- Only scan targets you own or are allowed to scan (scanme.nmap.org is allowed for practice).
- Do not scan random internet hosts without permission.

Quick SOC takeaways

- Many SYN packets with few responses usually mean scanning activity.
- Scans reveal open ports and services that defenders should monitor and protect.
- Use IDS/monitoring to detect high SYN rates or new open services.

How to do simple lab

1. Start Kali or another lab VM.
2. Run the Nmap commands above against `scanme.nmap.org` or your lab targets.
3. Save outputs and screenshots to the repo folder.

Notes
- See the README and screenshot of nmap scaning inside the nmap folder.
