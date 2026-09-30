\# Network Traffic Analysis Using Wireshark



\## Project Overview



This project demonstrates basic network traffic analysis and packet-level investigation using Wireshark in a controlled Kali Linux lab environment.



The objective was to capture and analyze different types of network traffic and identify important network indicators such as source IP, destination IP, ports, protocols, TCP flags, and application-layer information.



\## Objectives



\- Analyze DNS queries and responses

\- Understand the TCP three-way handshake

\- Analyze HTTP request and response traffic

\- Identify source and destination IP addresses

\- Identify source and destination ports

\- Analyze TCP flags and connection behavior

\- Examine basic port scanning activity

\- Reconstruct a TCP stream

\- Document packet-level evidence using screenshots and packet captures



\## Tools Used



\- Wireshark 4.6.6

\- Kali Linux

\- cURL

\- nslookup

\- Python HTTP server

\- Nmap



\## Investigations Performed



\### 1. DNS Traffic Analysis



Analyzed a DNS query generated using `nslookup` and identified:



\- Source IP

\- Destination IP

\- UDP transport protocol

\- Source port

\- Destination port 53

\- DNS query type

\- Requested domain



\### 2. TCP Three-Way Handshake



Captured and analyzed TCP connection establishment using:



\- SYN

\- SYN-ACK

\- ACK



The packet sequence was examined to understand how a TCP connection is established.



\### 3. HTTP Traffic Analysis



Generated HTTP traffic in the controlled lab and analyzed:



\- HTTP request

\- HTTP response

\- Source and destination IPs

\- TCP ports

\- HTTP status information

\- Request/response relationship



\### 4. Port Scanning Analysis



Generated controlled TCP scanning traffic and analyzed TCP responses, including:



\- SYN packets

\- SYN-ACK responses

\- RST responses

\- Source and destination ports

\- TCP connection behavior



\### 5. TCP Stream Reconstruction



Used Wireshark's TCP stream functionality to follow and reconstruct communication belonging to a TCP connection.



\## Project Structure



```text

SOC-Wireshark-Project/

│

├── captures/

│   ├── 01-dns-analysis.pcapng

│   ├── 02-tcp-handshake.pcapng

│   ├── 03-http-analysis.pcapng

│   └── 04-port-scan-analysis.pcapng

│

├── notes/

│   ├── 01-dns-analysis.txt

│   ├── 02-tcp-handshake.txt

│   ├── 03-http-analysis.txt

│   ├── 04-port-scan-analysis.txt

│   └── 05-tcp-stream-analysis.txt

│

├── reports/

│   └── 00-Network-Traffic-Analysis-Report.txt

│

└── screenshots/

&#x20;   └── Packet-analysis evidence



\##Key Learning Outcomes



Through this lab, I practiced:



* Packet capture and filtering
* Network protocol identification
* IP and port analysis
* TCP flag analysis
* DNS traffic analysis
* HTTP traffic analysis
* Basic network reconnaissance analysis
* Packet-level evidence collection
* Technical documentation



\##Environment



The analysis was performed in a controlled VMware Kali Linux virtual machine.



The traffic generated during the investigation was intended for educational and security-analysis purposes within the lab environment.



\##Disclaimer



This project was conducted in a controlled lab environment for educational and cybersecurity learning purposes. No unauthorized systems were targeted.

