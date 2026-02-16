<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
In this lab I'll be using Oracle Virtual Box to create an Active Directory home lab environment. I've used this lab to help develop my understanding of Active Directory and Windows Networking. 
<br />


<h2>Programs and Utilities Used</h2>

- <b>Oracle Virtual Box</b>
- <b>PowerShell</b> 
- <b>Active Directory</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>

<h2>Lab walk-through:</h2>

<p align="center">
Identify and label the two Network Connections on the Win Server 2019 VM: <br/>
<img src="https://i.imgur.com/MX781Sr.png" height="80%" width="80%" alt="Network Connections"/>
<br />
<br />
Renamed the PC to "DC" (Domain Controller) for accessibility purposes: <br/>
<img src="https://i.imgur.com/8HChP8W.png" height="80%" width="80%" alt="Renamed PC"/>
<br />
<br />
Configuring the "Internal" IPv4 network connection: <br/>
<img src="https://i.imgur.com/0xlq1QA.png" height="80%" width="80%" alt="Internal IPv4"/> <br/>
<i> IP Address - 172.16.0.1 | Subnet Mask - 255.255.255.0 | DNS Server Address - 127.0.0.1 </i> 
<br />
<br />
Installing Active Directory Domain Services: <br/>
<img src="https://i.imgur.com/cr4izBA.png" height="80%" width="80%" alt="AD Domain Services"/>
<img src="https://i.imgur.com/DC362V1.png" height="80%" width="80%" alt="AD Domain Services2"/>
<br />
<br />
</p>
