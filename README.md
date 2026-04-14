# eJPT Penetration Testing Lab Writeups

**Author:** Showrya Boga  
**Platform:** INE  
**Tool:** Kali Linux + Metasploit Framework  

---

## Labs Overview

### Lab 1 — System-Host Based Attacks CTF 1
- **Targets:** Windows (IIS + SMB)
- **Key Vulnerability:** WebDAV + SMB Brute-Force
- **Flags:** 4

### Lab 2 — System-Host Based Attacks CTF 2
- **Targets:** Linux (Apache + SSH)
- **Key Vulnerability:** Shellshock + libssh Authentication Bypass
- **Flags:** 4

### Lab 3 — Metasploit Framework CTF 1
- **Targets:** Windows (MSSQL 2012)
- **Key Vulnerability:** MSSQL CLR Payload + Privilege Escalation
- **Flags:** 4

### Lab 4 — Metasploit Framework CTF 2
- **Targets:** Linux (RSYNC + Roxy-WI Web App)
- **Key Vulnerability:** RSYNC Enumeration + Unauthenticated RCE
- **Flags:** 4

---

## Methodology (Applied Across All Labs)

1. **Host Discovery** — Ping sweep to confirm target is alive
2. **Port Scanning** — `nmap -sV -p-` to identify open ports and service versions
3. **Exploitation** — Metasploit modules or manual tools based on findings
4. **Post-Exploitation** — Shell access, privilege escalation, flag retrieval

---

## Tools Used

- `Nmap` — Port scanning and service enumeration
- `Metasploit Framework` — Exploitation and post-exploitation
- `crackmapexec` — SMB brute-forcing
- `smbclient` / `enum4linux` — SMB share enumeration
- `cadaver` — WebDAV file upload
- `rsync` — RSYNC module enumeration
- `netcat` — Reverse shell listener

---

## Flags Summary (16 Total)

### Lab 1 — Windows CTF 1
- **Flag 1** — Found in WebDAV share (`/webdav/flag1.txt`)
- **Flag 2** — Found on `C:\` drive via ASP webshell RCE
- **Flag 3** — Retrieved via SMB brute-force on target2
- **Flag 4** — Found in `C:\Users\Administrator\Desktop\`

### Lab 2 — Linux CTF 2
- **Flag 1** — Found in `/` directory after Shellshock exploit
- **Flag 2** — Hidden file in `/opt/apache/htdocs/`
- **Flag 3** — Found in `/home/user/` via libssh auth bypass
- **Flag 4** — Found in `/root/` after SUID privilege escalation

### Lab 3 — Metasploit CTF 1
- **Flag 1** — Found in `C:\` after MSSQL shell access
- **Flag 2** — Found in `C:\Windows\System32\config\`
- **Flag 3** — Found in `C:\Windows\System32\drivers\etc\`
- **Flag 4** — Found in `C:\Users\Administrator\Desktop\`

### Lab 4 — Metasploit CTF 2
- **Flag 1** — Found in RSYNC banner (target1)
- **Flag 2** — Found inside RSYNC module backup files
- **Flag 3** — Retrieved after Roxy-WI RCE exploit (target2)
- **Flag 4** — Found inside `/etc/cron.d/` scheduled job file

---

> These labs were completed as part of eJPT exam preparation on the INE platform.
