<h1>Packet Sniffing with Wireshark: Createing filters</h1>

<h2>Description</h2>
Packet Sniffing with Wireshark: Create Your First Filters, will help a security analyst who is looking to use packet sniffing with Wireshark to capture, display, and observe specific HTTP and HTTPS packets.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux</b> 
- <b>Wireshark</b>

<h2>Environments Used </h2>

- <b>Linux</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Install wireshark using command - sudo apt install wireshark: <br/>
<img src="https://i.imgur.com/MHYugWj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Limit the user privledges of wireshark, and any program that does not need it to prevent issues in future:  <br/>
<img src="https://i.imgur.com/gQ0P2mS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add user to the wireshark group to add packet capture capablities using the command - sudo usermod -aG wireshark $USER  - Goal of all these steps
  is to prevent wireshark from being a superuser, and causing damage to the system: <br/>
<img src="https://i.imgur.com/Kt2c0Zq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open wireshark, and click ens5 as an example. To start capturing packets click the blue shark fin. To stop click the red rectangle, from there captured packets can be saved for later review:  <br/>
<img src="https://i.imgur.com/e1beTXb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Apply filter in order to capture https packets - tcp.port==443:  <br/>
<img src="https://i.imgur.com/Zoj3T1s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Doubleclick desired packet to get detailed information:  <br/>
<img src="https://i.imgur.com/0e8nNOu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
You can use the tls.handshake.type==1 command to show only client hellos, and destination ip address of the first one will be open page example for this was google.com: 
  You can also use ip.addr followed by an ip adress to filter for all packets involving said ip adress. You can use ip.src/ip.dst to find all packets orgininating or going to for ip.dst from a source adress. <br/>
<img src="https://i.imgur.com/PoML6T6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
You can use keywords such as and, or, ! to apply additional filters:  <br/>
<img src="https://i.imgur.com/CaLqcG5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
