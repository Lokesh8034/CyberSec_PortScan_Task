# Network Port Scan Task

## Overview
This repository contains the results and notes from a local network port scanning task using Nmap.

## Steps Performed
1. Installed Nmap on local machine.
2. Discovered local IP range using `ipconfig` / `ifconfig`.
3. Performed TCP SYN scan on local network range.
4. Analyzed open ports and services running on discovered hosts.
5. (Optional) Captured packets during scan with Wireshark to understand SYN scan behavior.
6. Researched common services for open ports found.
7. Identified potential security risks from open ports.
8. Saved scan results in text format.

## Scan Results
| IP Address | MAC Address | Open Ports | Services	| Notes |
|------------|-------------|------------|-----------|-------|
| 10.x.x.x	| 52:54:xx:xx:xx:xx (QEMU)	| 53	| domain (DNS) |	DNS service likely running |
| 10.x.x.x	| 52:54:xx:xx:xx:xx (QEMU)	| 135, 445 |	msrpc, microsoft-ds |	Possibly Windows host or SMB share |
| 10.x.x.x	| 08:00:xx:xx:xx:xx (VirtualBox) |	None	| - |	All 1000 ports filtered |
| 10.x.x.x	| - |	None	| _ | All 1000 ports closed |

## Key Learnings
- Understanding open ports and what they imply.
- How TCP SYN scan works.
- Security risks of exposed services.
- Role of firewall in protecting open ports.

## Tools Used
- Nmap
