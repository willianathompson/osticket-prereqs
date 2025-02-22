<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
  
<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create a Windows 10 virtual machine in Azure
- Install IIS, PHP and MySQL
- Create a MySQL database for osTicket
- Download and install osTicket
- Run the osTicket installer

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/ac3d3b27-3647-4895-878d-d12b5022d593)



<p>
1
Sign in to Azure and create a virtual machine (VM) within a resource group. Choose Windows 10 as the opeating system and select the VM size, region and configure a username and password to access the VM. Ensure the Public IP Address is enabled as it will be required. Set up Remote Desktop Protocol (RDP) access to connect to the windows VM. Use the Public IP Address for your VM to connect to the VM through the RDP.  
</p>
<br />

![image](https://github.com/user-attachments/assets/48e85edf-df81-42d6-afa9-1fd62e8b0af1)

</p>
<p>
2
Install IIS (Internet Information Services) through the control panel > programs and features > Turn Windows features on or off. Check the IIS and click okay to install the IIS. IIS will be sep up on the Windows 10 VM.


Install PHP

Install PHP:
Download PHP from the official PHP for Windows page. Choose the thread-safe version (VC15 x64) for Windows.
Extract the downloaded PHP ZIP file to a folder, e.g., C:\PHP.
Edit the php.ini file (make a copy of php.ini-development as php.ini), and enable the required extensions such as mysqli, pdo_mysql, and mbstring.
In IIS, configure PHP by adding the PHP handler via IIS Manager under Handler Mappings.
Verify PHP is working by creating a phpinfo.php file in the wwwroot folder (usually located at C:\inetpub\wwwroot) with the following content:
php
Copy
<?php
phpinfo();
?>


Open a browser and go to http://your-vm-ip/phpinfo.php. If PHP is configured correctly, you’ll see the PHP information page.
Install MySQL:
Download and install MySQL from the official MySQL website.
Choose the MySQL Server version and follow the installation steps to set up MySQL.
Once installed, configure MySQL and set the root password.

  
  
  
  
  
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![image](https://github.com/user-attachments/assets/02860ecb-626e-49d8-9000-cfb58d4e6fba)

</p>
<p>
3
  
Create a MySQL Database for osTicket
Log into MySQL: Open MySQL Command Line Client and log in with your root password.
bash
Copy
mysql -u root -p


Create the osTicket Database:
sql
Copy
CREATE DATABASE osticket;
CREATE USER 'osticket_user'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON osticket.* TO 'osticket_user'@'localhost';
FLUSH PRIVILEGES;


Replace osticket_user and password with your chosen username and password.

</p>
<br />

![image](https://github.com/user-attachments/assets/31cf31c0-7d5e-49f1-82a4-a5b5ab0ed2bc)

</p>
<p>
4
  
Download and Install osTicket
Download osTicket: Go to the osTicket download page and download the latest stable version.
Extract osTicket Files: Extract the downloaded osTicket ZIP file to C:\inetpub\wwwroot\osticket (or any preferred directory in your IIS web root).
Set Permissions: Ensure the include, attachments, and upload directories are writable by the web server (IIS).
Right-click the folder, select Properties, then go to the Security tab and give Full Control to the IIS_IUSRS group.

</p>
<br />

![image](https://github.com/user-attachments/assets/94771711-7c1b-4ed7-b4b4-622891ae71ab)

</p>
<p>
5
  
 Run the osTicket Installer
Access the osTicket Installer: Open a browser and navigate to http://your-vm-ip/osticket to start the installation.
Follow the Installation Steps:
The osTicket installer will check for the necessary PHP and MySQL configurations.
Database Configuration: Enter the database details (Database name osticket, Database user osticket_user, and the password you set earlier).
Admin User Setup: Set up the Admin Email, Timezone, and create your Admin Username and Password for the osTicket admin dashboard.
Finalize Installation: Complete the installation process, and osTicket will be ready for use.
Post-Installation:
Delete the setup folder: For security reasons, after the installation is complete, delete the setup directory from the osTicket installation folder.
Test the system: Log in to the Admin Panel and verify ticket creation, email integration, and the overall functionality of osTicket.


</p>
<br />

![image](https://github.com/user-attachments/assets/e90b4022-cc29-4577-a8d3-7f9859f33b2b)

</p>
<p>
Optional Step: Set Up Domain Name and SSL
If you want to use a custom domain (e.g., support.yourdomain.com), set up the DNS records to point to your Azure VM's public IP. You can also set up an SSL certificate using Let’s Encrypt or purchase an SSL certificate for secure communication.

</p>
<br />

![image](https://github.com/user-attachments/assets/ca39c679-fd31-438c-ab31-4d9d840c09ff)


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
