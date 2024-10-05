# Wireshark Basic Traffic Analysis and Nmap Scans

## Overview

This `README.md` provides an introduction to basic traffic analysis using **Wireshark** and highlights 15 types of network analysis you can perform using Wireshark. Additionally, it covers 15 types of **Nmap** scans that are essential for network discovery and security auditing.

---
## Pre-requisites:

• Basic understanding of network protocols and packet structures.

• Installing Kali OS on Virtual Box and Kali Purple on VMWare

---
## Wireshark: Basic Traffic Analysis

Wireshark is a widely-used network protocol analyzer that allows users to capture and interactively browse the traffic running on a computer network. It's useful for troubleshooting network issues, analyzing suspicious traffic, and investigating performance bottlenecks.

### Getting Started with Wireshark

1. **Install Wireshark**: Download and install Wireshark from [https://www.wireshark.org/](https://www.wireshark.org/).

2. **Open Wireshark**: Launch Wireshark and select the network interface you want to monitor.

![Screenshot 2024-10-04 205105](https://github.com/user-attachments/assets/fe1e8a41-f486-49af-955f-b3449debbc1c)

3. **Start Capturing Traffic**: Click the **Start** button to begin capturing packets on your chosen interface.

![Screenshot 2024-10-04 205105](https://github.com/user-attachments/assets/0f1b12a7-e991-4f5d-b56f-e22c689fc5d4)

4. **Stop Capturing Traffic**: Click the **Stop** button to halt packet capture once you’ve gathered sufficient data.

![Screenshot 2024-10-05 082223](https://github.com/user-attachments/assets/5e92fbc3-29c5-4987-be90-368669f4b55d)

5. **Analyze Packets**: Use filters, statistics, and other analysis tools to dissect the captured packets.

![Screenshot 2024-10-05 090225](https://github.com/user-attachments/assets/d46ff414-93d5-4d89-97a9-99fb8f2c4023)

---

## 15 Types of Network Analysis Using Wireshark

1. **Packet Capture**  
   Capture all network traffic on an interface and display detailed packet data in real-time.

![Screenshot 2024-10-05 090640](https://github.com/user-attachments/assets/903cbcfb-4d77-463a-85bc-6e577bfa8532)

2. **Protocol Analysis**  
   Analyze the different network protocols in use, such as HTTP, TCP, UDP, DNS, and more.

![Screenshot 2024-10-05 090225](https://github.com/user-attachments/assets/0efd76ca-870c-4baf-81e4-e955d06f712a)

3. **Filter Traffic by IP Address**  
   Focus on traffic from or to a specific IP address using filters (e.g., `ip.addr == 142.250.200.67`).

![Screenshot 2024-10-05 092256](https://github.com/user-attachments/assets/9aeb5067-41bc-417b-ac11-f1da3ea8ee35)

4. **Filter Traffic by Protocol**  
   Analyze specific protocols, such as HTTP (`http`), DNS (`dns`), or SSL/TLS (`ssl`).

![wire http filter](https://github.com/user-attachments/assets/2c95f18c-6add-49cc-b53d-8c4cd3f4f0d1)
![wire dns filter](https://github.com/user-attachments/assets/40fff4fb-7101-4420-88f1-6824e89e62ee)

5. **Reconstruct TCP Sessions**  
   Follow and reconstruct TCP streams to view entire communication sessions between two endpoints.

![Screenshot 2024-10-05 093631](https://github.com/user-attachments/assets/956f5473-bc71-45f0-b767-d5c32a628230)

6. **Network Latency Analysis**  
   Measure Round Trip Time (RTT) and identify delays in packet delivery between source and destination.

![Screenshot 2024-10-05 115127](https://github.com/user-attachments/assets/d9d3aef3-7be0-4f22-937b-cb70c98eb843)

7. **Bandwidth Usage Monitoring**  
   Determine which hosts or protocols are consuming the most bandwidth.

![Screenshot 2024-10-05 115737](https://github.com/user-attachments/assets/36b04f6e-c0e6-4ed7-87ad-87808ba614ac)

8. **DNS Query Analysis**  
   Monitor and inspect DNS queries and responses to troubleshoot name resolution issues.

![Screenshot 2024-10-05 120411](https://github.com/user-attachments/assets/2ad7b252-960d-4ab4-b6ba-32463dc9004b)

9. **HTTP/HTTPS Analysis**  
   Analyze web traffic, inspect HTTP requests/responses, and follow TLS/SSL handshakes.

10. **VoIP Traffic Analysis**  
    Capture and analyze VoIP (SIP/RTP) traffic to troubleshoot call setup, quality, or security issues.

11. **Capture File Transfers**  
    Analyze file transfer protocols like FTP, SMB, or HTTP file uploads/downloads.

12. **Identify Security Threats**  
    Detect malicious traffic, port scanning, man-in-the-middle attacks, or abnormal network behavior.

13. **Filter by Port Number**  
    Analyze traffic to or from a specific port (e.g., `tcp.port == 80` for HTTP).

14. **Analyze Packet Loss**  
    Identify packet retransmissions or dropped packets to diagnose network instability.

15. **Check Network Congestion**  
    Examine TCP window sizes and sequence numbers to detect congestion and bottlenecks.

---

## Nmap: Types of Scans

Nmap (Network Mapper) is a network discovery and security auditing tool. It provides a range of scans for identifying hosts, services, and potential vulnerabilities on a network.

### 15 Types of Nmap Scans

1. **TCP SYN Scan (Stealth Scan)**  
   **Command:** `nmap -sS [target]`  
   A fast and stealthy scan that only sends SYN packets to detect open ports without completing the TCP handshake.

2. **TCP Connect Scan**  
   **Command:** `nmap -sT [target]`  
   Completes the full TCP handshake, useful when SYN scanning is not allowed.

3. **UDP Scan**  
   **Command:** `nmap -sU [target]`  
   Detects open UDP ports by sending UDP packets to check for responses.

4. **SCTP INIT Scan**  
   **Command:** `nmap -sY [target]`  
   Scans for open SCTP ports using the INIT packet, used in specialized network communications.

5. **SCTP COOKIE-ECHO Scan**  
   **Command:** `nmap -sZ [target]`  
   Uses COOKIE-ECHO chunks to identify SCTP services more accurately.

6. **Ping Scan (ICMP Scan)**  
   **Command:** `nmap -sn [target]`  
   Checks if hosts are online by sending ICMP echo requests, without port scanning.

7. **TCP ACK Scan**  
   **Command:** `nmap -sA [target]`  
   Determines firewall rules and detects whether a port is filtered by sending ACK packets.

8. **TCP Window Scan**  
   **Command:** `nmap -sW [target]`  
   Analyzes TCP window size responses to detect open ports even when firewalls are blocking SYN/ACK responses.

9. **TCP FIN Scan**  
   **Command:** `nmap -sF [target]`  
   Sends TCP FIN packets to determine open or closed ports on systems with weak security configurations.

10. **Xmas Scan**  
    **Command:** `nmap -sX [target]`  
    Sends TCP packets with FIN, PSH, and URG flags set to detect open ports.

11. **Null Scan**  
    **Command:** `nmap -sN [target]`  
    Sends packets with no TCP flags to elicit responses from poorly-configured systems.

12. **Idle (Zombie) Scan**  
    **Command:** `nmap -sI [zombie] [target]`  
    A stealthy scan that uses a third-party system to send packets, masking the source of the scan.

13. **Service Version Detection Scan**  
    **Command:** `nmap -sV [target]`  
    Detects the software version running on open ports.

14. **Operating System Detection Scan**  
    **Command:** `nmap -O [target]`  
    Attempts to identify the target’s operating system based on network responses.

15. **NSE Script Scan**  
    **Command:** `nmap --script [scriptname] [target]`  
    Uses the Nmap Scripting Engine to perform advanced scans, such as vulnerability assessments or brute force attacks.

---

## Conclusion

By combining **Wireshark** and **Nmap**, network administrators and security professionals can effectively monitor, analyze, and secure network environments. Wireshark’s powerful traffic analysis capabilities, paired with Nmap’s versatile scanning techniques, provide a comprehensive toolkit for identifying vulnerabilities and maintaining network integrity.

---

### Additional Resources

- [Wireshark Official Documentation](https://www.wireshark.org/docs/)
- [Nmap Official Documentation](https://nmap.org/book/man.html)

---

Feel free to contribute to this document by submitting pull requests or opening issues for improvement!
