
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<!-- <h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- osTicket-Installation-Files.zip
- Install / Enable IIS in Windows WITH CGI
- Install the PHP Manager and Rewrite Module
- Create directory C:\PHP. From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 into C:\PHP
- Install VC_redist.x86.exe and MySQL 5.5.62
- Register PHP from within IIS
- Install osTicket v1.15.8
- Open osTicket Installer
- Enable Extension
- Rename and Assign Permissions: ost-config.php
- Setting up osTicket in the browser
- Install HeidiSQL
- Continute setting up osTicket in browser


<h2>Installation Steps</h2>

<p>
  <img width="1209" alt="Screenshot 2025-06-12 at 6 39 46 PM" src="https://github.com/user-attachments/assets/8090bf97-fcdc-441f-9cb0-29ab1302a296" />
</p>
<p>
Download osTicket-Installation-Files.zip onto computer, then Unzip folder. The files in this folder are used to install osTicket and some of the dependencies.
</p>
<br />

<p>
  <img width="395" alt="Screenshot 2025-06-12 at 6 51 53 PM" src="https://github.com/user-attachments/assets/e0c0e8b1-1fb0-4efe-a68e-92c1926d3eed" />
</p>
<p>
Enable Internet Information Services with CGI. 
</p>
<br />

<p>
  <img width="198" alt="Screenshot 2025-06-12 at 7 00 34 PM" src="https://github.com/user-attachments/assets/9b976099-3f12-4c82-8f79-de3e297de565" />
</p>
<p>
Installed the PHP Manager and Rewrite Module. 
</p>
<br />

<p>
  <img width="907" alt="Screenshot 2025-06-12 at 7 08 57 PM" src="https://github.com/user-attachments/assets/95d7d8fb-0115-4e2e-92ad-664f9bddb23e" />
</p>
<p>
Created directory C:\PHP. From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 into C:\PHP
</p>
<br />

<p>
  <img width="140" alt="Screenshot 2025-06-12 at 7 18 58 PM" src="https://github.com/user-attachments/assets/04195723-4123-4913-8f94-f15b3f8828fe" />
  <img width="116" alt="Screenshot 2025-06-12 at 7 17 55 PM" src="https://github.com/user-attachments/assets/5fd89ca3-e4bb-4b5e-9ea1-54d88e9ee0f0" />
</p>
<p>
From the "osTicket-Installation-Files" folder install VC_redist.x86.exe and MySQL 5.5.62. For MySQL,Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration -> 
</p>
<br />

<p>
  <img width="519" alt="Screenshot 2025-06-12 at 7 25 08 PM" src="https://github.com/user-attachments/assets/629e7821-6774-49be-a5e4-c3e38a87577d" />
<img width="203" alt="Screenshot 2025-06-12 at 7 26 03 PM" src="https://github.com/user-attachments/assets/e068086d-845d-452d-a826-0e6fa282faf3" />

</p>
<p>
Open IIS as an Admin, Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe). Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
 <img width="438" alt="Screenshot 2025-06-12 at 7 34 38 PM" src="https://github.com/user-attachments/assets/5c216898-418c-421c-9a6c-b9e0193276bc" />
 <img width="439" alt="Screenshot 2025-06-12 at 7 35 03 PM" src="https://github.com/user-attachments/assets/049664d0-cd0d-4359-a22c-abd485cd91ff" />
</p>
<p>
From the "osTicket-Installation-Files" folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”. Within “c:\inetpub\wwwroot”, Rename “upload” to "osTicket". 
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
  <img width="200" alt="Screenshot 2025-06-12 at 7 39 53 PM" src="https://github.com/user-attachments/assets/3a23e87a-4e67-4ae6-b45e-e57fb2ab3555" />
  <img width="199" alt="Screenshot 2025-06-12 at 7 40 01 PM" src="https://github.com/user-attachments/assets/81c5f70e-981a-497b-a447-330996458216" />
</p>
<p>
On IIS, Go to sites -> Default -> osTicket On the right, click “Browse *:80”. osTicket Installer should open on a web page. 
</p>
<br />

<p>
<img width="443" alt="Screenshot 2025-06-12 at 7 50 18 PM" src="https://github.com/user-attachments/assets/885dca34-6a29-49c1-9f8e-e516c7e7f96d" />
<img width="829" alt="Screenshot 2025-06-12 at 7 50 24 PM" src="https://github.com/user-attachments/assets/55528854-4526-45ab-8860-a7bbde91d188" />
</p>
<p>
Some Extensions are not enable. On IIS, go to sites -> Default -> osTicket. Double-click PHP Manager. Click “Enable or disable an extension”. Enable: php_imap.dll , php_intl.dll , php_opcache.dll Refresh the osTicket site in your browser, observe the changes
</p>
<br />

<p>
<img width="153" alt="Screenshot 2025-06-12 at 7 55 52 PM" src="https://github.com/user-attachments/assets/002b4aaf-9a83-4be8-b107-42f7eea06cce" />
<img width="116" alt="Screenshot 2025-06-12 at 7 56 15 PM" src="https://github.com/user-attachments/assets/dda2000a-5977-49a4-9890-959ecb83c9e5" />
<img width="366" alt="Screenshot 2025-06-12 at 8 03 52 PM" src="https://github.com/user-attachments/assets/4f62efcf-9d8e-40b4-a11d-72230daa2325" />
</p>
<p>
Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php Assign Permissions: ost-config.php Disable inheritance -> Remove All New Permissions -> Everyone -> All(Don't do this in real life)
</p>
<br />

<p>
 <img width="831" alt="Screenshot 2025-06-12 at 8 11 52 PM" src="https://github.com/user-attachments/assets/99f582d1-a312-42e3-9a0c-48cf9899832a" />
</p>
<p>
Continue setup in osTicker web browser. Don't install just yet.
</p>
<br />

<p>
<img width="187" alt="Screenshot 2025-06-12 at 8 19 23 PM" src="https://github.com/user-attachments/assets/cfdfe64b-1c90-45da-ad59-870e69ae38cd" />
<img width="278" alt="Screenshot 2025-06-12 at 8 23 50 PM" src="https://github.com/user-attachments/assets/23170e84-2681-4ff9-b9ca-8f39a278ff9c" />
</p>
<p>
From the "osTicket-Installation-Files" folder, install HeidiSQL. Once installed, Open Heidi SQL, Create a new session root/root , Connect to the session, Create a database called “osTicket”
</p>
<br />

<p>
<img width="827" alt="Screenshot 2025-06-12 at 8 26 47 PM" src="https://github.com/user-attachments/assets/9360bd62-156c-4297-a013-ee15c9ca50c4" />
</p>
<p>
Continue Setting up osTicket in the browser. MySQL Database: osTicket. MySQL Username: root MySQL Password: root Click “Install Now!”
</p>
<br />
