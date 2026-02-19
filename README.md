# Network Mapping & Connectivity Test
**Course:** The Bits and Bytes of Computer Networking  

## 1. Network Configuration & Results
| Network Component | Details/Results |
| :--- | :--- |
| **Operating System** | Windows 10 |
| **Local IPv4 Address** | 172.20.7.117 |
| **Default Gateway** | 172.20.6.1 |
| **Ping Target** | 8.8.8.8 (Google Public DNS) |
| **Packet Loss** | 0% |
| **Average Latency** | 1ms |

---

## 2. Network Topology Diagram
<img width="1024" height="1024" alt="network_map png" src="https://github.com/user-attachments/assets/a01cce79-8040-45b5-9e2d-bd6631c2e047" />


> **Technical Overview:** This diagram illustrates the logical transition from a private LAN to the public WAN. Data originates at the workstation (172.20.7.117) and is routed to the Default Gateway (172.20.6.1), where Network Address Translation (NAT) allows communication with the global internet.

---

## 3. Technical Evidence & Analysis

### Local IP Discovery
<img width="795" height="629" alt="ip config" src="https://github.com/user-attachments/assets/55d7efb4-de16-48ce-838c-558c5c9a9191" />

**Analysis:** The `ipconfig` output confirms a valid lease within a Class B private subnet. This indicates the local Network Interface Card (NIC) is properly initialized and has successfully communicated with a DHCP server to receive its configuration.

### Connectivity Verification (Ping Test)
<img width="507" height="293" alt="ping test" src="https://github.com/user-attachments/assets/e15f6247-e3dd-4099-b193-6d8a9e96522f" />

**Analysis:** By utilizing the **ICMP protocol**, I verified end-to-end connectivity.
* **DNS Resolution:** The successful ping to `google.com` proves the Application Layer is correctly interacting with DNS resolvers.
* **Latency Performance:** An average Round-Trip Time (RTT) of **1ms** indicates a high-bandwidth, low-jitter connection, likely due to a high-speed local backbone.
* **Reliability:** 0% packet loss confirms a stable physical and data-link layer.

---

## 4. Conclusion
The connectivity test was successful. The configuration proves that the local workstation has a clear, functional route to the internet, with all layers of the networking stack (Physical to Application) operating as intended.
