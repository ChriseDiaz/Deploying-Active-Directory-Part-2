<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Directory Part2 (Azure)</h1>
This tutorial outlines the implementation of Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube/ClipChamp: How to Deploy Active Directory within Azure Part2](https://youtu.be/i5HH1awlY-o?si=fE-FspCEQroCowh8)

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

-Enable Remote Desktop on Client-1:

Log into Client-1 as jane_admin.
Allow domain users access to Remote Desktop via System Properties.

-Create User Accounts in Active Directory:

Log into DC-1 as jane_admin.
Use PowerShell to create multiple user accounts in the _EMPLOYEES OU.

-Verify Account Creation:

Check the _EMPLOYEES OU in Active Directory Users and Computers (ADUC) to ensure the accounts were created correctly.

-Test Remote Desktop Access:

Log into Client-1 using one of the new non-administrative user accounts to confirm Remote Desktop access works.

<h2>Deployment and Configuration Steps</h2>

<p>
  
![Image](https://github.com/user-attachments/assets/55a81b3c-8e81-453f-b3b2-df50bad2fcbb)
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
