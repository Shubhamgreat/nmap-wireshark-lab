# 🔍 Network Scan & Packet Analysis (Nmap + Wireshark)

This repository contains my cybersecurity lab project focused on scanning a local network and analyzing TCP packets using Nmap and Wireshark on Kali Linux.

---

## 📌 Objective

- Perform a TCP SYN scan on the local network
- Identify live hosts and open ports
- Capture and analyze TCP traffic using Wireshark
- Distinguish between open/closed ports using SYN, SYN-ACK, and RST flags

---

## 🧰 Tools Used

- Kali Linux (Attacker VM)
- Nmap
- Wireshark
- VirtualBox or VMware (for isolated lab)
- Metasploitable 2 (Target VM for response only)

---

## 📁 Contents

| File | Description |
|------|-------------|
| `report/NetworkScan_Report.pdf` | Final compiled report |
| `report/nmap-output.png` | Screenshot of Nmap output |
| `report/wireshark-syn-filter.png` | SYN packet filter output |
| `report/wireshark-synack-filter.png` | SYN-ACK packet filter output |
| `report/wireshark-rst-filter.png` | RST packet filter output |
| `README.md` | This file |

---

## ✅ Wireshark Filters Used

- `tcp.flags.syn == 1 and tcp.flags.ack == 0` → SYN packets (connection attempts)
- `tcp.flags.syn == 1 and tcp.flags.ack == 1` → SYN-ACK (open ports)
- `tcp.flags.reset == 1` → RST packets (closed ports)

---

## 🧠 Learnings

- Performed a full SYN scan over subnet: `nmap -sS 192.168.153.0/24`
- Understood TCP 3-way handshake through live capture
- Used filters to distinguish open vs closed ports visually
- Created a professional report using LaTeX with figures and tables

---

> 🧪 All testing was done in an isolated, virtualized environment for educational purposes.
