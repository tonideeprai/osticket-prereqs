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
  <img width="70%" alt="Screenshot 2024-10-07 at 2 17 34 PM" src="https://github.com/user-attachments/assets/26df1379-954c-4f56-ad59-7392fb8ced29">
</p>
<p>
  2. Expand "Internet Information Services" > "World Wide Web Services" > "Application Development Features", then check "CGI" box<br>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 29 35 PM" src="https://github.com/user-attachments/assets/7e0549af-c296-495d-bac6-721fde8fd4ac">
</p>
<p>
  Should look like this when finished<br>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 44 08 PM" src="https://github.com/user-attachments/assets/34000ac6-d671-4d1a-9b8c-61fb4bb30672">
</p>
<p>
  3. From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)<br>
  <img width="70%" alt="Screenshot 2024-10-07 at 2 59 26 PM" src="https://github.com/user-attachments/assets/53a08925-aea6-4cfe-af3d-becb5d68b026"><br>
  Finised<br>
  <img width="70%" alt="Screenshot 2024-10-07 at 3 00 31 PM" src="https://github.com/user-attachments/assets/5eb324ab-c18f-477b-bc5c-2ac26961038c">
</p>
