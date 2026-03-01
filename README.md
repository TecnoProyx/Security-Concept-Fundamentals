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

- <b> Windows 11 (21H2): Operating System(VM)</b>
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
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
-->
