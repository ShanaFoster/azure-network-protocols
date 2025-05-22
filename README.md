<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, ICMP)
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
The image above shows the creation of Resource Group, Virtual Network, and both Windows and Linux Virtual Machines. To create a Resource Group, I navigated to "create resource group" in Microsoft Azure, provided a name, selected a region, then reviewed and created it. To create the Virtual Machines, I went to Virtual machines, selected "create" named Resource Group, the Virtual Machine, chose region, select image , specified the VM size, create Username and Password, Selected Virtual Machine (VNet), and then reviewed and created the VMs.
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

The above image shows Remote Desktop being accessed with the public IP address obtained from the Windows virtual machine. Another image shows Wireshark being instlled using Windows 64-bit version. Wireshark is used to monitor network traffic going in and out of  virtual machines. The final image shows the Wireshark protocol analyzer open, displaying packet captures including spam traffic, before a specific filter is applied.
</p>
<br />
<p>

<img src="https://i.imgur.com/2d5j3ie.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
The Wireshark protocol analyzer images above display specific packet captures: ICMP Internet Control Message Protocol): Used for network ping and doesn't use a port; SSH (Secure Shell): A protocol used for secure remote login. It uses TCP port 22, known also as a secure port. DNS (Domain Name System): Used to resolve domain names into IP addresses, it uses UDP port 53 but can also uses TCP port for larger queries.DHCP(Dynamic Host Configuration Protocol): Used for assiging IP addresses. It uses UDP port 67 (Server) and 68 (client). RDP(Remote Desktop Protocol): Enable remote access to another computer overa nework. Ut uses TCP port 3389.
</p>
<br />

<img src="https://i.imgur.com/D8X5O0Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/mTyLqR0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above images show the command-line output of NSlookup and Ping commands executed in Powershell.

</p>
<br />
<img src="https://i.imgur.com/DKPi6Eb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
The above image is shows a rule being created to block incoming traffic to the Windows Virtual Machine.To do this, I navigate to Microsoft Azure, opened the Linux Virtual Machine, went to Network > Network Setting > Network Security Group > Linux VM NSG > Inbound Security Rules, and add a new rule.  The execution of this rule was then observed in PowerShell and Wireshark. 

</p>
<br />

<img src="https://i.imgur.com/DvnxYv4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
The image above show the Linux machine's private IP address being used to initiate a ping coomand from within the Windows VM using PowerShell. The above display also show the ping traffic in Wireshark. This ping command is used to test connection between the two machine.

</p>
<br />


