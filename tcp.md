#TCP Protocol Analysis


## 🎯 Objective

The objective of this lab was to analyze TCP (Transmission Control Protocol) traffic using Wireshark. I focused on how TCP establishes connections with the 3-way handshake, how it tears them down, and how to interpret important TCP fields and flags.


## 🛠️ Lab Setup

### System Environment

* Operating System:  Kali Linux (Wireshark is pre-installed)
* Network Adapter:   Used for packet capture

### Files Used

* [Sample PCAP file]



## 📘 Protocol Analyzed

In this lab, I analyzed TCP traffic, a Layer 4 transport protocol that ensures reliable and ordered communication. I looked at how connections are started (SYN), acknowledged (ACK), and closed (FIN).



## 🔍 Filters I Used in Wireshark

| Filter                   | Purpose                                    |
| ------------------------ | ------------------------------------------ |
| `tcp`                    | Show all TCP packets                       |
| `tcp.flags.syn == 1`     | Show packets starting a connection (SYN)   |
| `tcp.flags.fin == 1`     | Show packets ending a connection (FIN)     |
| `tcp.port == 80`         | Show TCP packets on port 80 (HTTP traffic) |
| `ip.addr == 192.168.1.1` | TCP traffic to/from a specific host        |




* TCP guarantees **reliable, ordered data transfer** using features like the **3-way handshake** and **flow control**.
* By focusing on **TCP flags** (SYN, ACK, FIN), I was able to clearly see connection setup and teardown in the capture.
* These techniques are useful for identifying abnormal traffic such as **scanning activity, RST floods, or connection resets**.

I captured screenshots showing results

* All TCP packets
* SYN packets (connection start)
* FIN packets (connection end)
* TCP traffic to/from a specific host
