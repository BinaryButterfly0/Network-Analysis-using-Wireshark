## HTTP Protocol Analysis


## 🎯 Objective

The objective of this lab was to analyze HTTP (Hypertext Transfer Protocol) packets using Wireshark. I explored HTTP request and response headers, understood how web communication works, and learned how to detect common HTTP-based data leaks or suspicious activity.


## 🛠️ Lab Setup

### System Environment

 Operating System: Kali Linux (Wireshark pre-installed)
 Network Adapter: Used for packet capture

### Files Used

[Sample PCAP file](na_pcap.pcapng)

## 📘 Protocol Analyzed

In this lab, I analyzed HTTP traffic, which is an application-layer protocol used for communication between clients (browsers) and web servers. HTTP usually runs over TCP port 80.

### Key HTTP Fields Observed:

| Field Name         | Description                                 |
| ------------------ | ------------------------------------------- |
| Request Method | GET, POST, HEAD, etc.                       |
| Host           | Website being accessed                      |
| User-Agent     | Information about the client/browser        |
| URI            | Resource path on the server                 |
| Status Code    | Server response status (e.g., 200 OK)       |
| Content-Type   | MIME type of the response (e.g., text/html) |
| Cookie/Header  | Session or tracking information             |

---

## 🔍 Filters I Used in Wireshark

| Filter                         | Purpose                              |
| ------------------------------ | ------------------------------------ |
| `http`                         | Show all HTTP traffic                |
| `tcp.port == 80`               | Show HTTP traffic on default port    |
| `http.request.method == "GET"` | Show all GET requests                |
| `http.request.uri`             | View requested resources             |
| `http.set_cookie`              | Show cookies in HTTP responses       |
| `ip.addr == 192.168.1.10`      | HTTP traffic to/from a specific host |

---


 🔰HTTP traffic is readable and easy to analyze in Wireshark.
 By examining HTTP packets, I could detect:

   🔰Sensitive data in URLs or headers
   🔰Malware beaconing to C2 servers
   🔰Suspicious file downloads or unauthorized access
 Filters make it easier to focus on requests, responses, and cookies for investigation.


Screenshots captured showing results

 All HTTP traffic
![Alt text](http.png)


 All GET requests

 ![Alt text](get.png)


 Requested resources

![Alt text](http.png)

