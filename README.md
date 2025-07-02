<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<!-- <h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install/Enable IIS with CGI
- Install PHP Manager for IIS
- Install the Rewrite Module
- Create PHP directory
- Install VC Redistributable
- Install MySQL


<h2>Prerequisite Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/11e38f10-c687-42f2-95cf-b9c644a60fa6" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
First step is to go to Control Panel > Programs > Programs and Features. Then on the left side, click "Turn Windows Features on or off".
In the window that pops up, scroll down to Internet Information Services and open the drop-down. Then open the drop-down for World Wide Web Services, then open the drop-down for Application Development Features. Here, you will check the box for CGI.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/27236822-a452-4ac4-95e0-1420d278a5ff" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For reference, above are a list of the executables and zip files you will need for the rest of the procedure.
</p>
<br />

<p>
Step 2: Install PHP Manager for IIS. Simple install, no extra steps here. The link is here: https://github.com/RonaldCarter/PHPManager/releases/tag/V1.5.0
</p>
<br />

<p>
Step 3: Install the Rewrite Module. Simple install, no extra steps here. The link is here: https://www.iis.net/downloads/microsoft/url-rewrite. Scroll down to the bottom to download the version you need (x86 or x64). You can also choose the language.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/630f6abd-4c12-42d0-b7a8-725df23f4a05" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Go to the C Drive, and create a "PHP" folder. Next, extract the contents of the "php-7.3.8..." zip file into the C:\PHP\ folder. I'm using v7.3.8, however, on "https://windows.php.net/download/", you can get the latest version.
</p>
<br />

<p>
Step 5: Install VC Redistributable. Simple install, no extra steps here. The link is here: https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170. 
</p>
<br />

<p>
Step 6: Install MySQL. The link is here: https://www.mysql.com/downloads/. I used v5.5.62 in this tutorial, but you can download the latest version from the link provided.
</p>
<p>
The install is simple, however, you need to configure it further. Check the box that says "Launch Configuration..." after the install is complete, and follow the images below to complete the configuration.
</p>
<p>
<img src="https://github.com/user-attachments/assets/67579c17-c87d-4789-8a74-d81b1cd40e98" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/a619d0a1-6412-4eca-9b1d-5b2f962bc138" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here you want to put a secure password. I used "root" as an example, but a more secure password is ideal. 
</p>
<p>
<img src="https://github.com/user-attachments/assets/b4e2e9df-0a7c-4f4b-907b-0b121db22a58" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Step 7: Download the zip file for osTicket: https://osticket.com/download/
</p>
<p>
Step 8: Download the executable for HeidiSQL: https://www.heidisql.com/download.php
</p>
<br />

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/f5d39da4-b701-4600-8e5a-7542de657648" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1) Open IIS as an Administrator and double-click on PHP Manager. 
</p>
<p>
<img src="https://github.com/user-attachments/assets/814818fe-c97a-45b7-8b96-f6b629f0c46a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2) Click "Register new PHP version" under PHP Setup.
</p>
<p>
<img src="https://github.com/user-attachments/assets/104e127a-b67c-42a5-8b45-0be4d4386e54" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3) Open the path where php-cgi.exe is located (see image above)
</p>
<p>
<img src="https://github.com/user-attachments/assets/a6584169-57c0-4ecd-91e8-d7030b27aaa7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4) Once that's done, go back to the main page of IIS, right click on the top-level connection, and click "Stop" then click "Start".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ab14d1ae-d51e-46e6-94b3-83e57a6f5c7c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5) Now, extract the osTicket installation files onto the desktop (or anywhere where you can find the folder easily).
</p>
<p>
6) Open the extracted folder and copy the folder named "upload".
</p>
<p>
<img src="https://github.com/user-attachments/assets/8b09c73b-d02f-4045-96d7-85a2724be8f9" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7) Go to C:\inetpub\wwwroot\ and paste the "upload" folder there. Once copied, rename the folder to "osTicket" with a capital T. 
</p>
<p>
<img src="https://github.com/user-attachments/assets/e9fd0531-8f4c-4b72-a8b6-877ea0b7838b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/f0d60e1d-b178-4456-879b-781777df3ea7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/0b8d9c1a-8ef7-4ce4-823d-36d98cbafec2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8) Go back to IIS, locate the osTicket folder on the left side of the window (in the cascading list), and click it. Look on the right and it should show "Browse *:80 (http)". Click on it to be redirected to the OS Ticket installer page on your web browser.
</p>
<p>
<img src="https://github.com/user-attachments/assets/1d53a127-bb6f-4375-b836-336cbb8cce57" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9) You'll notice some extensions listed at the bottom that are marked with a red X. Go back to IIS\osTicket, double-click PHP Manager, and click on "Enable or disable an extension" at the bottom.
</p>
<p>
<img src="https://github.com/user-attachments/assets/6fcb69aa-051f-4cb6-ab3f-da49a52f7d8c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10) Look in the list and enable the following:
</p>
<p>
10a) php_imap.dll
</p>
<p>
10b) php_intl.dll
</p>
<p>
10c) php_opcache.dll
</p>
<p>
<img src="https://github.com/user-attachments/assets/414d94c4-0865-4ea8-852a-d53ada95b3a0" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11) Once that is done, go back and refresh the osTicket Installer page. It will now give an error of a missing config file. Go back to C:\inetpub\wwwroot\osTicket and go into the folder named "include". Scroll down to "ost-sampleconfig.php" and rename it to "ost-config.php".
</p>
<p>
<img src="https://github.com/user-attachments/assets/8c3cc736-0c1f-4a28-b64c-0911ede0b315" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12) After renaming the file, right-click it to open the Properties, and go to the Security tab. Once there, click "Disable Inheritance" at the bottom, click "Remove all inherited permissions from this object".
</p>
<p>
<img src="https://github.com/user-attachments/assets/14fdf30d-abf1-40c2-818d-63fd0c5a3531" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13) Now, in the same Security Tab, click Add. In the pop-up, type in "Everyone". This will allow everyone to be able to make changes to this .php file. DO NOT DO THIS. I am only doing this so as to get the ball rolling in a secure environment. Naturally, please take into account your company's security detail when making any changes!
</p>
<p>
<img src="https://github.com/user-attachments/assets/6cf4c1ad-4fc4-4fca-a793-39bd3436addb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14) If all went well, you should see the image above.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/74504ec4-89bf-4a46-bfe8-b5f3d803262a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15) You can start filling out stuff, but you'll get stuck near the bottom, which requires a database login and password. This is so that we have a database to store all the tickets.
</p>
<p>
<img src="https://github.com/user-attachments/assets/9d4799fc-892d-4932-ab78-7dfee2b71cc1" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
16) Go back to the HeidiSQL installer and double-click it. It's a simple install. Once you install it, double-click it to open it.
</p>
<p>
<img src="https://github.com/user-attachments/assets/23bbba2e-4df8-4e71-a258-1d8baecf6f5b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
17) Earlier, we made a password when configuring MySQL. Bring that password back here.
</p>
<p>
<img src="https://github.com/user-attachments/assets/93479912-0cb0-4edd-a2fb-3272e59bac43" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
18) Now, create a new database and call it "osTicket".
</p>
<p>
<img src="https://github.com/user-attachments/assets/d1e6ec0b-d2a5-4130-b8b9-973944b821f7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
19) Go back to the osTicket Installer webpage and type in the name of the database (osTicket), and the username and password associated with it.
</p>
<p>
<img src="https://github.com/user-attachments/assets/bc856f16-3fb0-405b-a08b-cf00091f182f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
20) This is what the end result should be.
</p>
<p>
<img src="https://github.com/user-attachments/assets/81074ee0-fcfd-4836-8d2e-c85200c779cc" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
21) To confirm, you can go back to HeidiSQL and see all the data added to the osTicket database.
</p>
<p>
<img src="https://github.com/user-attachments/assets/b15eea56-db5c-4424-9711-39248c5d7253" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
22) Go to "localhost/osTicket/scp/login.php", and login using the Username and Password used when installing osTicket. 
</p>
<p>
<img src="https://github.com/user-attachments/assets/cde003bd-61c0-4210-ab43-27ef7c58c4df" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
23) This is what will be shown on the "Agent Panel". You can click "Admin Panel on the top right to go and view a different set of tabs (further explained in the next part of the osTicket tutorial).
</p>
<p>
<img src="https://github.com/user-attachments/assets/01962166-4d38-41b5-bade-97826fde034e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
24) If you go to "localhost/osTicket" you'll see the site where any user can submit a ticket request. 
</p>
<p>
25) And that's all! You've now installed osTicket!
</p>
<br />
