
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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Web Server
- Microsoft Azure
- osTicket
- PHP
- MySQL

<h2>Installation Steps</h2>

<p>
To start, we will create a virtual machine(VM) in the Microsoft Azure Portal. The virtual machine is great to use to run a separate computing environment. When creating the VM, the resource group will title as "osTicket",the image will be set to "Windows 10 Pro, version 22H2 - x64 Gen2", and select any size as long as it has at least two virtual CPUs (vcpus). Also don't forget to create the desired username and password for the VM.
</p>
<br />

![osTicket1](https://github.com/user-attachments/assets/f08cc012-ea1b-433f-a163-47735140312c)


<p>
Next, we will connect our physical computer to connect with the VM using Remote Desktop Connection by copying and pasting the public PIv4 address.
</p>
<br />

![osTicket2](https://github.com/user-attachments/assets/9a40e320-9440-4a66-98b7-893889c68875)



<p>
After connecting to the virtual machine, you will begin enabling the Internet Information Services (IIS). The IIS can be used to host, deploy, and manage web applications. In this project, the IIS will act as web server to run on the virtual machine and it will be serving up the osTicket. Click on the Windows menu and type "control panel" to access it then select "Uninstall a program" under the Programs section. Off to the left, select "Turn windows features on or off". A list of features will appear, you will enable the IIS with CGI
</p>
<br />

![image](https://github.com/user-attachments/assets/2378df14-d711-4ec4-bfb2-ace2f053ab70)



<p>
From the “osTicket-Installation-Files” folder, we will install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi and the Rewrite Module (rewrite_amd64_en-US.msi). Then create the directory C:\PHP. After creating the directory, we will unzip the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder then install the VC_redist.x86.exe and the MySQL 5.5.62 (mysql-5.5.62-win32.msi).   
</p>
<br /> 

![image](https://github.com/user-attachments/assets/693b975f-3b29-46ff-89b0-4abd71a3e67b) 



<p>
To install the osTicket, extractadn copy the "upload" folder into  “c:\inetpub\wwwroot” then rename the foldr to osTicket
</p> 
<br /> 

![image](https://github.com/user-attachments/assets/e62aafbf-094b-48cf-83bb-89db3ed7b659) 



<p>
 Next, open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.  
</p> 
<br /> 

![image](https://github.com/user-attachments/assets/629df2b0-8f72-4e47-8db7-e59d35922400)

