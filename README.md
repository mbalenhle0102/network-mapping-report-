# Network Mapping & Connectivity Test
**Course:** The Bits and Bytes of Computer Networking  
**Student Project:** Network Mapping & Ping Test Task

## Introduction
This project demonstrates the ability to map a local area network (LAN) and verify connectivity to the wide area network (WAN). By identifying local IP configurations and testing the path to a public DNS server, we can visualize how data travels from a local workstation to the internet.## Network Configuration & Test Results

| Network Component | Details/Results |
| :--- | :--- |
| **Operating System** | [e.g., Windows 11 / macOS / Linux] |
| **Local IPv4 Address** | [192.168.1.15 ] |
| **Default Gateway** | [192.168.1.1] |
| **Ping Target** | 8.8.8.8 (Google Public DNS) |
| **Packet Loss** | 0% |
| **Average Latency** | [e.g., 22ms] |



## Network Topology Diagram
![Network Map](![Uploading network_map.png.png…]()
)
> **Description:** Architectural Overview: This topology illustrates the transition from Private Addressing (LAN) to Public Addressing (WAN). It visualizes the "First Hop" logic where the workstation encapsulates data frames and sends them to the MAC address of the Default Gateway. The Gateway then performs NAT (Network Address Translation) to route the request across the ISP’s infrastructure to the global internet cloud.. 


### 1. Local IP Configuration
<img width="795" height="629" alt="ip config" src="https://github.com/user-attachments/assets/55d7efb4-de16-48ce-838c-558c5c9a9191" />
> **Description:** Technical Analysis: This output reveals the workstation is operating within a Class B private network range. The IPv4 Address (172.20.7.117) is the local identifier for this NIC, while the Default Gateway (172.20.6.1) indicates the internal interface of the router. The fact that these are on the same subnet confirms the local routing table is correctly configured to hand off non-local traffic to the gateway..

### 2. Connectivity Test (Ping)
<img width="507" height="293" alt="ping test" src="https://github.com/user-attachments/assets/e15f6247-e3dd-4099-b193-6d8a9e96522f" />
<img width="507" height="250" alt="ping google" src="https://github.com/user-attachments/assets/f980cc42-f5e0-4372-93e2-5adf59ca9404" />
> **Description:**Network Verification: Sending ICMP Echo Requests to 8.8.8.8 and https://www.google.com/url?sa=E&source=gmail&q=google.com yielded a 0% packet loss and an exceptionally low average latency of 1ms.

Name Resolution: The successful ping to google.com proves that the DNS (Domain Name System) is correctly resolving hostnames to IP addresses.

Network Stability: The 1ms RTT (Round Trip Time) suggests a high-speed fiber or high-performance local backbone connection with negligible jitter.



## Methodology
To complete this task, the following steps were performed:
1. **Discovery:** Used the `ipconfig` (or `ifconfig`) command to identify the device's local IP and the router's gateway address.
2. **Testing:** Utilized the `ping` command to send ICMP Echo Request packets to a remote server (8.8.8.8).
3. **Mapping:** Created a topology diagram to show the relationship between the workstation, the router, the ISP, and the internet.

## Conclusion
The connectivity test was successful. The 0% packet loss confirms that the local Network Interface Card (NIC) is functional, the router is correctly performing NAT (Network Address Translation), and there is an active route to the public internet.

##Term,Definition in this Project
ICMP,"The protocol used by ping to send ""Echo Requests"" and receive ""Echo Replies."""
Latency,The time it takes for a data packet to travel to the target and back (measured in ms).
Default Gateway,"The ""exit door"" of your local network; the router's address."
Subnet Mask,Determines which part of the IP address is the network ID vs. the host ID.
