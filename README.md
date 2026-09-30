# Network Traffic Analysis Using Wireshark

## Project Overview

This project demonstrates basic network traffic analysis and packet-level investigation using Wireshark in a controlled Kali Linux lab environment.

The objective was to capture and analyze different types of network traffic and identify important network indicators such as source IP, destination IP, ports, protocols, TCP flags, and application-layer information.

## Objectives

- Analyze DNS queries and responses
- Understand the TCP three-way handshake
- Analyze HTTP request and response traffic
- Identify source and destination IP addresses
- Identify source and destination ports
- Analyze TCP flags and connection behavior
- Examine basic port scanning activity
- Reconstruct a TCP stream
- Document packet-level evidence using screenshots and packet captures

## Tools Used

- Wireshark 4.6.6
- Kali Linux
- VMware Workstation
- curl
- nslookup
- Nmap

## Project Structure

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
    ├── 01-dns-packet-details.png
    ├── 01-dns-packet-overview.png
    ├── 02-tcp-handshake-ack.png
    ├── 02-tcp-handshake-syn-ack.png
    ├── 02-tcp-handshake-syn.png
    ├── 03-http-request.png
    ├── 03-http-response.png
    ├── 04-port-scan-rst-closed.png
    ├── 04-port-scan-syn-ack-open.png
    ├── 04-port-scan-syn.png
    └── 05-tcp-stream-reconstruction.png
```


## Investigations Performed

### 1. DNS Traffic Analysis

A DNS query was generated using `nslookup` and captured using Wireshark.

The packet was analyzed to identify:

- Source IP
- Destination IP
- UDP transport protocol
- Source port
- Destination port 53
- DNS query type
- Requested domain

### 2. TCP Three-Way Handshake

TCP traffic was captured and analyzed to understand the connection establishment process.

The analysis examined the TCP handshake sequence:

```text
SYN
 ↓
SYN-ACK
 ↓
ACK
```
```markdown

TCP flags, source and destination ports, sequence numbers, and acknowledgement numbers were examined using Wireshark.

### 3. HTTP Traffic Analysis

HTTP traffic was generated using `curl` and captured using Wireshark.

The investigation examined:

- HTTP request
- HTTP response
- Source and destination IP addresses
- TCP source and destination ports
- HTTP status code
- HTTP headers
- Request and response relationship

### 4. Basic Port Scan Analysis

Network traffic associated with basic port scanning was captured and analyzed.

The investigation examined TCP SYN packets and responses such as:

- SYN-ACK responses indicating a listening/open TCP port
- RST responses indicating that the attempted TCP connection was refused/closed

### 5. TCP Stream Reconstruction

A TCP conversation was selected in Wireshark and reconstructed using the Follow TCP Stream feature.

This demonstrated how multiple TCP packets can be viewed as part of a single communication session.

## Key Skills Demonstrated

- Packet capture
- Wireshark display filters
- DNS traffic analysis
- TCP analysis
- HTTP traffic analysis
- IP address identification
- Port identification
- TCP flag analysis
- Basic port scan analysis
- TCP stream reconstruction
- Packet-level evidence collection
- Technical documentation

## Environment

The analysis was performed in a controlled VMware Kali Linux virtual machine.

The traffic generated during the investigation was intended for educational and cybersecurity learning purposes.

## Disclaimer

This project was conducted in a controlled lab environment for educational and cybersecurity learning purposes. No unauthorized systems were targeted.