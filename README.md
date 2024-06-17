<h1> Migrating-on-premise-fileshares-to-Microsoft-Sharepoint-using-a-Macbook </h1>


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

<p align="center">
From sharepoint admin center create a site where you will have the document library which will store our on-premise fileshares: <br/>
<img src="https://i.imgur.com/OuQEzmP.png" height="80%" width="80%" alt="Windows 10 on VM"/>
<br />

<br />

- Ensure that you create a communication site has a document library where we will be migrating the on-premise fileshares to.

 <p align="center">
<b>Creating a communication site:</b> <br/>
<img src="https://i.imgur.com/aC7D0EK.png" height="80%" width="80%" alt="VMbox"/>
<br />

<br />

 <p align="center">
<b>Parameters of the communication site:</b> <br/>
<img src="https://i.imgur.com/M851wXu.png" height="80%" width="80%" alt="VMbox"/>
<br />

<br />


<p align="center">
<b>communication site is ready:</b> <br/>
<img src="https://i.imgur.com/mFpxlQS.png" height="80%" width="80%" alt="VMbox"/>
<br />

<br />



<p align="center">
<b>Ensure that your Document library where you would migrate the on-premise fileshares to has been created on your sharepoint site:</b> <br/>
<img src="https://i.imgur.com/VqS2GiD.png" height="80%" width="80%" alt="VMbox"/>
<br />

<br />

<p>Now you have created your sharepoint site and your document library where we intend to move the fileshares to, its important to note that 
for the migration to be successful you have to be on the same network with the fileshare, so now since we are not physically present in the same location
with our fileshare another way to make that happen is to map the network on our virtual machine c: drive, and to do this you will need the socket url and admin logon credential of the on-premise fileshare. 

To map the drive take the following steps:</p>



<p align="center">
<b>Open File Explorer, click on computer at the top right and then Map Network Drive:</b> <br/>
<img src="https://i.imgur.com/c8G6Kp5.png" height="80%" width="80%" alt="VMbox"/>
<br />

<br />




 <p align="center">
<b>A pop up will appear requesting for the folder destination, this is where you need to input the socket url or url of the location of the file you want to 
 migrate,  also note the format of using a backslash instead of forward slash when inputting the destination url, follow the format of the example given</b> <br />
<img src="https://i.imgur.com/ulxA1V7.png" height="80%" width="80%" alt="VMbox"/>
<br />
<br />




 <p align="center">
<b>Once that is done, tick the reconnect at sign-in box and click finish</b> <br />
<img src="https://i.imgur.com/a82BMgL.png" height="80%" width="80%" alt="VMbox"/>
<br />
<br />



 <p align="center">
<b>If every step is followed you would see the mapped network under the network locations</b> <br />
<img src="https://i.imgur.com/ZP8qBQL.png" height="80%" width="80%" alt="VMbox"/>
<br />
<br />


<p>Now that we have the fileshare locations mapped in same network we can commence with our migration 



- Go to your sharepoint admin center and click on Migration 
- you will see Migration Manager
- Click on Fileshare getstarted which will pop up a wizard to install a migration manager agent </p>

<br />

 <p align="center">
<b>Click on Getstarted button under the fileshare label</b> <br />
<img src="https://i.imgur.com/FdjKoOc.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />



 <p align="center">
<b>Download the Migration Agent and follow the prompt</b> <br />
<img src="https://i.imgur.com/BRvEBT7.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />




 <p align="center">
<b>Add the migration task follow the prompt.</b> <br />
<img src="https://i.imgur.com/aZCVUPv.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />


<p align="center">
<b>Follow the prompt and select single migration, the fileshare you want to migrate and the destination which is the url location of your document library 
where you will be migrating the files to.</b> <br />
<img src="https://i.imgur.com/1NahVVC.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />

<p align="center">
<b>Follow the prompt the fileshare you want to migrate and the destination which is the url location of your document library 
where you will be migrating the files to.</b> <br />
<img src="https://i.imgur.com/8PTg0Zs.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />



<p align="center">
<b>Name the migration task, click on preserve permisions to keep the current permissions of the files you are migrating and then click on run.</b> <br />
<img src="https://i.imgur.com/IhJvKSJ.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />



<p align="center">
<b>When task is complete you will see the complete badge under status</b> <br />
<img src="https://i.imgur.com/T500KEv.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />


<p align="center">
<b>When task is complete you will see the complete badge under status</b> <br />
<img src="https://i.imgur.com/HOx3cPc.png" height="80%" width="80%" alt="Migration"/>
<br />
<br />

<p> I hope this project has been helpful, if you have any questions or additions to make please feel free to reach me on my email: emmanuel.chukwuemeka0416@gmail.com</p>
