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
Promoting the Server to a Domain Controller: <br/>
<img src="https://i.imgur.com/9EvgGGI.png" height="80%" width="80%" alt="Promo to DC"/>
<img src="https://i.imgur.com/iSKVVkr.png" height="80%" width="80%" alt="New Forest"/>
<img src="https://i.imgur.com/FxtYAUR.png" height="80%" width="80%" alt="Installation"/>
<br />
<br />
Creating a Domain Admin Account: <br/>
<img src="https://i.imgur.com/DP7yqvP.png" height="80%" width="80%" alt="ADMINS OU"/> <br/>
<i> Created an Organizational Unit to store the Administrator Accounts </i> <br/> 
<img src="https://i.imgur.com/iQQd9Wc.png" height="80%" width="80%" alt="Admin Account"/> <br/>
<i> Created Administrator Account under the name John Snow </i> <br/>
<i> Username denoted a-john.snow to differentiate from regular user accounts added later </i> <br/> 
<img src="https://i.imgur.com/JGmNDsD.png" height="80%" width="80%" alt="Admin Account 2"/> 
<img src="https://i.imgur.com/d91MFdr.png" height="80%" width="80%" alt="Admin Account 3"/>
<br/>
<br/>
Installing Remote Access and Routing on the Domain Controller: <br/>
<img src="https://i.imgur.com/Pot7e5R.png" height="80%" width="80%" alt="RAS 1"/>
<img src="https://i.imgur.com/dhVHnqD.png" height="80%" width="80%" alt="RAS 2"/>
<img src="https://i.imgur.com/MCJqLr3.png" height="80%" width="80%" alt="RAS 3"/>
<br />
<br />
Configuring NAT on the Routing and Remote Access Server Setup: <br/>
<img src="https://i.imgur.com/or5CKiv.png" height="80%" width="80%" alt="NAT 1"/>
<img src="https://i.imgur.com/Lff7te9.png" height="80%" width="80%" alt="NAT 2"/>
<img src="https://i.imgur.com/wPVtXa3.png" height="80%" width="80%" alt="NAT 3"/>
<br />
<br />
Configuring DHCP on the Domain Controller: <br/>
<img src="https://i.imgur.com/sEZ1fSm.png" height="80%" width="80%" alt="DHCP 1"/>
<img src="https://i.imgur.com/SoaewpA.png" height="80%" width="80%" alt="DHCP 2"/>
<img src="https://i.imgur.com/7YEANSm.png" height="80%" width="80%" alt="DHCP 3"/>
<img src="https://i.imgur.com/Xcf2nOb.png" height="80%" width="80%" alt="DHCP 4"/>
<img src="https://i.imgur.com/pai2Nvh.png" height="80%" width="80%" alt="DHCP 5"/>
<img src="https://i.imgur.com/9W1HkUt.png" height="80%" width="80%" alt="DHCP 6"/>
<img src="https://i.imgur.com/4dNPQQo.png" height="80%" width="80%" alt="DHCP 7"/>
<img src="https://i.imgur.com/3ZJOFu7.png" height="80%" width="80%" alt="DHCP 8"/>
<img src="https://i.imgur.com/RK64t0O.png" height="80%" width="80%" alt="DHCP 9"/>
<img src="https://i.imgur.com/QLBuclI.png" height="80%" width="80%" alt="DHCP 10"/>
<br />
<br /> 
Creating Users in Active Directory: <br/>
<img src="https://i.imgur.com/SoRrqla.png" height="80%" width="80%" alt="User 1"/> <br/>
<i> Generated random first and last names from a website and stored them in names.txt file </i> <br/>
<img src="https://i.imgur.com/ceCqtYh.png" height="80%" width="80%" alt="User 2"/> <br/>
<i> Utilizing this script, I'm able to create Active Directory accounts for all the users inside the names.txt file </i> <br/>
<img src="https://i.imgur.com/1BAjKhj.png" height="80%" width="80%" alt="User 3"/> <br/>
<i> The list of users being created in Active Directory </i> <br/>  
<img src="https://i.imgur.com/t7Lbq16.png" height="80%" width="80%" alt="User 4"/> <br/>
<i> New users seen in Active Directory in the "_USERS" OU </i> <br/>  
<img src="https://i.imgur.com/FBJvRCn.png" height="80%" width="80%" alt="User 5"/> <br/>
<i> Searched for my John Snow account, regular user account and admin account successfully displayed </i> <br/>  
<br />
<br />
Adding a Client PC to the Domain: <br/>
<img src="https://i.imgur.com/ohDYRgQ.png" height="80%" width="80%" alt="Client 1"/> <br/>
<i> Added an Internal Network Adapter to the Client VM. DHCP on the DC will provide the IP Address. </i> <br/>
<img src="https://i.imgur.com/QpDiflZ.png" height="80%" width="80%" alt="Client 2"/> <br/>
<i> Opened ipconfig on cmd to check the DNS, Default Gateway and IP Address </i> <br/>
<img src="https://i.imgur.com/A5Bl8A7.png" height="80%" width="80%" alt="Client 3"/> <br/>  
<i> The client machine is connected to the Internet </i> <br/>  
<img src="https://i.imgur.com/bYtcCmk.png" height="80%" width="80%" alt="Client 4"/> <br/>  
<i> Client joining the Domain </i> <br/>  
<img src="https://i.imgur.com/CeR5WOc.png" height="80%" width="80%" alt="Client 5"/> <br/>
<img src="https://i.imgur.com/BlJY4SQ.png" height="80%" width="80%" alt="Client 6"/> <br/>  
<i> Client successfully joined the Domain </i> <br/>  
<br />
<br />  
</p>
