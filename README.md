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

![image](https://github.com/user-attachments/assets/5235455c-130b-43d3-9615-51a1cae68b2a)


</p>
<p>
The Windows 10 Virtual Machine was successfully created in Azure, with the appropriate VM size, region, and configuration settings. Public IP was enabled, and RDP access was set up for remote connection. The VM was deployed and is ready for use.  
</p>
<br />

![image](https://github.com/user-attachments/assets/f7ed5859-f8d2-491b-b333-d71bd9d1fc87)
![image](https://github.com/user-attachments/assets/ca704747-6847-4f3a-9b08-d1d0ba66dbf0)
![image](https://github.com/user-attachments/assets/5a225435-901c-4f26-a22f-c4b4836c13de)
![image](https://github.com/user-attachments/assets/c31473b0-cc6d-42aa-8ab0-988d1b42dba6)

</p>
<p>
  
IIS, PHP, and MySQL were successfully installed on the Windows 10 VM. IIS was turned on using the "Turn Windows features on or off" settings. PHP was downloaded and extracted to the C:\PHP folder, then configured by editing files like php_imap, php_ini, and php_opcache to enable the needed extensions. MySQL was installed, set up, and the root password was created for secure database access.

</p>
<br />

![image](https://github.com/user-attachments/assets/cbb716c1-0d07-450f-ab93-de974437beba)
![image](https://github.com/user-attachments/assets/b1a74234-381a-493c-bdee-f3782a0c6ec6)
![image](https://github.com/user-attachments/assets/0c72235c-6009-41c3-8479-4dccf41cbfd8)

</p>
<p>
  
The MySQL database for osTicket was successfully created. The "osticket" database was set up, and a user called "labuser" was given full access to it with the specified password. The privileges were refreshed to make sure everything worked properly and the user had the correct access.

</p>
<br />

![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)
![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)


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



</p>
<p>

</p>
<br />




