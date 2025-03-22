<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install/Enable IIS in Windows WITH CGI
- Install PHP Manager
- Install the Rewrite Module
- Create the Directory C:\PHP
- Install VC_redist
- Install MySQL
- You can get these files [here](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

<h2>Installation Steps</h2>



</p>
<p></p>
Here I have all the prerequisites in one folder on my desktop.
<img src="https://i.imgur.com/vUced2W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<br />

<p>
1) open up Control Panel > Programs > Programs and Features > Turn Windows Features on or off
<img src="https://i.imgur.com/2gqawMt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
2) Once the "Windows Features" tab is open scroll down and turn on "Internet Information Services"
<img src="https://i.imgur.com/uPswiJf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
3) After you turn on IIS expand the services under IIS and navigate to World Wide Web Services -> Application Development Features -> [X] CGI
<img src="https://i.imgur.com/7YvLf56.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<p>
4) Next from the Prerequisites folder, Install "PHP Manager" for IIS
<img src="https://i.imgur.com/PFcxjVL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<p>
5) Next Install the Rewrite Module from the folder.
<img src="https://i.imgur.com/OxthjxR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<p>
6) Create a new folder called "PHP" in your Windows C drive.
<img src="https://i.imgur.com/PLMiH8B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
</p>
<p>
<p></p>
7) Unzip php-7.3.8 into the C:\PHP folder by right clicking the zipped folder then clicking "Extract All",
then clicking the "Browse" Button, then navigating to your Windows C drive, then finally selecting the "PHP" folder.
<p>
<p>
<p>
<p>
8) Next install VC redist.
<img src="https://i.imgur.com/XiJFhuN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<p>
9) Next install MySQL.
<p>
<img src="https://i.imgur.com/3AYeOYg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/CwjIhid.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/51rb4cU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/BVBaXoe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vUCyDbo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
10) Next Open IIS as admin by searching "IIS" in the windows search bar then clicking "Run as Administrator".
<img src="https://i.imgur.com/UTg8G4V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
11) Next Register PHP from within IIS.
<img src="https://i.imgur.com/2X8OkDR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/pI18mL6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wuKpD5K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/a2uVW1O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Z9HVHLt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
12) Reload IIS by right clicking the server and stopping it then starting it again.
<img src="https://i.imgur.com/xAwp61n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
13) Install osTicket by unzipping the folder. Then copy the "upload" folder into C:inetpub\wwwroot, THEN RENAME "upload" folder to "osTicket"
<img src="https://i.imgur.com/yrDqQr9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/crAm7GB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/stvXSoh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/qXxv5KF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
</p>
<p>
<p></p>
14) Reload IIS (refer to step 12)
<p>
<p>
<p>
<p>
15) load osTicket site within IIS. Go to sites -> Default -> osTicket -> Browse .80
<img src="https://i.imgur.com/l6rLiQY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
16) We are going to enable some extensions in ISS.
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
<img src="https://i.imgur.com/Wcz7LYp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/y0CXZNf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/InwZgID.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/eHkzS4q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MnqbFLn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
17) Rename: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  <p> 
    To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<p>
18) Continue Setting Up Os Ticket. Fill out information up until "Database Settings" then stop.
<img src="https://i.imgur.com/rpmkuEp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/N3M2KxI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
19) Install HeidiSQL located in the osTicket Installation files folder. Open HeidiSQL and create a new session. Enter in the username and password you created when installing MySQL then click "Open". Right Click "Unnamed" at the top left and click "Create New" then "Database". Name this EXACTLY "osTicket" then hit "Ok".
<img src="https://i.imgur.com/rpmkuEp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/N3M2KxI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/aopmfht.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/p9BGRiQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
20) Continue Setting Up Os Ticket in the browser. Fill out information for "Database Settings" then hit "Install Now"
<img src="https://i.imgur.com/PK7eDVi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hivBNsz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>
- All done! now you can go [here](http://localhost/osTicket/scp/login.php) and login


