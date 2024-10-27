<h1>Performing a DoS Attack Using Smurf Attack</h1>


<h2>Description</h2>
<n>In this lab, we will conduct a DoS attack using the Smurf attack.</n>

A DoS (Denial of Service) Attack is an attack meant to shut down a network or a mahcine and make it inaccessible to its users. The Smurf Attack is a distributed denial-of-service (DDoS) attack in which large numbers of Internet Control Message Protocol (ICMP) packets with the intended victim's spoofed source IP are broadcast to a computer network using an IP broadcast address.

**NOTE:** The information provided here is for educational purposes only and should not be used to harm or disrupt systems or networks without proper authorization.
Unauthorized access to computer systems and networks is illegal and can result in severe penalties. Please use this information responsibly and ethically.
<br />

<h2> Languages and Utilities Used</h2>
-<b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows 16</b>

<h2>LAB walk-through:</h2>

<p align="center">
From the desktop, open "Wireshark": <br/>
<img src="https://i.imgur.com/7qMrkc9.png" height="80%" width="80%" alt="Wireshark Steps"/>
<br />
<br />
In the Wireshark Network Analyzer window, select LO1 and then from the menu bar, click capture and select start:  <br/>
<img src="https://i.imgur.com/KAmJOso.png" height="80%" width="80%" alt="Wireshark Network Analyzer window"/>
<br />
<img src="https://i.imgur.com/s2YApJa.png" height="80%" width="80%" alt="Capturing from LO1"/>
<br />
<br />
Minimize the Capturing from LO1 window and open the Windows PowerShell: <br/>
<img src="https://i.imgur.com/s4jM0JN.png" height="80%" width="80%" alt="PowerShell"/>
<br />
<br />
In the Windows PowerShell window, execute the following command to perform DoS attack:  <br/>
</br>
hyenae -I 1 -A 4 -a icmp-echo -s %-% -d %-192.168.137.7 -t 128 
< br/>
<img src="https://i.imgur.com/ekVKuHX.png" height="80%" width="80%" alt="DoS command"/>
<br />
<br />
From the taskbar, restore the Wireshark application and observe the traffic:  <br/>
<img src="https://i.imgur.com/Oy9W0Hm.png" height="80%" width="80%" alt="Wireshark analyzer window"/>
<br />
<br />
Go to the Windows PowerShell window and press CTRL+X to stop the attack, then close the PowerShell window:  <br/>
<img src="https://i.imgur.com/czLJ1tG.png" height="80%" width="80%" alt="Stopping the attack"/>
<br />
<br />
In the Capturing from LO1 window, from the menu bar, click the Stop capturing packets icon:  <br/>
<img src="https://i.imgur.com/bVxsW1q.png" height="80%" width="80%" alt="Stopping the capture of packets"/>
<br/>
<br/>
From the menu bar, click File and select Save As, in the dialog box, type the File name as dos_attack and click save
<br />
<img src="https://i.imgur.com/9z1DXNr.png" height="80%" width="80%" alt="File save"/>
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
