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

 <b>Install / Enable IIS in Windows WITH CGI</b>  

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
 Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe) and reload IIS (Open IIS, Stop and Start the server)
</p>
<p>
 
</p>
