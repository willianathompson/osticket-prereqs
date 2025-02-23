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


![image](https://github.com/user-attachments/assets/5235455c-130b-43d3-9615-51a1cae68b2a)



<p>
The Windows 10 Virtual Machine was successfully created in Azure, with the appropriate VM size, region, and configuration settings. Public IP was enabled, and RDP access was set up for remote connection. The VM was deployed and is ready for use.  
</p>
<br />

![image](https://github.com/user-attachments/assets/30558d99-3f6c-4633-97fb-d845d4c1efd0)
![image](https://github.com/user-attachments/assets/be0dfbf0-ac84-483f-9fa8-d94de27e11d3)
![image](https://github.com/user-attachments/assets/b4d143ca-4545-4034-ab93-5db1ac816dde)
![image](https://github.com/user-attachments/assets/844de140-48b5-47cb-a422-e99e98bc3a38)


</p>
<p>
IIS, PHP, and MySQL were successfully installed on the Windows 10 VM. IIS was enabled through the "Turn Windows features on or off" settings. PHP was downloaded, extracted to the C:\PHP folder, configured by editing the php.ini file to enable necessary extensions, and verified by accessing the phpinfo.php page in the browser. MySQL was installed, configured, and the root password was set for secure database access.
</p>
<br />

![image](https://github.com/user-attachments/assets/119b37e9-3a84-4991-9f54-8cb9458dd5be)
![image](https://github.com/user-attachments/assets/9c8dceeb-5908-495b-a2c8-9775bc5373f0)


</p>
<p>
The MySQL database for osTicket was successfully created. The database `osticket` was initialized, and a user `osticket_user` with the specified password was granted all privileges to the database. The necessary privileges were flushed to ensure proper access and functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/d6fa2ebb-80e0-410b-9a49-9187f96e76ed)
![image](https://github.com/user-attachments/assets/9fa8f92a-4f62-4d92-ad56-127c4bc56f7a)


</p>
<p>
The latest stable version of osTicket was downloaded and extracted to the C:\inetpub\wwwroot\osticket directory on the IIS web root. Permissions were set to ensure the `include`, `attachments`, and `upload` directories were writable by the web server, granting Full Control to the IIS_IUSRS group for proper functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/c1ad9db6-fe35-48f6-8072-c6c3688e4a43)
![image](https://github.com/user-attachments/assets/1df63fd6-d332-452b-8129-5ad2332a3c2b)


</p>
<p>
The osTicket installer was successfully run by navigating to http://your-vm-ip/osticket in the browser. During installation, the necessary PHP and MySQL configurations were verified, and the database details (osticket, osticket_user, and the set password) were entered. The Admin user setup was completed with the creation of an Admin Username, Password, and Email, along with setting the Timezone. After finalizing the installation, the setup folder was deleted for security, and the system was tested by logging into the Admin Panel to verify ticket creation, email integration, and overall functionality.
</p>
<br />



</p>
<p>

</p>
<br />




