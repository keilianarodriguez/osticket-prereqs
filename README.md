# osticket-prereqs
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

- IIS & Management Console
- PHP and Rewrite Module
- MySQL
- HeidiSQL
- osTicket

<h2>Installation Steps</h2>

1. Azure Virtual Machine Creation:
Created an Azure Virtual Machine with Windows 10 and 4 vCPUs named "Vm-osticket" with the username "login" and password "Password1!". Signed into Remote Desktop Protocol, with the Public IP address. 

<p>
<img src="https://imgur.com/qH00Yog.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/gLLYor7.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>



2. Install/Enable IIS and Components:
Installed IIS in Windows with CGI, Common HTTP Features, and IIS Management Console enabled.
<br />

https://imgur.com/uPhLElu
https://imgur.com/i8vglHu
https://imgur.com/nnVLUxd
https://imgur.com/1qXOBVr
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

3. Install PHP Manager for IIS and Rewrite Module:
Downloaded and installed PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) and the Rewrite Module (rewrite_amd64_en-US.msi).
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

https://imgur.com/J28xNWX
https://imgur.com/9ON6qp5

5. Configure PHP:
Created the directory C:\PHP and downloaded PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip), then unzipped its contents into C:\PHP.
Installed VC_redist.x86.exe.

https://imgur.com/jzED3pY
https://imgur.com/CY8ES70
https://imgur.com/gHVf83l
https://imgur.com/RNS9xN8


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

5. Install MySQL:
Downloaded and installed MySQL 5.5.62 (mysql-5.5.62-win32.msi) with the standard configuration and password "Password1".
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

https://imgur.com/B7TZ3zX
https://imgur.com/0ucO65U
https://imgur.com/0nzD0Dk
https://imgur.com/JvCdJoE

6. Configure IIS and PHP:
Opened IIS as an admin, registered PHP within IIS, and reloaded IIS.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

https://imgur.com/oeeecxt
https://imgur.com/ZINCvQW
https://imgur.com/CG0j4y3




7. Install osTicket:
Downloaded osTicket from the installation files folder, extracted and copied the "upload" folder to c:\inetpub\wwwroot, then renamed it to "osTicket".
Reloaded IIS.

https://imgur.com/lVAp7cl
https://imgur.com/sarTqbB
https://imgur.com/ohiJWqc



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

8. Enable PHP Extensions:
Opened "Browse *.80 (http)" Enabled php_imap.dll, php_intl.dll, and php_opcache.dll in PHP Manager within IIS.
Refreshed the osTicket site in the browser.

https://imgur.com/f3xCwhu
https://imgur.com/H6qWZl4
https://imgur.com/iGRB0oG
https://imgur.com/9eyPHtR



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

9. Rename Configuration File and Set Permissions:
Renamed ost-sampleconfig.php to ost-config.php and set permissions to Everyone -> All.

https://imgur.com/Z8W14aq
https://imgur.com/tq70phB
https://imgur.com/PswzNGA


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

10. Continue Setting up osTicket:
Continued setting up osTicket in the browser, configuring the helpdesk name and default email.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

https://imgur.com/PswzNGA
https://imgur.com/8m5z3ac


11. Install HeidiSQL and Create Database:
Downloaded and installed HeidiSQL, created a new session with root/Password1, connected to the session, and created a database called "osTicket".



12. Finish osTicket Setup:
Completed the osTicket setup in the browser, specifying the MySQL database, username, and password, then clicked "Install Now!".

https://imgur.com/ry2qldA
https://imgur.com/gsaAcPN

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

13. Access osTicket:
Accessed the help desk login page at http://localhost/osTicket/scp/login.php.

https://imgur.com/Yg1HL7q 
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

14. Clean Up:
Deleted the setup folder and set permissions to "Read" only for ost-config.php.
Congratulations! The installation and setup of osTicket should be complete without errors.
