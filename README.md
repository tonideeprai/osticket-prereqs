<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br/>
* This lab is done using a virtual machine in Azure (<a href="google.com" styl>my showcase</a>) *

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Prerequisites</h2>

- Download the [file](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0) and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
- We will use the files in this folder to install osTicket and some of the dependencies.


<h2>Installation Steps</h2>

<p>
  1. Go to Control Panel > Under Programs, clicked "Uninstalled Program, then clicked "Turn Windows features on or off"
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 17 34 PM" src="https://github.com/user-attachments/assets/26df1379-954c-4f56-ad59-7392fb8ced29">
</p>
<p>
  2. Expand "Internet Information Services" > "World Wide Web Services" > "Application Development Features", then check "CGI" box<br>
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 29 35 PM" src="https://github.com/user-attachments/assets/7e0549af-c296-495d-bac6-721fde8fd4ac">
  <img width="70%" alt="Screenshot 2024-10-07 at 2 44 08 PM" src="https://github.com/user-attachments/assets/34000ac6-d671-4d1a-9b8c-61fb4bb30672">
</p>
<p>
  3. From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)<br>
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 59 26 PM" src="https://github.com/user-attachments/assets/53a08925-aea6-4cfe-af3d-becb5d68b026"><br>
  <img width="70%" alt="Screenshot 2024-10-07 at 3 00 31 PM" src="https://github.com/user-attachments/assets/5eb324ab-c18f-477b-bc5c-2ac26961038c">
</p>
<p>
 4. From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-07 at 4 34 15 PM" src="https://github.com/user-attachments/assets/5253b294-e5a0-42e9-aabb-3bf2293ad108">
<img width="70%" alt="Screenshot 2024-10-07 at 4 35 16 PM" src="https://github.com/user-attachments/assets/eb2bbec6-80de-4b4a-9f4d-7df9d466e796">
</p>
<p>
 5. Create the directory C:\PHP, then from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-07 at 4 40 10 PM" src="https://github.com/user-attachments/assets/907b898a-01e3-4067-b033-f3580f3db8eb">
</p>
<p>
 6. From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-07 at 4 46 26 PM" src="https://github.com/user-attachments/assets/503cc703-a69b-4f94-a240-3449de8a2836">
 <img width="70%" alt="Screenshot 2024-10-07 at 4 47 17 PM" src="https://github.com/user-attachments/assets/2b28e7fa-d1f5-44b7-9b7a-cc5c1c0bca28">
</p>
<p>
 7. From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-07 at 4 50 15 PM" src="https://github.com/user-attachments/assets/00c35fc7-4b17-49d3-844b-219e50780b18">
<img width="70%" alt="Screenshot 2024-10-07 at 4 51 34 PM" src="https://github.com/user-attachments/assets/a26c23f9-dfc6-4082-90f3-6c6d794afca1">
<img width="70%" alt="Screenshot 2024-10-07 at 4 53 12 PM" src="https://github.com/user-attachments/assets/b5294a96-c766-4f30-9e70-405d04ea05b9">
</p>
<p>
  8. Configuration Wizard window will pop up after you finish the installation, continue instaling Wizard
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-07 at 4 57 52 PM" src="https://github.com/user-attachments/assets/3269ca81-2d86-479b-83a8-738d1380705e">
<img width="70%" alt="Screenshot 2024-10-07 at 4 59 15 PM" src="https://github.com/user-attachments/assets/699bc23e-857b-4abd-9212-8406531b580f">
<img width="70%" alt="Screenshot 2024-10-07 at 5 02 35 PM" src="https://github.com/user-attachments/assets/91038e20-fe45-4eb2-987c-10182a7cf569">
<img width="70%" alt="Screenshot 2024-10-07 at 5 06 47 PM" src="https://github.com/user-attachments/assets/ab4b75ac-6b30-478d-990c-45e6555efbdf">
</p>
<p>
 9. Open IIS as an Admin<br>
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-12 at 7 43 25 PM" src="https://github.com/user-attachments/assets/fade4bd9-0c71-452d-9955-d7ac15e54e6c">
</p>
<p>
 10. Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe) and reload IIS (Open IIS, Stop and Start the server)
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-12 at 7 48 21 PM" src="https://github.com/user-attachments/assets/dc507a81-cc30-4a83-abad-1315ee34d304">
<img width="70%" alt="Screenshot 2024-10-12 at 7 50 01 PM" src="https://github.com/user-attachments/assets/dd23bd8d-668f-4480-bd81-f0aea99c315e">
<img width="70%" alt="Screenshot 2024-10-12 at 7 52 41 PM" src="https://github.com/user-attachments/assets/855832fe-e2a9-4167-a734-d8395bdf9f9e">
<img width="70%" alt="Screenshot 2024-10-12 at 7 57 34 PM" src="https://github.com/user-attachments/assets/7ea31853-7658-4860-b5ee-1a00ce754016">
</p>
<p>
 11. From the “osTicket-Installation-Files” folder, Extract “osTicket-v1.15.8.zip” and copy the “upload” folder inside it into “c:\inetpub\wwwroot”<br>
  Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”<br>
</p>
<p>
 <img width="70%" alt="Screenshot 2024-10-12 at 8 19 25 PM" src="https://github.com/user-attachments/assets/22e7fdd5-8622-4ea3-9d47-6b5a4e60174a">
<img width="70%" alt="Screenshot 2024-10-12 at 8 25 08 PM" src="https://github.com/user-attachments/assets/2ff14406-4345-49e6-8298-0966d4127662">
<img width="70%" alt="Screenshot 2024-10-12 at 8 37 47 PM" src="https://github.com/user-attachments/assets/e9bfba7f-c48c-4600-8759-8dc50f4ca7d0">
</p>
<p>
 12. Restart IIS again
</p>
<p>
 13. Load the osTicket site<br>
 - In IIS, GO to sites > Default Web Site > osTicket > click 'Browse *:80 (http) 
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-13 at 8 19 57 AM" src="https://github.com/user-attachments/assets/163d8363-8ace-4ddc-a5ed-e89c5ba94ed5">
</p>
<p>
  Note that some extensions are not enabled
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-13 at 8 23 13 AM" src="https://github.com/user-attachments/assets/b9020b5a-e637-4f54-852b-b3e0957d611f">
</p>
<p>
  14. Go back to IIS and double-click PHP Manager in Sites -> Default -> osTicket<br>
  Click “Enable or disable an extension”<br>
  Find these extensions, right-click > Enable<br>
 - Enable: php_imap.dll<br>
 - Enable: php_intl.dll<br>
 - Enable: php_opcache.dll<br>
 Refresh the osTicket site in your browser, observe the changes<br>
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-13 at 8 39 49 AM" src="https://github.com/user-attachments/assets/51ca1f11-3824-4ce0-8461-e1507b77e3ac">
<img width="70%" alt="Screenshot 2024-10-13 at 8 41 47 AM" src="https://github.com/user-attachments/assets/f159a38c-6a9f-466a-adcb-dede0810ab54">
</p>
<p>
  After enabling the extension
</p>
<p>
  <img width="1512" alt="Screenshot 2024-10-13 at 5 03 38 PM" src="https://github.com/user-attachments/assets/53ab9874-6719-40ef-a9bb-46d944319fbe">
</p>
<p>
  15. From: C:\inetpub\wwwroot\osTicket\include<br>
  - Find "ost-sampleconfig.php" file<br>
  - Rename it to "ost-config.php"
</p>
<p>
  <img width="70%" alt="Screenshot 2024-10-13 at 5 07 49 PM" src="https://github.com/user-attachments/assets/e9af7bf3-513c-40d7-83ea-550a259affd9">

</p>
