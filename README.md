# Active Directory Network File Shares and Permissions
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>

## Objective

This Active Directory Lab project aimed to create file sharing to allow Read, Write, or Deny access yo individual users or groups. The primary focus was to create and analyze file share and permissions within a Domain Controller, generating test telemetry to mimic real-world helpdesk scenarios. I did this by running Active Directory in Azure on a virtual machine (DC1) and a client machine in Azure on a virtual machine (client1) and joined to the domain. This hands-on experience was designed to deepen understanding of network files and permissions .

### Skills Learned<h2>

- Advanced understanding in file sharing.
- Ability to generate and recognize user permissions.

### Tools and Technology Used<h2>

  - Microsoft Azure (Virtual Machines/Computers)
  - Remote Desktop
  - Active Directory Domain Services
  - Windows Server 2022
    
## Steps<h2>

* **Step 1: On DC1, on C:\drive , create 4 folders: "read-access", "write-access", "no-access", "accounting"**
  - Click the start menu and click "File Explorer"
  - Click "this PC" and right click "new" this will create folders in the "C" drive
    
![file](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/42253af8-7695-4221-af83-30873257a713)
![file2](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/a7886bd0-c044-443a-8ea4-3a1b1450271b)<p>

* **Step 2: Set the following permissions (share the folder) for the “Domain Users” group:
Folder: “read-access”, Group: “Domain Users”, Permission: “Read”
Folder: “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”
Folder: “no-access”, Group: “Domain Admins”, “Permissions: “Read/Write”**<p>
Permissions in Active Directory are access privileges that you grant to users and groups that permit them to interact with objects. An administrator assigns permissions to a user or a group so that they can access or manage a folder.
Permissions in Active Directory are divided into standard permissions and special permissions. Standard permissions give the user privileges such as read, write, and full control. Special permissions give the user different abilities such as allowing the user to modify object permissions or owners.

  - Right the folder and select "Properties"
  - Click the "Sharing" tab then click the "share" button
  - In the network access box type which user groups you want to have access to give to which folder. In the photo belows below I chose "Domain users"
  - Last you want to click the "Permission Level" tab and choose which permissions you want to give to the folder. In the photo below I chose "Read" which means users outside of the Domain Users group will be able to "read only" the files in the folder.
 
![file3](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/3c1839e5-d5fb-4353-a44b-45f9cd3470d3)
![file4](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/2c16c0ce-0a04-4959-ac80-9e1926dbee12)
![file5](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/52f34a64-9130-4134-a71a-c469bd778002)<p>

* **Step 3: Attempt to access file shares as a normal user an test access**
  - On Client-1, navigate to the shared folder (start, run, \\dc-1)
  - Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in?


![file6](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/b71145c7-9098-450b-85ae-e9718fbeb6b3)
![file7](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/a4262f00-77fa-4405-bba6-52a6b7fffa43)
![file8](https://github.com/TerrellSowell/Active-Directory-File-Share-Permissions/assets/161978506/6bb6dfeb-5fc6-4cbc-9a20-137f04901f74)


