# Security Concept Fundamentals
<h1>RAID & File Integrity Monitoring (FIM)</h1>

 ### [YouTube Demonstration] in progress!!

<h2>Description</h2>
This project explores the basics of cybersecurity using the Confidentiality, Integrity, and Availability (CIA) triad.
To improve availability, RAID (RAID 1/10) was configured to copy data across multiple disks. This helps prevent data loss and keeps the system running if one disk fails. To protect integrity, File Integrity Monitoring (FIM) was implemented to monitor critical system files and detect unauthorized changes. 
<br />

<h2> Skills Learned</h2>

- <b> Create two unformatted Virtual Hard Disk (VHDs)</b>
- <b> Configure RAID 1 across the unallocated disks</b>
- <b> Prepare the security information and event management (SIEM)</b>
- <b> Install an agent on WIN11 and configure File Integrity Monitoring (FIM)</b>
- <b> Test File Integrity Monitoring (FIM)</b>

<h2>Languages and Utilities Used</h2>

- <b> Windows Server 2022: Domain Controller (VM)</b>?
- <b> Windows 11 pro (21H2):Domain Member (VM)</b>
- <b> Disk Management: For creating and initializing virtual hard disks (VHDs)</b>
- <b> Storage Spaces: For configuring software RAID 1 (disk mirroring)</b>
- <b> File Explorer: For verifying data and testing mirroring</b>

<h2>Steps</h2>

- <b> Task 1 – Create Two Unformatted VHDs</b>

<p align="center">
Create and format hard disk partitions: <br/>
<img src="Create and format hard disk partitions.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 
<br />
Click Action → Create VHD:  <br/>
<img src="Create VHD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Browse to C:\ and create a new folder named VHDs: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Open the VHDs folder and create the first VHD, Name as VHD1:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Size folder: 5 GB, Format: VHDX, and Click OK:  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Repeat to create the second VHD, Name: VHD2, Size: 5 GB:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Observe that both VHDs appear Unallocated in Disk Management. Leave them as they are:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- <b> Task 2 – Configure RAID 1</b>

<br />
Open Manage Storage Spaces via Start → Storage Spaces:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Click Create a new pool and storage space:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Select VHD1 and VHD2 as the disks for the pool → Click Create pool:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Setup, Name: RAID 1 VOL, Size: 8.74 GB, Select Create storage space:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Setup, Name: RAID 1 VOL, Size: 8.74 GB, Select Create storage space:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
-->
