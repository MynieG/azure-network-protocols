<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/4NmKWF4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Windows 10 Virtual Machine (VM)
While creating the VM, select the previously created Resource Group
While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet
Create a Linux (Ubuntu) VM

</p>
<br />

<p>
<img src="https://i.imgur.com/jAKQudn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Use Remote Desktop to connect to your Windows 10 Virtual Machine
Within your Windows 10 Virtual Machine, Install Wireshark


</p>
<br />

<p>
<img src="https://i.imgur.com/9isB8zu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Observe ICMP Traffic
Open Wireshark and filter for ICMP traffic only
Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM

</p>
<br />


<img src="https://i.imgur.com/KHpM4Wn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Observe SSH Traffic
From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)
Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark

</p>
<br />


<img src="https://i.imgur.com/HQayzj9.png" height)="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Observe DHCP Traffic
From your Windows 10 VM, attempt to issue your VM a new IP address from the command line ipconfig /renew

</p>
<br />


<img src="https://i.imgur.com/9isB8zu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Observe DNS Traffic
From your Windows 10 VM within a command line, use nslookup to see what google.com IP address is 
Observe the DNS traffic being show in WireShark


</p>
<br />


<img src="https://i.imgur.com/9isB8zu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Observe RDP Traffic
Open Wireshark and filter for ICMP traffic only
Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM

</p>
<br />

