🔰General Packet Capture & Filtering


## 🎯 Objective

The objective of this lab is to learn and  get hands-on experience with **Wireshark** by capturing and analyzing general network traffic.


## 🛠️ Lab Setup

### System Requirements

* Operating System: Kali Linux (Wireshark pre-installed)
* Network Adapter: Required for live capture

### Files Needed

[Sample PCAP file](na_pcap.pcapng)



## 📘 **Protocol Analyzed in this Lab**

For this lab, I focused on analyzing **ICMP traffic** (Internet Control Message Protocol), which is often used for **ping requests/replies** and is helpful for basic connectivity and troubleshooting.



## 🔍 **Filters Used in Wireshark**

| Filter           | Type           | Description                                    |
| ---------------- | -------------- | ---------------------------------------------- |
| `icmp`           | Display Filter | Shows all ICMP traffic                         |
| `icmp.type == 8` | Display Filter | Shows only ICMP Echo Requests                  |
| `icmp.type == 0` | Display Filter | Shows only ICMP Echo Replies                   |
| `icmp`           | Capture Filter | Captures only ICMP packets during live capture |



## ✅ Conclusion

🔰Learned how to create a custom profile called **“SOC Analyst.”**
🔰Successfully applied **display and capture filters** to focus only on ICMP traffic.
🔰This exercise showed how Wireshark can be used to filter large amounts of traffic and zero in on specific communication patterns.

Screenshots provided showing result

🔰New profile named **“SOC Analyst.”
🔰Display filter applied to view ICMP traffic.
🔰Capture filter applied to collect only ICMP traffic.


![Alt text](Captured-file-upload.png)
![Alt text](profile.png)
![Alt text](icmp-1.png)
