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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create a Windows 10 virtual machine in Azure
- Install IIS, PHP and MySQL
- Create a MySQL database for osTicket
- Download and install osTicket
- Run the osTicket installer

<h2>Installation Steps</h2>
</p>
<p>

</p>
<br />
<h4>Create a Windows 10 virtual machine in Azure</h4>

![image](https://github.com/user-attachments/assets/5235455c-130b-43d3-9615-51a1cae68b2a)

</p>
<p>
  
The Windows 10 Virtual Machine is created in Azure with the appropriate VM size, region, and configuration settings. Public IP is enabled, and RDP access is set up for remote connection. The VM is deployed and ready for use. Use the link below to download the latest osTicketinstallation.zip files to the desktop and extract all.
</p>
  
[link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

</p>
<p>

</p>
<br />
<h4>Install IIS, PHP and MySQL</h4>

![image](https://github.com/user-attachments/assets/2d837218-60f7-4f58-9985-8ce9eb4eba10)

</p>
<p>
On your Windows 10 VM, go to Control Panel > Programs and select Turn Windows features on or off. Ensure that Internet Information Services, World Wide Web Services, and CGI are all checked. IIS will then be ready to serve web content.
</p>
<p>

![image](https://github.com/user-attachments/assets/90583efe-5dcf-4da9-80ce-396c488f29f4)

</p>
<p>
Check the loopback IP address (127.0.0.1) in your web browser to verify that IIS is ready.
</p>
<p>

![image](https://github.com/user-attachments/assets/ca704747-6847-4f3a-9b08-d1d0ba66dbf0)

</p>
<p>

From the extracted osTicket files, install PHP Manager using the installer in the PHP Manager folder.

</p>
<p>
  
![image](https://github.com/user-attachments/assets/c31473b0-cc6d-42aa-8ab0-988d1b42dba6) 

</p>
<p>
  
Create a new folder named PHP for the compressed PHP files. Navigate to 'This PC > Windows (C:) > PHP' and extract all the files from the compressed PHP folder.

</p>
<p>

![image](https://github.com/user-attachments/assets/133df083-fdde-4c4c-9daf-2680db99663a)

</p>
<p>
Navigate back to the installation folder and install Microsoft Visual C++.
</p>
<p>
  
![image](https://github.com/user-attachments/assets/5a225435-901c-4f26-a22f-c4b4836c13de)

  </p>
<p>
Install MySQL from the installation folder and make sure to select the Standard Configuration during the setup.

</p>
<p>

</p>
<br />
<h4>Create a MySQL database for osTicket</h4>

![image](https://github.com/user-attachments/assets/290794a5-ce80-43a5-8bdb-19b04cdb7db7)

</p>
<p>
During the MySQL installation setup, it is important to set up a root username and password for the database connection. Select the default username 'root', choose a password, and proceed with the installation.

 </p>
<p> 

![image](https://github.com/user-attachments/assets/0c72235c-6009-41c3-8479-4dccf41cbfd8)

</p>
<p>
Navigate to the Start menu, search for IIS, open it as an administrator, and click on PHP Manager.

</p>
<p>

![image](https://github.com/user-attachments/assets/beefab68-5528-487f-bda8-10e72cfdc04d)

</p>
<p>
  
Select Register New PHP Version, browse to the PHP folder on the C: drive, select the php-cgi file, click OK, and then click Start/Stop in IIS.

</p>
<p>

</p>
<br />
<h4>Download and install osTicket</h4>

![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)

</p>
<p>
Navigate to the installation folder and extract the osTicket folder, which will contain two folders: scripts and upload. Copy the upload folder to Windows (C:) > inetpub > wwwroot and rename it to "osTicket". Then, start/stop in IIS.
</p>
<p>

![image](https://github.com/user-attachments/assets/e197f3ef-466f-4c00-ad4a-4fc295d17e71)

</p>
<p>
Go to IIS Server > Sites > Default > osTicket, click on PHP Manager, then select PHP Extensions. Click Enable or Disable Extension and enable the following: php_imap, php_intl, and php_opcache. Finally, refresh IIS. Navigate to Windows (C:) > inetpub > wwwroot > osTicket > include, find the ost-sampleconfig.php file and rename it to ost-config.php.
</p>
<p>

![image](https://github.com/user-attachments/assets/65504b4f-3ded-4954-bc27-01ce1a2415fd)

</p>
<p>
Right-click the ost-config.php file, select Properties, remove all inheritance, click Add, select Principal, type "admin", and apply Full Control.
</p>
<p>

![image](https://github.com/user-attachments/assets/cc248045-c37d-44a8-bb6b-39333da3080f)

</p>
<p>
Go to the installation folder on the desktop, install, and launch HeidiSQL. In HeidiSQL, click New, enter the root username and password, then click Open. Click on Unnamed, and create a new database named osTicket.

</p>
<p>

</p>
<br />
<h4>Run the osTicket installer</h4>

![image](https://github.com/user-attachments/assets/8bf64098-7af3-438b-ab43-ab3f203d9324)

</p>
<p>
Go to IIS Server > Sites > Default > osTicket, and click on Browse *:80 (http). This will open a new tab in the browser with the osTicket welcome page.
</p>
<p>

![image](https://github.com/user-attachments/assets/31cf31c0-7d5e-49f1-82a4-a5b5ab0ed2bc)

</p>
<p>
Navigate to the osTicket site in your browser, click Continue, and enter the Help Desk Name, Default Email, Admin Name, Email Address, Username, and Password. In the Database Settings, enter osTicket for the database name, along with the root username and password, then click Install. 
<br>
After installation, the setup folder should be deleted for security, and the system was tested by logging into the Admin Panel to ensure ticket creation, email integration, and other features worked correctly.
  </p>
<p>
<br>
  
[osTicket: Post-Installation Configuration](https://github.com/willianathompson/osticket-Post-Install-Config)


