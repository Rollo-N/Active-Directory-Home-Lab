<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
A hands-on lab simulating a small corporate network. Using Oracle VirtualBox, I deployed a Windows Server VM and configured it as a domain controller running Active Directory Domain Services. I then used a PowerShell script that programatically built over a thousand user accounts and joined a client VM to the domain to validate authentication.
<br />


<h2>Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows 10 ISO</b> (21H2)
- <b>Server 2019 ISO</b> (21H2)
- <b>VirtualBox</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Create and open the first VM: <br/>

  <img width="1700" height="1000" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/a420bf58-29ff-4f27-a864-078b0e70c137" />




<br />
<br />
I set up two NICs. One for the outside internet and the other for the internal network  :  <br/>
<img width="1920" height="1200" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/ed98887e-5a5e-4fb4-a845-a285c92e6540" />


<br />
<br />
Installed Active Directory Domain Services and created a domain: <br/>
<img width="1920" height="861" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/3469fdd7-7dcd-4559-b697-7edfd2ea4b61" />


<br />
<br />
Set up a DHCP Server on our Domain Controller VM:  <br/>

<img width="1920" height="1200" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/3344de93-d8fc-4c15-a143-232879802e9c" />


<br />
<br />
Ran PowerShell script creating over 1000 users:  <br/>
<img width="1920" height="1200" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/3870610d-bc25-45c2-97a0-c45f8ee04116" />



<br />
<br />
Set up Windows 10 on a differnet VM for "Client" and checked internet was working properly:  <br/>
<img width="1755" height="906" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/6bb9cf37-96bc-45f4-b960-d54ee75406ad" />


<br />
<br />
Signed in using my "corporate" credentials and ran whoami and see that I am a member of mydomain:  <br/>
<img width="1920" height="933" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/a414f1fd-3705-4186-bfee-58139d2f266e" />







<!--
 ```diff
- text in red
+ text in green
