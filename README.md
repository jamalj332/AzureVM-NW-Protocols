<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Inspecting Traffic in Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machines
- Remote Desktop
- Command-Line Tools(ping, ipconfig)
- Wireshark 
- Various Network Protocols-(SSH, TCP, DHCP, ICMP)

<h2>Operating Systems Used </h2>

- Windows 10
- Ubuntu Server

<h2>Objectives</h2>

- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic
- Observe TCP == 39 Traffic

<h2></h2>

<p>
</p>
<p>
Two virtual machines(VMs)-Microsoft 10 and Ubuntu-were created.
</p>
<br />

<p>
<img src="https://i.imgur.com/w2FjOYl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To monitor the ICMP traffic between two virtual machines, Wireshark was installed on a Windows 10 virtual machine. The private IP address of an Ubuntu virtual machine was retrieved and pinged from within the Windows 10 virtual machine. The ping requests and replies were then observed in Wireshark and the command line ping activity was monitored in the Windows 10 virtual machine.

</p>
<br />

<p>
<img src="https://i.imgur.com/SsYlNMb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the Windows 10 virtual machine, Wireshark was used to filter for SSH traffic. From the Windows 10 virtual machine, SSH was used to access the Ubuntu virtual machine using its private IP address. The SSH traffic was then observed in Wireshark.Is is also possible tp log  into the Ubuntu virtual machine from the command line in the Windows virtual machine to observe additional traffic.


</p>
<br />

<p>
<img src="https://i.imgur.com/LjarY7e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Filter for "DHCP" traffic. From within the Windows 10 virtual machine, issue a new IP address using the command line by typing "ipconfig /renew." This will allow you to observe DHCP traffic in Wireshark.

</p>
<br />

<p>
<img src="https://i.imgur.com/eGygRWe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To view TCP traffic in Wireshark, filter for "tcp port== 3389" and observe the constant traffic that is shown in the Windows 10 virtual machine due to the remote connection to the VM. This traffic includes mouse strokes, keyboard clicks, and other activity in the VM.





</p>
<br />
