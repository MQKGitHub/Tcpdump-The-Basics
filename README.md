### 🛡️ Tcpdump: The Basics

**Room:** [Tcpdump: The Basics — TryHackMe](https://tryhackme.com/room/tcpdump)  
**Status:** ✅ Completed  
**Date:** *22 May 2025*

### 🎯 Objective  
To learn how to use Tcpdump to capture, filter, and display network packets. The focus was on saving to PCAP files, filtering by host, port, or protocol, and displaying packets in readable formats.

---

### 🗝️ Key Concepts  
- **Tcpdump** — A command-line packet capture tool used to sniff, save, and analyse network traffic.  
- **libpcap** — A C-based library used by Tcpdump and Wireshark to capture network packets.  
- **Capture Filters** — Filters applied while collecting packets (e.g. by host, port, or protocol).  
- **Display Filters** — Options to control how captured packets are displayed.  
- **Verbose Flags (`-v`, `-vv`, `-vvv`)** — Increase the level of detail shown in captured packets.  
- **Quick Output (`-q`)** — Shortens the displayed packet information.  
- **Hex/ASCII Display (`-X`)** — Displays packet headers and data in both hexadecimal and ASCII.  
- **TCP Flags Filtering** — Use expressions like `tcp[tcpflags] & tcp-syn != 0` to capture SYN packets.  
- **Binary Operators (`&`, `|`, `!`)** — Used to apply logical operations in advanced filters.  

---

### 🛠️ Tools Used  
- **Tcpdump** — Used to capture live traffic, save to `.pcap` files, apply filters, and inspect packet contents.  
- **wc** — Used to count packet lines when piped with Tcpdump output.  

---

### ⚠️ Challenges Faced  
- Some advanced filter expressions using TCP flags and byte offsets were tricky.
- Binary operations like `&` and `|` in Tcpdump filters took a bit of extra reading.

*Solution:* Focused on understanding examples and tested each one in the terminal. Reading the `man pcap-filter` helped.

---

### 🧠 What I Learned  
- How to filter by host (`host IP`), port (`port 53`), or protocol (`icmp`, `tcp`).  
- How to use Tcpdump with `-w` to save PCAPs, and `-r` to read and filter them later.  
- The difference between capture vs display filters.  
- How to use TCP flags and binary logic to isolate specific types of traffic like SYN or ACK.  
- Custom display formats using `-q`, `-e`, `-A`, `-xx`, and `-X`.

---

### 🌐 Real-World Application:  
> Tcpdump is often used by network engineers and security analysts to quickly capture and inspect traffic directly from the terminal, especially when GUIs like Wireshark are unavailable. It’s also great for scripting, automation, and forensic packet analysis during incident response.

---

### 💭 Reflections:  
- Tcpdump is way more powerful than I expected for a terminal-only tool.  
- The filter expressions gave me a good challenge and made me feel more confident working closer to the packet level.  
