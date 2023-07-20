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

<h2>Prerequisites</h2>

- Create an account in Microsoft Azure and add an Azure subscription
- Create a Resource Group and name it RG-osTicket ![create_a_resource_group](https://github.com/Annelys08/osticket-prereqs/assets/139095349/a6af5f73-8b97-4df1-b2ab-73b3430159a8)
- Make a Virtual Machine and allow it to create a new virtual network and subnet
- In Remote Desktop, use the Public IP address that was created to connect to Virtual Machine (make sure to log in with the username and password you created when making the virtual machine) 
 ![create_a_virtualmachine](https://github.com/Annelys08/osticket-prereqs/assets/139095349/63d938d2-52de-41dd-b24c-65adc877cca8)

![remotedesktopconnection](https://github.com/Annelys08/osticket-prereqs/assets/139095349/01ef2fb7-48d5-4228-8159-87c333ea4a46)
- Install the Prerequisites for the OsTicketing System

<h2>Installation Steps</h2>

Once the virtual machine is open, right-click the start menu, select run, and type control. Next, you click Programs and turn Windows features on or off to go through the features and select Internet Information Services, World Wide Web Services, Application Development features, CGI, and Common HTTP features(make sure the rest of the boxes below are also checked) then press OK. This Installs IIS which is a web server.

![image](https://github.com/Annelys08/osticket-prereqs/assets/139095349/be2c714c-a65e-4fe3-91f1-68f7d26c40c2)

Next, we will install PHP Manager and open the file when it's done downloading. Repeat with the Rewrite Module and the PHP 7.3.8 file. After, open file explorer and search Windows (C:) and create a new folder named PHP. In this new folder created, you will extract all the files that are in PHP 7.3.8 file. Then you will install Microsoft Visual C++, MySQL, and osTicket. In IIS you should enable a few extensions in the osTicket section and click on the PHP Manager which are the following (the website should look like this after you have enabled the extensions): 
1. Enable: php_imap.dll
2. Enable: php_intl.dll
3. Enable: php_opcache.dll

![image](https://github.com/Annelys08/osticket-prereqs/assets/139095349/939cf0dc-5b0a-4da1-8809-8334a982adb1) 

On the OsTicket web page, fill in the information it is requesting. Before you continue, you must install the HeidiSQL file. When you finish installing, create a database called " osTicket" and then finish filling in the MySQL section with the username as root and the password as Password1. You should have the same result below:


![image](https://github.com/Annelys08/osticket-prereqs/assets/139095349/6e01729d-df6d-409a-a3b3-ef7a4a20d154)

Just to make sure you were successful at completing the installation, login to the link that says " Your osTicket URL:" on the bottom of the web page. 
