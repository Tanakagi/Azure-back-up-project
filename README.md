# Azure-back-up-project
<h2>Description<h2>
In this project, I used Azure Backup to back up my files contained in my Azure Fileshare.

<h2>Environments Used </h2>

- <b>Azure Portal</b> 


<h2>Project walk-through:</h2>

<p align="center">
I first went to the marketplace and searched for backup and site recovery: <br/>
<img src="https://i.imgur.com/7YQtNve.png" height="80%" width="80%" />
<br />
<br />
and started the creation of my Recovery Services vault named rsavault and made sure it was in the same region as the storage account and fileshare that I would use for this project:  <br/>
<img src="https://i.imgur.com/JUdaJHj.png" height="80%" width="80%" />
<br />
<br />
 Once rsavault was created I went to it and started configuring the backup. I then selected locally redundant replication method for the backup since the data on the file share could be easily reconstructed and my goal was to minimize costs:  <br/>
 <img src="https://i.imgur.com/yUCCFga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
I then selected “Azure file share” on the dropdown and clicked backup:  <br/>
<img src="https://i.imgur.com/2oQdijj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br /> 
Using the portal I then started configuring the backup for my fileshare. I selected the storage account (storesyncrsa) for the backup and added fileshare1rsa:  <br/>
<img src="https://i.imgur.com/UBOHe3E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
I then configured a new policy for the backup named DailyBackupP and set the time of the daily backups to 19:00 PM UTC (coordinated universal time):  <br/>
<img src="https://i.imgur.com/Bj5SWfC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<br />
After selecting enable backup I then went to the resource to confirm the completion of the backup, which was the end of this project. I had succedfully achieved my goal of backing up my files within fileshare1rsa to Azure:  <br/>
<img src="https://i.imgur.com/ZSEQuY5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/qxWgJuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
