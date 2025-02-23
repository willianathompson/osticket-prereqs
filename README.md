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

![image](https://github.com/user-attachments/assets/f7ed5859-f8d2-491b-b333-d71bd9d1fc87)
![image](https://github.com/user-attachments/assets/ca704747-6847-4f3a-9b08-d1d0ba66dbf0)
![image](https://github.com/user-attachments/assets/5a225435-901c-4f26-a22f-c4b4836c13de)
![image](https://github.com/user-attachments/assets/c31473b0-cc6d-42aa-8ab0-988d1b42dba6)

</p>
<p>
IIS, PHP, and MySQL were successfully installed on the Windows 10 VM. IIS was enabled through the "Turn Windows features on or off" settings. PHP was downloaded, extracted to the C:\PHP folder, configured by editing the php.ini file to enable necessary extensions, and verified by accessing the phpinfo.php page in the browser. MySQL was installed, configured, and the root password was set for secure database access.
</p>
<br />

![image](https://github.com/user-attachments/assets/cbb716c1-0d07-450f-ab93-de974437beba)
![image](https://github.com/user-attachments/assets/b1a74234-381a-493c-bdee-f3782a0c6ec6)
![image](https://github.com/user-attachments/assets/0c72235c-6009-41c3-8479-4dccf41cbfd8)

</p>
<p>
The MySQL database for osTicket was successfully created. The database `osticket` was initialized, and a user `osticket_user` with the specified password was granted all privileges to the database. The necessary privileges were flushed to ensure proper access and functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)
![image](https://github.com/user-attachments/assets/896e6336-40f7-477d-a4bb-797264a881b6)


</p>
<p>
The latest stable version of osTicket was downloaded and extracted to the C:\inetpub\wwwroot\osticket directory on the IIS web root. Permissions were set to ensure the `include`, `attachments`, and `upload` directories were writable by the web server, granting Full Control to the IIS_IUSRS group for proper functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/8d5f5e23-e28f-48f3-920c-5fa0dd52641b)
![image](https://github.com/user-attachments/assets/c44619b9-dd44-45f2-9bf2-b5f8d0bbf188)



</p>
<p>
The osTicket installer was successfully run by navigating to http://your-vm-ip/osticket in the browser. During installation, the necessary PHP and MySQL configurations were verified, and the database details (osticket, osticket_user, and the set password) were entered. The Admin user setup was completed with the creation of an Admin Username, Password, and Email, along with setting the Timezone. After finalizing the installation, the setup folder was deleted for security, and the system was tested by logging into the Admin Panel to verify ticket creation, email integration, and overall functionality.
</p>
<br />



</p>
<p>

</p>
<br />




