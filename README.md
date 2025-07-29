# 5G Security and Resource Allocation Dataset

This repository provides a **comprehensive collection of 5G datasets** designed for analyzing security threats and resource allocation behaviors in next-generation mobile networks. The datasets were generated in controlled testbed and simulation environments, covering a range of **control-plane, data-plane, and radio-layer experiments**.

---

## Dataset Contents

### **5G Security Attack Datasets**

Generated using **Open5GS**, **OpenAirInterface (OAI)**, and **Amarisoft 5G cores**, covering multiple attack scenarios:

- **Flooding Attacks:** Deregistration flooding, Registration flooding, ICMP flooding, SYN flooding  
- **Replay-based Attacks:** High-rate control-plane message replays via 5Greplay  
- **PFCP Session Deletion DoS:** Spoofed SMF IP and brute-forced SEIDs to disconnect UEs  
- **Fuzzing Attacks:** Malformed NAS messages triggering repeated NG setup failures  
- **Physical-layer Jamming (analysis-only):** Based on simulated resource allocation telemetry  

Each scenario includes:

- **`.pcap` files:** Raw network captures for low-level protocol analysis  
- **`.csv` files:** Processed and labeled datasets (benign vs. malicious traffic), extracted via [5GPacketParser](https://github.com/)  
- **AMF log snapshots:** Internal errors and crash reports during attacks  

---

### **Resource Allocation Telemetry Dataset (MATLAB SLS)**

To complement the security datasets, we provide **radio resource scheduling traces** generated using the **MATLAB 5G Toolbox System Level Simulator (SLS)**.

- Simulations ran with three scheduling algorithms: **Proportional Fair (PF)**, **Round Robin (RR)**, and **Best CQI**  
- **Monte Carlo runs** with 4–12 user devices randomly distributed in a 5 MHz channel  
- Logged **per-OFDM-symbol allocations** for every UE, capturing:
  - Resource Block (RB) group assignments  
  - Modulation and Coding Scheme (MCS) levels  
  - Channel Quality Indicators (CQI) per RB  
  - RB-pair allocation patterns  

This dataset supports **selective jamming attack analysis**, showing how predictable scheduling behavior could help attackers anticipate RB usage and disrupt specific UEs with minimal interference.

---

## Reference

These datasets are introduced and discussed in the following publication:

> **Title:** A Comprehensive 5G Network Dataset for Control and Data Plane Security and Resource Allocation Analysis  
> **Authors:** Beny Nugraha, Mehrdad Hajizadeh, Tim Niehoff, Abhishek Venkatesh Jnanashree, Trung V. Phan, Dionysia Triantafyllopoulou, Oliver Krause, Martin Mieth, Klaus Moessner, and Thomas Bauschert  
> **Conference:** *2025 IEEE International Conference on Cyber Security and Resilience (CSR)*, Chania, Crete, Greece, August 4–6, 2025.  

If you use these datasets in your research, please cite this paper.

---

## ⚙️ Tools Used

- **[5GPacketParser](https://github.com/trungpv92/5GPacketParser/):** Converts `.pcap` captures to structured `.csv` format with labeled traffic flows 

---

