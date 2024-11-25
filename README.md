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

- Install / Enable IIS in Windows with CGI - World Wide Web Services -> Application Development Features -> [X] CGI
- From the installation files, download and install PHP Manager for IIS - (PHPManagerForIIS_V1.5.0.msi)
- From the installation files, download and install the Rewrite Module - (rewrite_amd64_en-US.msi)
- Create the directory C:\PHP
- From the installation files, download PHP 7.3.8 - (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP 
- From the installation files, download and install VC_redist.x86.exe. 
- From the installation files, download and install MySQL 5.5.62 - (mysql-5.5.62-win32.msi) - Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/kxxornI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8 - From the "osTicket-Instillation-Files" folder, unzip "osTicket-v1.15.8.zip" and copy the "upload" folder into "c:\inetpub\wwwroot". 
(Within "c:\inetpub\wwwroot", rename "upload" to "osTicket")
</p>
<br />

<p>
<img src="https://i.imgur.com/iMfbI8L.png" alt="Disk Sanitization Steps"/>
</p>
<p>
On IIS, go to sites -> Default -> osTicket, and click "Browse *:80" on the right side.
Double click PHP Manager and click "Enable or disable an extension". 
Enable "php_imap.dll",
Enable "php_intl.dll",
Enable "php_opcache.dll"
</p>
<br />

<p>
<img src="https://i.imgur.com/glDgNql.png" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to file explorer and find "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php"
Rename the "ost-sampleconfig.php" to "ost-config.php"
After renaming the file, right click on it and go to properties -> security -> advance
Disable the inheritance and select remove all inherited permissions from this object.
Next, click add -> Select a principal -> and type "Everyone" in the box.
Under basic permissions check Full control.
Click Apply and Ok
</p>
<br />
