<h1>Implementation of Banking Network Infrastructure</h1>

<h2>Goal</h2>
<br />In this lab, I will design a network comprising four floors, with each floor containing three departments. Each department will be equipped with its own devices, and the networks of each department will be isolated to ensure data security. The objective of this project is to enable seamless communication between all devices.
<br />
To achieve this, I will utilize four routers, one for each floor, and deploy four Layer3 switches per floor. Each Layer3 switch will be interconnected with the corresponding routers and three Layer2 switches for each floor. Additional details are provided in the accompanying diagram..

<h2>Environments Used </h2>

- <b>Packet Tracer</b> 
- <b>Windows 11</b>

<h2>Lab walk-through:</h2>
Step Nr.1: The initial step involves creating a network diagram to provide a clearer understanding of the process and illustrate the methodology to be employed.
<p align="center">
Step Nr.1 : Network Diagram: <br/>
<img src="https://i.imgur.com/w8KYEpa.png" height="80%" width="80%" alt="Lab Steps Nr.1"/>
<br />
Step Nr.2: Configure basic settings on all devices, including enabling SSH on the routers and 13 switches.
For all departmental switches, the following configurations will be applied:Set console and VTY passwords, Configure banner messages, Disable domain name lookup, Enable password encryption.
<p align="center">
Step Nr. 2: VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/pb2OHuF.png" height="80%" width="80%" alt="Lab Steps Nr.2"/>
<img src="https://i.imgur.com/h6BCDeh.png" height="80%" width="80%" alt="Lab Steps Nr.2"/>
<br />
Step Nr.2.1: Configure basic settings on all devices, including enabling SSH on the routers and 13 switches.
For all departmental switches, the following configurations will be applied:Set console and VTY passwords, Configure banner messages, Disable domain name lookup, Enable password encryption.
<p align="center">
Step Nr. 2.1 : VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/pb2OHuF.png" height="80%" width="80%" alt="Lab Steps Nr.2.1"/>
<img src="https://i.imgur.com/h6BCDeh.png" height="80%" width="80%" alt="Lab Steps Nr.2.1"/>
<br />
Step Nr.2.2: Next, I will replicate the same configuration across all routers.
<p align="center">
Step Nr. 2.2 : VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/FYaiZNM.png" height="80%" width="80%" alt="Lab Steps Nr.2.2"/>
<img src="https://i.imgur.com/jHKW86d.png" height="80%" width="80%" alt="Lab Steps Nr.2.2"/>
<br />
Step Nr.3: Here, I will configure VLAN assignments, along with all access and trunk ports, and implement switch port security across all 12 switches. The Layer 3 switches connecting to each department switch will be set as trunk ports, and similarly, the Layer 2 switches connected to their respective department switches will be configured as access ports.
<p align="center">
Step Nr.3 : Trunk, Port Security : <br/>
<img src="https://i.imgur.com/sVIqvSb.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/JE5427V.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/fVO6Xch.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/3TdbIVd.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<br />
Step Nr.4: I will begin by performing subnetting and IP addressing. First, I will configure the trunk ports on the Layer 3 switches to connect with all departmental interfaces. Then, I will assign IP addresses to the Layer 3 switch interfaces according to the provided diagram. Subsequently, I will configure the router interfaces in accordance with the diagram and assign the appropriate clock rates to each serial interface.
<p align="center">
Step Nr.4 : Trunk, Port Security : <br/>
<img src="https://i.imgur.com/sVIqvSb.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<img src="https://i.imgur.com/JE5427V.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<img src="https://i.imgur.com/fVO6Xch.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<img src="https://i.imgur.com/3TdbIVd.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<br />
Step Nr.5: I will begin by configuring the OSPF protocol on the routers, followed by its implementation on all switches.
<p align="center">
Step Nr.5 : OSPF Configuration : <br/>
<img src="https://i.imgur.com/KAbrCPO.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<img src="https://i.imgur.com/bzgGjYQ.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<img src="https://i.imgur.com/hhZOAw9.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<img src="https://i.imgur.com/MgnC58t.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<br />
Step Nr.6: I will assign static IP addresses to all devices in the server room, beginning with the servers.
<p align="center">
Step Nr.6 : Assign Server's IP : <br/>
<img src="https://i.imgur.com/s1rdIPn.png" height="80%" width="80%" alt="Lab Steps Nr.6"/>
<img src="https://i.imgur.com/o4ATbyA.png" height="80%" width="80%" alt="Lab Steps Nr.6"/>
<br />
Step Nr.7: I will configure the DHCP server to assign IP addresses to all devices across the network. Specifically, I will create address pools for each floor and its respective departments, excluding the server department. This will involve creating 11 distinct pools for the 4 floors, with each floor consisting of 3 departments.
<p align="center">
Step Nr.7 : DHCP Pool : <br/>
<img src="https://i.imgur.com/sFAee5h.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
<br />
Step Nr.8: Inter-VLAN routing will be configured across all 13 switches, along with the assignment of IP DHCP helper addresses. As indicated in the diagram, the DHCP server is located on a separate network. To ensure all devices can access the DHCP server, I will create the necessary VLANs and configure the DHCP server's IP address as the DHCP helper address for each VLAN, thereby enabling device communication with the server.
The first step will involve establishing inter-VLAN routing on the Layer 3 switches. Subsequently, I will verify that each department’s PCs can automatically receive an IP address from the DHCP server. Next, I will configure the DNS server and assign the server’s IP address to all relevant DHCP pools. Following the configuration of the DNS server, I will verify on each PC that it has successfully obtained the DNS server address and is able to resolve domain names to IP addresses.
<p align="center">
Step Nr.8 : Inter-VLAN, DNS  : <br/>
<img src="https://i.imgur.com/UptOWyd.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<img src="https://i.imgur.com/JWiAj53.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<img src="https://i.imgur.com/JE5VOQt.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<img src="https://i.imgur.com/TUuDUs8.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<img src="https://i.imgur.com/h6JRtiX.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<img src="https://i.imgur.com/BXSZDYH.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<br />
Step Nr.9: Verification and Testing of Configuration, in the final step, i will verify that each department can communicate with one another, and ensure that guest wireless laptops can connect to the Wi-Fi, obtain IP and DNS addresses via DHCP, and successfully access the network.
I will then perform a ping test from the admin department to the wireless PCs to confirm interconnectivity. Once all tests are successfully completed and all devices are able to communicate as intended, the configuration process will be considered fully successful, and the bank's network project will be deemed complete.
<p align="center">
Step Nr.9 : Verification and Testing of Configuration : <br/>
<img src="https://i.imgur.com/QEMl1Wg.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/qqRdbDC.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/Mw7Pqau.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/p565kio.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/bKzMc2d.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/B8BMiSM.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/X27plfw.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/j4bhzlD.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/CxZ80cb.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/q50uMuN.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/RNEl9lw.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<br />
Step Nr.9.1 : Final Diagram and Accomplishment : <br/>
<img src="https://i.imgur.com/XJ7ELyf.png" height="80%" width="80%" alt="Lab Steps Nr.9.1"/>



 
<br />


</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
