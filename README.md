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
<h3>Create a Virtual Machine in Azure</h3>

![image](https://github.com/user-attachments/assets/5235455c-130b-43d3-9615-51a1cae68b2a)

</p>
<p>
  
The Windows 10 Virtual Machine is created in Azure with the appropriate VM size, region, and configuration settings. Public IP is enabled, and RDP access is set up for remote connection. The VM is deployed and ready for use. Use the link below to download the latest osTicket.zip files to the desktop and extract all.
</p>
<p>
  
[link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
</p>
<br />

![image](https://github.com/user-attachments/assets/2d837218-60f7-4f58-9985-8ce9eb4eba10)

On your Windows 10 VM, go to Control Panel > Programs and select Turn Windows features on or off. Ensure that Internet Information Services, World Wide Web Services, and CGI are all checked. IIS will then be ready to serve web content.


![image](https://github.com/user-attachments/assets/90583efe-5dcf-4da9-80ce-396c488f29f4)

</p>
<p>
Check the loopback IP address (127.0.0.1) in your web browser to verify that IIS is ready.

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

Navigate back to the installation folder and install Microsoft Visual C++.
  
![image](https://github.com/user-attachments/assets/5a225435-901c-4f26-a22f-c4b4836c13de)
  
Install MySQL from the installation folder and make sure to select the Standard Configuration during the setup.


![image](https://github.com/user-attachments/assets/290794a5-ce80-43a5-8bdb-19b04cdb7db7)

During the MySQL installation setup, it is important to set up a root username and password for the database connection. Select the default username 'root', choose a password, and proceed with the installation.

 </p>
<p> 

![image](https://github.com/user-attachments/assets/0c72235c-6009-41c3-8479-4dccf41cbfd8)

Navigate to the Start menu, search for IIS, open it as an administrator, and click on PHP Manager.

</p>
<p>

![image](https://github.com/user-attachments/assets/beefab68-5528-487f-bda8-10e72cfdc04d)

</p>
<p>
  
Select Register New PHP Version, browse to the PHP folder on the C: drive, select the php-cgi file, click OK, and then click Start/Stop in IIS.

</p>
<br />


![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)

Navigate to the installation folder and extract the osTicket folder, which will contain two folders: scripts and upload. Copy the upload folder to Windows (C:) > inetpub > wwwroot and rename it to "osTicket". Then, start and stop IIS.






Go to IIS Server > Sites > Default > osTicket, click on PHP Manager, then select PHP Extensions. Click Enable or Disable Extension and enable the following: php_imap, php_intl, and php_opcache. Finally, refresh IIS.






![image](https://github.com/user-attachments/assets/cbb716c1-0d07-450f-ab93-de974437beba)
![image](https://github.com/user-attachments/assets/b1a74234-381a-493c-bdee-f3782a0c6ec6)


</p>
<p>










  
The MySQL database for osTicket was successfully created. The "osticket" database was set up, and a user called "labuser" was given full access to it with the specified password. The privileges were refreshed to make sure everything worked properly and the user had the correct access.

</p>
<br />

![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)

![image](https://github.com/user-attachments/assets/65504b4f-3ded-4954-bc27-01ce1a2415fd)

</p>
<p>

The latest stable version of osTicket was downloaded and extracted to the C:\inetpub\wwwroot\osticket directory on the IIS web server. Permissions were set to make sure the "include", "attachments", and "upload" folders were writable by the web server. Full Control was given to the IIS_IUSRS group to ensure everything worked correctly.

</p>
<br />

![image](https://github.com/user-attachments/assets/8d5f5e23-e28f-48f3-920c-5fa0dd52641b)
![image](https://github.com/user-attachments/assets/c44619b9-dd44-45f2-9bf2-b5f8d0bbf188)



</p>
<p>
  
The osTicket installer was successfully run by going to http://localhost/osTicket/scp/login.php in the browser. During the setup, the required PHP and MySQL settings were checked, and the database details (osticket, labuser, and the password) were entered. The Admin user was set up by creating an Admin username, password, and email, and selecting the correct timezone. After finishing the installation, the setup folder was deleted for security reasons. Finally, the system was tested by logging into the Admin Panel to make sure ticket creation, email integration, and everything else worked as expected.
  
</p>
<br />



