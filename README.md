<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Directory Part2 (Azure)</h1>
This tutorial outlines the implementation of Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube/ClipChamp: How to Deploy Active Directory within Azure Part2](https://youtu.be/Pl8JxPP6c4g?si=rV24UuJx_eK--dnY)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Active Directory Users and Computers
- Powershell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Active Directory Domain Services were installed and configured on DC-1, promoting it to a Domain Controller with the domain mydomain.com.

- Two Organizational Units (OUs) were created: _EMPLOYEES and _ADMINS. A Domain Admin user (jane_admin) was set up and added to the Domain Admins group.

- Client-1 was successfully joined to the domain, and its organizational structure was updated by placing it into the _CLIENTS OU in ADUC.

<h2>Deployment and Configuration Steps</h2>

<p>
  
![Image](https://github.com/user-attachments/assets/fd581858-db9a-40ec-ab7c-e288d1315944)

</p>
<p>
Part 1: Install Active Directory

1.Login to DC-1: Log in to the server designated as DC-1.

2.Install Active Directory Domain Services: Use the Server Manager to add the Active Directory Domain Services (AD DS) role to the server.

3.Promote DC-1 to Domain Controller:

During the AD DS installation, you'll be prompted to promote the server to a domain controller.
Choose the option to set up a new forest and enter your domain name (e.g., mydomain.com).

4.Restart the Server: After the promotion is complete, restart the server to apply changes.

5.Login as User: After the server restarts, log back into DC-1 as the user mydomain.com\labuser.
</p>
<br />

<p>

5.Organize Client-1 in ADUC:

Create a new OU called _CLIENTS in ADUC.
Drag Client-1 into the _CLIENTS OU.
</p>
<br />
