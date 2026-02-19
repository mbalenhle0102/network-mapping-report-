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
<img width="1024" height="1024" alt="diagram" src="https://github.com/user-attachments/assets/2bb2e751-9b2c-4cfc-9c43-a01d867e86b6" />
> **Description:** This diagram provides a visual representation of the data path from the local workstation through the router and ISP to the public internet.

### 1. Local IP Configuration
<img width="795" height="629" alt="ip config" src="https://github.com/user-attachments/assets/55d7efb4-de16-48ce-838c-558c5c9a9191" />
> **Description:** Output of the `ipconfig` command identifying the workstation's unique IP on the LAN and the Default Gateway (Router) address.

### 2. Connectivity Test (Ping)
<img width="507" height="293" alt="ping test" src="https://github.com/user-attachments/assets/e15f6247-e3dd-4099-b193-6d8a9e96522f" />
<img width="507" height="250" alt="ping google" src="https://github.com/user-attachments/assets/f980cc42-f5e0-4372-93e2-5adf59ca9404" />
> **Description:** Successful `ping` tests to Google's DNS (8.8.8.8) and google.com, verifying that the network is successfully resolving names and routing traffic externally with 0% packet loss.




## Methodology
To complete this task, the following steps were performed:
1. **Discovery:** Used the `ipconfig` (or `ifconfig`) command to identify the device's local IP and the router's gateway address.
2. **Testing:** Utilized the `ping` command to send ICMP Echo Request packets to a remote server (8.8.8.8).
3. **Mapping:** Created a topology diagram to show the relationship between the workstation, the router, the ISP, and the internet.

## Conclusion
The connectivity test was successful. The 0% packet loss confirms that the local Network Interface Card (NIC) is functional, the router is correctly performing NAT (Network Address Translation), and there is an active route to the public internet.
