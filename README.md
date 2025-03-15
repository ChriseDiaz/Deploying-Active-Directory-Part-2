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
Summary of Steps for Setting Up Remote Desktop for Non-Administrative Users on Client-1

1.Log into Client-1 as mydomain.com\jane_admin:

Log into the Client-1 machine using an administrative account.

2.Enable Remote Desktop for Domain Users:

Open System Properties on Client-1.
Go to the Remote Desktop section and allow access for domain users (e.g., domain users group).

3.Create Additional Users:

Log into DC-1 (Domain Controller) as jane_admin.
Open PowerShell_ise as Administrator.
Create a script to generate multiple user accounts.
Run the script and monitor the creation of accounts.

4.Verify Account Creation in Active Directory Users and Computers (ADUC):

After running the script, open Active Directory Users and Computers (ADUC).
Check that the new accounts are in the appropriate organizational unit (_EMPLOYEES).

5.Test Remote Desktop Access:

Log into Client-1 with one of the newly created non-administrative user accounts (refer to the password specified in the script).
Ensure that the user is able to log in successfully via Remote Desktop.

The remote desktop access should now be available for non-administrative users, and you can verify the creation of accounts and their ability to log in on Client-1.
</p>
<br />
