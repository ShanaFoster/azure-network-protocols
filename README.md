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
Image above is showing the images of the resource group, Virtual Network, and both Window and Linux Virtual Machine being created. Need correctionhjjajhh
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

The above image shows Remote Desktop being accessed the public IP address obtained from the Windows virtual machine. Anthother image shows Wireshark being instlled using Windows 64-bit version. Wreshark is used to monitor network traffic going in and out of both virtual machines. The final image is shows the Wireshark protocol analyzer open, displaying packet captures including spam traffic, before a specific filter is applied.
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
The Wireshark protocol analyzer images above shows specific packet captures, including ICMP which doesn't use a port; SSH which is port 22 and is known as the secure port; DHCP which uses port 67 and 68, DNS which uses port 53; and Remote Desktop which uses TCP port 3389.
</p>
<br />

<img src="https://i.imgur.com/D8X5O0Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/mTyLqR0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above images show the command-line output of NSlookup and Ping coomands executed in Powershell.

</p>
<br />
<img src="https://i.imgur.com/DKPi6Eb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above image is shows a rule being created to block incoming traffic to the Windows Virtual Machine.To do this, I navigate to Microsoft Azure, opened the Linux Virtual Machine, went to Network > Network Setting > Network Security Group > Linux VM NSG > Inbound Security Rules, and add a new rule.  The execution of this rule was then observed in Powershell.

</p>
<br />
