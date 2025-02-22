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
The Windows 10 Virtual Machine was successfully created in Azure, with the appropriate VM size, region, and configuration settings. Public IP was enabled, and RDP access was set up for remote connection. The VM was deployed and is ready for use.  
</p>
<br />

![image](https://github.com/user-attachments/assets/48e85edf-df81-42d6-afa9-1fd62e8b0af1)

</p>
<p>
IIS, PHP, and MySQL were successfully installed on the Windows 10 VM. IIS was enabled through the "Turn Windows features on or off" settings. PHP was downloaded, extracted to the C:\PHP folder, configured by editing the php.ini file to enable necessary extensions, and verified by accessing the phpinfo.php page in the browser. MySQL was installed, configured, and the root password was set for secure database access.
</p>
<br />

![image](https://github.com/user-attachments/assets/02860ecb-626e-49d8-9000-cfb58d4e6fba)

</p>
<p>
The MySQL database for osTicket was successfully created. The database `osticket` was initialized, and a user `osticket_user` with the specified password was granted all privileges to the database. The necessary privileges were flushed to ensure proper access and functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/31cf31c0-7d5e-49f1-82a4-a5b5ab0ed2bc)

</p>
<p>
The latest stable version of osTicket was downloaded and extracted to the C:\inetpub\wwwroot\osticket directory on the IIS web root. Permissions were set to ensure the `include`, `attachments`, and `upload` directories were writable by the web server, granting Full Control to the IIS_IUSRS group for proper functionality.

</p>
<br />

![image](https://github.com/user-attachments/assets/94771711-7c1b-4ed7-b4b4-622891ae71ab)

</p>
<p>
The osTicket installer was successfully run by navigating to http://your-vm-ip/osticket in the browser. During installation, the necessary PHP and MySQL configurations were verified, and the database details (osticket, osticket_user, and the set password) were entered. The Admin user setup was completed with the creation of an Admin Username, Password, and Email, along with setting the Timezone. After finalizing the installation, the setup folder was deleted for security, and the system was tested by logging into the Admin Panel to verify ticket creation, email integration, and overall functionality.
</p>
<br />

![image](https://github.com/user-attachments/assets/e90b4022-cc29-4577-a8d3-7f9859f33b2b)

</p>
<p>

</p>
<br />

![image](https://github.com/user-attachments/assets/ca39c679-fd31-438c-ab31-4d9d840c09ff)


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
