# Network Mapping & Connectivity Test
**Course:** The Bits and Bytes of Computer Networking  
**Student Project:** Network Mapping & Ping Test Task

## Introduction
This project demonstrates the ability to map a local area network (LAN) and verify connectivity to the wide area network (WAN). By identifying local IP configurations and testing the path to a public DNS server, we can visualize how data travels from a local workstation to the internet.## Network Configuration & Test Results

| Network Component | Details/Results |
| :--- | :--- |
| **Operating System** | [e.g., Windows 11 / macOS / Linux] |
| **Local IPv4 Address** | [e.g., 192.168.1.XX] |
| **Default Gateway** | [e.g., 192.168.1.1] |
| **Ping Target** | 8.8.8.8 (Google Public DNS) |
| **Packet Loss** | 0% |
| **Average Latency** | [e.g., 22ms] |

## Network Topology Diagram
Below is a visual representation of the network path used during this test:
<img width="1024" height="1024" alt="diagram" src="https://github.com/user-attachments/assets/2bb2e751-9bc2-4cfc-9c43-a01d867e86b6" />


![Network Map](<img width="795" height="629" alt="ip config" src="https://github.com/user-attachments/assets/fdb3238b-06ab-4a27-bffc-57119dc0d884" />
)## Methodology
To complete this task, the following steps were performed:
1. **Discovery:** Used the `ipconfig` (or `ifconfig`) command to identify the device's local IP and the router's gateway address.
2. **Testing:** Utilized the `ping` command to send ICMP Echo Request packets to a remote server (8.8.8.8).
3. **Mapping:** Created a topology diagram to show the relationship between the workstation, the router, the ISP, and the internet.

## Conclusion
The connectivity test was successful. The 0% packet loss confirms that the local Network Interface Card (NIC) is functional, the router is correctly performing NAT (Network Address Translation), and there is an active route to the public internet.
