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
<img src="Create and format hard disk partitions.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
 
<br />
Click Action → Create VHD:  <br/>
<img src="Create VHD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Browse to C:\ and create a new folder named VHDs: <br/>
<img src="rename the newly created folder as follows, VHDs.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Open the VHDs folder and create the first VHD, Name as VHD1:  <br/>
<img src="double-click on the VHDs folder and file name saction VHD1 and press save.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Size folder: 5 GB, Format: VHD or VHDX, and Click OK:  <br/>
<img src="select OK.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Repeat to create the second VHD, Name: VHD2, Size: 5 GB:  <br/>
<img src="select GB from the dropdown menu and type the following (2).png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Observe that both VHDs appear Unallocated in Disk Management. Leave them as they are:  <br/>
<img src="Observe that both VHDs appear Unallocated in Disk Management. Leave them as they are.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

- <b> Task 2 – Configure RAID 1</b>

<br />
Open Manage Storage Spaces via Start → Storage Spaces:  <br/>
<img src="Open Manage Storage.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Click Create a new pool and storage space:  <br/>
<img src="click Create a new pool.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Select Disk 2 and Disk 3 for the pool → Click Create pool:  <br/>
<img src="Select drives to create a storage pool.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Setup, Name: RAID 1 VOL:  <br/>
<img src="SET Name, RAID 1 VOL.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br /> Size: 8.74 GB, Select Create storage space:  <br/>
<img src="size maximun field 8.74gb.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
Verify that RAID 1 VOL is listed as OK in Storage Spaces:  <br/>
<img src="Verify that RAID 1 VOL is listed as OK in Storage Spaces.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<br />
(Optional) Copy files from another drive to RAID 1 VOL to test mirroring:  <br/>
<img src="Copy files from another drive to RAID 1 VOL to test mirroring.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
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
