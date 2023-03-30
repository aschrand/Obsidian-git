---
source: 
created: 2023-02-27
type: cheatsheet
---

If we want to run a quick scan of machines in our network without trying to see if any port is open, we run:
nmap -sn 192.168.1.0/24

More verbose with additional info:
nmap -O -v 192.168.1.0/24