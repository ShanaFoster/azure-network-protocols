<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)
- Ubuntu Server 22.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/2CxRgP9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/m76BLYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zSlbHka.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<img src="https://i.imgur.com/EnFHWU8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/4XIdlWV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Image above is showing the images of the resource group, Virtual Network, and both Window and Linux Virtual Machine being created.
</p>
<br />

<p>
<img src="https://i.imgur.com/IGXT8Fb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 </p>
<p> 
<img src="https://i.imgur.com/34syu6n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<p>
  
<img src="https://i.imgur.com/wotubUC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
<img src="https://i.imgur.com/34qQUah.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The above image shows Remote Desktop being navigated with the public IP address I got from the Windows virtual machine. Also an image of the wireshark being instlled with Windows 64 bit. Wireshark is used to view traffic going in and out from both virtual machine. The other image is showing Wireshark protocol analyzer being open and packet capture is be shown with all the spams before a specific filter is be performed.
</p>
<br />
<p>
<img src="https://i.imgur.com/aVAPD1V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
<img src="https://i.imgur.com/GsnJh5c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
<img src="https://i.imgur.com/8qoieze.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 </p>
<p>
<img src="https://i.imgur.com/tehrqDN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
<img src="https://i.imgur.com/Sgtf17u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The Wireshark protocol analyzer images above is showing specific packet capture of ICMP that does have a port, SSH which is port 22 and is also know as the secure port. Then we have a capture for DHCP port 67 and 68, DNS port 53 and Remote Desktop port tcp port 3389.
</p>
<br />

<img src="https://i.imgur.com/D8X5O0Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/mTyLqR0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above images show the command line for NSlookup and Ping performed in Powershell.

</p>
<br />
<img src="https://i.imgur.com/DKPi6Eb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above image is showing a rule being created to block coming traffic from going to the Windows Vitural Machines.To do this I had to navigate to Microsoft Azure, open the Linux Virtual Machine, navigate network, network setting, network security group, Linux VM NSG, setting inbound security rules then add rule and watching the rule be executed in Powershell.

</p>
<br />
