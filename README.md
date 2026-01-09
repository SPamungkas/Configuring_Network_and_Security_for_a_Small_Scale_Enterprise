# Configuring_Network_and_Security_for_a_Small_Scale_Enterprise
Designing and configuring a simple corporate network topology using Cisco Packet Tracer, including the implementation of IP addressing schemes, gateways, and end-to-end connectivity verification.

# About Me
Information Systems graduate, currently transitioning to Cyber Security. Previously served as a Technician at Oil and Gas Industry (Pertamina Patra Niaga vendor), where I developed a highly disciplined approach to managing critical infrastructure compliance and 24/7 reliability. Currently formalizing expertise through an intensive cybersecurity bootcamp at Dibimbing, I am eager to apply this technical foundation and structured approach to a security operations role.

# Tools
- Cisco Packet Tracer

# Topology Design 
Network Topology Design for a Small Enterprise
<p align="center">
  <img width="500" height="311" alt="image" src="https://github.com/user-attachments/assets/18b40cd0-fbb3-4695-96ab-6d4c85a993b1" />
  <br>
</p>

# 1. Router Configuration 
Before assigning an IP address to the router, install the PT-ROUTER-NM-1CFE module. Then, open the router configuration. The first technical step involved configuring the Router 0 to act as the central gateway for the network.
<p align="center">
  <img width="500" height="460" alt="image" src="https://github.com/user-attachments/assets/e5e5ccbd-0212-419b-b304-84240e9961b2" />
  <br>
</p>
To establish connectivity across the entire infrastructure, I configured multiple interfaces on the router(s). Each interface serves as a unique gateway for different network segments. Since the configuration process for each interface is identical, I used a standardized approach: assigning the IP address, defining the subnet mask, and enabling the port status.
<br>
<br>

<div align="center">
  
| Device | Interface | IP Address | Subnet Mask | Port Status |
| :--- | :--- | :--- | :--- | :--- |
| **Router 0** | FastEthernet 0/0 | 192.168.1.1 | 255.255.255.0 | **Active (On)** |
| **Router 0** | FastEthernet 1/0 | 192.168.2.1 | 255.255.255.0 | **Active (On)** |
| **Router 1** | FastEthernet 0/0 | 192.168.2.2 | 255.255.255.0 | **Active (On)** |
| **Router 1** | FastEthernet 1/0 | 192.168.3.1 | 255.255.255.0 | **Active (On)** |

</div>

Note: The configuration for Router 1 follows the same standardized procedure as Router 0. This involves assigning the designated static IP address to the respective FastEthernet interfaces and enabling the port 

# 2. PC and Laptop Configuration
All workstations (PCs and Laptops) were configured with static IP addresses corresponding to their respective gateways.
<p align="center">
  <img width="500" height="443" alt="image" src="https://github.com/user-attachments/assets/aeb03371-48f3-487c-9673-40a091e0bc6c" />
  <br>
</p>

<div align="center">
  
| Device | Interface | IP Address | Subnet Mask
| :--- | :--- | :--- | :--- |
| **PC 0** | FastEthernet 0 | 192.168.1.2 | 255.255.255.0
| **PC 1** | FastEthernet 0 | 192.168.3.2 | 255.255.255.0
| **Laptop 0** | FastEthernet 0 | 192.168.3.3 | 255.255.255.0

</div>

# 3. Physical Layer & Cabling Standards
1. Copper Straight Through Cable:
- PC to Switch
- Switch to Router <br>

2. Copper Cross Over Cable:
- PC to Router
- Router to Router

# 4. Connectivity Testing & Verification
- Local Connectivity: Ping from PC-01 to router — Result: Success.
<p align="center">
  <img width="500" height="243" alt="image" src="https://github.com/user-attachments/assets/9f61d8ec-2446-476e-8f64-9255a9dad4cc" />
  <br>
</p>
<br>
- Inter Network Connectivity: Ping from PC-01 to Laptop-01 — Result: Success.
<p align="center">
  <img width="500" height="235" alt="image" src="https://github.com/user-attachments/assets/72b0c824-7625-44a9-aaf3-44b28ab9f7ad" />
  <br>
</p>
