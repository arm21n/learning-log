# learning-log
day-to-day updates from my cybersecurity studying sessions
- - -
## Day 1 - Setup
- Installed VirtualBox + Kali Linux, fixed a Windows defender false-positive block on the download
- Got Guest Additions working (had a few case-sensitivity errors along the way - Linus is case-sensitive!)
- Learned basic terminal commands: 'ls', 'cd', 'pwd', 'mkdir', 'rm', 'rm -r', 'cp', 'mv'
- Ran my first 'nmap' scan on localhost - all ports closed (as expected on a fresh system)
- Started a Python HTTP server on port 8080, scanned it again, watched 'nmap' detect the open port
- Practiced 'chmod' by locking myself out of my own file, then fixing it
- Ran my first MD5 hash with 'md5sum' and saw how a tiny input change completely changes the output
- Completed 4 rooms on TryHackMe's Pre Security path
- Thought of a handle: **0xdomm**
- - -
# Day 2 — Networking Refresher Notes
*From TCM's Practical Ethical Hacking course (00:00–1:04:39)*
## Effective Note-Keeping
TCM uses KeepNote. Alternatives I'm considering:
- CherryTree
- OneNote
- Joplin
## Important Tools
Downloaded and learned GreenShot + KeepNote to start taking notes.
## Networking Refresher: Introduction
**IP Addressing**
- `ifconfig` — command to view IP info
- IPv4 vs IPv6
- NAT (Network Address Translation)
- Private IP classes:
  - Class A — huge networks (e.g. `10.x.x.x`), millions of addresses, used by large orgs
  - Class C — small networks (e.g. `192.168.x.x`), ~254 addresses, used for personal/home use
- Operates at **Layer 3** (Router)
- Subnetting — dividing a network into smaller sub-networks
**MAC Addresses**
- Media Access Control — physical hardware identifier
- Operates at **Layer 2** (Switching)
- Every NIC (Network Interface Card) gets a MAC address when installed
- First 3 pairs = manufacturer/device identifier
**TCP, UDP, & the Three-Way Handshake**
- Operates at **Layer 4** (Transport)
- **TCP** — connection-oriented, high reliability
- **UDP** — connectionless, faster but less reliable
- Three-way handshake (how a connection is established):
  `SYN → SYN-ACK → ACK`
## Common Ports & Protocols
**TCP**
| Port | Protocol | Purpose |
|------|----------|---------|
| 21 | FTP | File Transfer Protocol |
| 22 | SSH | Encrypted remote login (secure version of Telnet) |
| 23 | Telnet | Remote login, unencrypted |
| 25 | SMTP | Sending mail |
| 110 | POP3 | Receiving mail |
| 143 | IMAP | Receiving mail (syncs across devices) |
| 53 | DNS | Resolves IP addresses to domain names |
| 80 | HTTP | Website traffic, unencrypted |
| 443 | HTTPS | Website traffic, encrypted |
| 139/445 | SMB | File shares — common target for pentesters |
**UDP**
| Port | Protocol | Purpose |
|------|----------|---------|
| 53 | DNS | Same as above, but UDP |
| 67/68 | DHCP | Assigns temporary IPs, refreshed periodically |
| 69 | TFTP | Simplified version of FTP |
| 161 | SNMP | Simple Network Management Protocol — monitors/manages network devices remotely, uses a "community string" as a weak auth mechanism |
---
**Note:** TryHackMe Pre Security path still locked behind premium — continuing with TCM's free course instead.
