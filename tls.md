
# TLS Protocol Analysis


## 🎯 **Objective**

The objective of this lab was to analyze **TLS (Transport Layer Security)** traffic using **Wireshark**. I explored how TLS secures data over the network, observed handshake messages, and identified metadata such as server names and certificate details.

---

## 🛠️ **Lab Setup**

### **System Environment**

* **Operating System:** Kali Linux (Wireshark pre-installed)
* **Network Adapter:** Used for packet capture

### **Files Used**

[Sample PCAP file](na_pcap.pcapng)



## 📘 **Protocol Analyzed**

In this lab, I analyzed **TLS traffic**, which is a **cryptographic protocol** used to secure communications over the internet. TLS usually runs over **TCP port 443** and is used in HTTPS, FTPS, SMTPS, etc.

### **Key TLS Handshake Messages Observed:**

| Message Type     | Description                                              |
| ---------------- | -------------------------------------------------------- |
| **Client Hello** | Client initiates secure connection, offers cipher suites |
| **Server Hello** | Server selects cipher and provides certificate           |
| **Certificate**  | Server sends digital certificate (X.509)                 |
| **Key Exchange** | Client and server exchange keys for the session          |
| **Finished**     | Secure session begins                                    |

---

## 🔍 **Filters I Used in Wireshark**

| Filter                         | Purpose                    |
| ------------------------------ | -------------------------- |
| `tls`                          | Show all TLS traffic       |
| `tcp.port == 443`              | Show TLS over HTTPS        |
| `tls.handshake.type == 1`      | Show Client Hello messages |
| `tls.handshake.type == 2`      | Show Server Hello messages |
| `tls.record.version == 0x0303` | TLS 1.2 traffic            |
| `tls.record.version == 0x0304` | TLS 1.3 traffic            |

---

## ✅ **Conclusion**

* TLS encrypts communication, so the actual payload is unreadable without keys.
* Wireshark can reveal **metadata** like server names (SNI), certificate chains, and TLS versions.
* Analyzing TLS metadata helps detect:

  🔰 Outdated TLS versions (e.g., TLS 1.0)
  🔰 Suspicious or self-signed certificates
  🔰 Malicious domain encryption abuse



Screenshots captured showing results

🔰 All TLS traffic
![Alt text](tls.png)


🔰 Client Hello messages

![Alt text](handshake-type.png)


🔰 TLS 1.2 traffic

![Alt text](tlsversion.png)













