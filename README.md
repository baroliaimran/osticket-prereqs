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
Step 4: Go to the C Drive, and create a "PHP" folder. Next, extract the contents of the "php-7.3.8..." zip file into the C:\PHP\ folder. I'm using 7.3.8, however, on "https://windows.php.net/download/", you can get the latest version.
</p>
<br />

<p>
Step 5: Install VC Redistributable. Simple install, no extra steps here. The link is here: https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170. 
</p>
<br />

<p>
Step 6: Install MySQL. Simple install, no extra steps here. The link is here: https://www.mysql.com/downloads/. I used v5.5.62 in this tutorial, but you can download the latest version from the link provided.
</p>
<br />

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3
</p>
<br />
