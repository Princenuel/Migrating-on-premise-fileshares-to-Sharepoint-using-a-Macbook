<h1> Migrating-on-premise-fileshares-to-Sharepoint-using-a-Macbook </h1>


<h2>Description</h2>
In this project, I successfully demonstrated the migration of on-premise file shares to SharePoint using a MacBook. The project showcases a step-by-step approach to transitioning from traditional file shares to a cloud-based collaboration platform, highlighting the benefits of enhanced security, scalability, and remote accessibility.

<br />


<h3>Environments Used </h3>

- <b>Windows 10 IS0 </b>
- <b> Virtual Box </b>
- <b>Microsoft 365 Admin Center</b> 
<br />


<h2>Program walk-through:</h2>

- install virtualbox on your Macbook

 <p align="center">
install virtualbox on your Macbook: <br/>
<img src="https://i.imgur.com/pdLmKUr.png" height="80%" width="80%" alt="Install VM"/>
<br />

   
- Download the Windows 10 ISO

 <p align="center">
<b>Download the Windows 10 ISO (64bit)</b>: <br/>
<img src="https://i.imgur.com/ZpG2p5Z.jpg" height="80%" width="80%" alt="windows 10 ISO"/>
<br />

   
- Now we have the virtualbox and the ISO file, next you run the virtualbox and Right-click the virtual machine and select the Settings option

 <p align="center">
<b>Right-click the virtual machine and select the Settings option:</b> <br/>
<img src="https://i.imgur.com/jtWLvV4.png" height="80%" width="80%" alt="VMbox"/>
<br />


- Click on Storage.
- Under the “Storage Drives” section, select the disc (Empty) item.

 <p align="center">
<b>Under the “Storage Drives” section, select the disc (Empty) item</b> <br/>
<img src="https://i.imgur.com/L3ljikb.png" height="80%" width="80%" alt="VMbox"/>
<br />


- Under the “Attributes” section, click the disc icon and select the “Choose a disk file” button.
- Select the ISO file.
- Click the Open button
- load the windows 10 ISO file into the Virtual Box
- CLICK ON OK


<p align="center">
Windows 10 64bits running on your virtual machine: <br/>
<img src="https://i.imgur.com/t9TvkLx.png" height="80%" width="80%" alt="Windows 10 on VM"/>
<br />

<br />

- Now using goto office.com on your browser and login to your tenant where you have admin privileges for sharepoint
- Goto sharepoint admin center and click on new site
- Ensure that your site has a document library where we will be migrating the on-premise fileshares to.


