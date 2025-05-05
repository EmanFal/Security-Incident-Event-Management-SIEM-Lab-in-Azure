<h1>Security Incident Event Management SIEM Lab in Azure</h1>

<h2>Content</h2>

- <b>Description</b> 
- <b>Languages and Utilities Used</b>
- <b>Program walk-through</b>
   - <b>Creating VM</b>
   - <b>Viewing Raw Logs</b>
   - <b>Logs Analytics Workspace</b>
   - <b>Location Data</b>
   - <b>Attack Map Creation</b>

<h2>Description</h2>
In this lab I set up a basic security operations centre (SOC) in Azure. I created a virtual machine (VM), and opened it to the internet to act as a honeypot, then forwarded logs to a central repository. I then used Microsoft Sentinel to analyse real-world attack data.
<br />


<h2>Environments Used </h2>

- <b>Windows 11</b>
- <b>PowerShell</b>
- <b>Azure Portal</b>
- <b>Azure Sentinel</b> 

<h2>Program walk-through:</h2>

<p align="center">
Create the Honey Pot: After creating an Azure account, access the portal and create a Windows 10 virtual machine.<br/>

<img src="https://imgur.com/9zMEjEz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/qSDOm5Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Access the Network Security Group and create a rule that allows all traffic to gain unrestricted access to the VM
<img src="https://imgur.com/D62IMHx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Using 'Remote Desktop Connection App, log into the VM and disable firewalls to increase its susceptibility to attacks ' : <br/>
<img src="https://imgur.com/RLX6Cyq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/hUSSaZa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here you can view raw logs on the VM such as failed login attempts:  <br/>
<img src="https://imgur.com/w0znJvv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/K7hj2Rf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure a log repository, via the log analytics workspace, to forward the VM logs into:  <br/>
<img src="https://imgur.com/JTVQvMJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a sentinal workbook which will be linked to the log analytics workspace, and access the failed log attempts from the repository:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
