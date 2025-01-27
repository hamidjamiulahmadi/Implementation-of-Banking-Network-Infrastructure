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
Step Nr. 2.2 : VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/FYaiZNM.png" height="80%" width="80%" alt="Lab Steps Nr.2.2"/>
<img src="https://i.imgur.com/jHKW86d.png" height="80%" width="80%" alt="Lab Steps Nr.2.2"/>
<br />
Step Nr.3: Here, I will configure VLAN assignments, along with all access and trunk ports, and implement switch port security across all 12 switches. The Layer 3 switches connecting to each department switch will be set as trunk ports, and similarly, the Layer 2 switches connected to their respective department switches will be configured as access ports.
Step Nr.3 : VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/sVIqvSb.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/JE5427V.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/fVO6Xch.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/3TdbIVd.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<br />
Step Nr.3: Here, I will configure VLAN assignments, along with all access and trunk ports, and implement switch port security across all 12 switches. The Layer 3 switches connecting to each department switch will be set as trunk ports, and similarly, the Layer 2 switches connected to their respective department switches will be configured as access ports.
Step Nr.3 : VTY, Banner, lookup, password encryption : <br/>
<img src="https://i.imgur.com/sVIqvSb.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/JE5427V.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/fVO6Xch.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<img src="https://i.imgur.com/3TdbIVd.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<br />

 
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
