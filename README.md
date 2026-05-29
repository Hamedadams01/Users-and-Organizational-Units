# Users and Organizational Units in Active Directory

Overview:

In this home lab, I will demonstrate how to create and manage users and Organizational Units (OUs) within Active Directory. This lab builds on a configured Windows Server 2022 environment with Active Directory Domain Services (AD DS) and DNS already installed.

This simulation reflects real-world IT administrative tasks such as user provisioning, organizational structuring, and access control using groups and shared resources.

## **Objectives**

- Create and manage domain user accounts
- Design and implement an Organizational Unit (OU) structure
- Assign users to appropriate departments
- Create security groups and manage permissions
- Configure shared folders and apply access control

AD DS and DNS are running. Now I’m moving into Active Directory to start building out users and organization.

![image alt]()

I opened Active Directory Users and Computers, and I can see my domain `houtech.locl` with all the default folders. From here, I’m getting ready to create my first user.”

![image alt]()
I right-clicked the **Users** container and selected **New > User** to open the New Object - User form. The

![image alt]()
I created a user named Emily Carter with the logon name Ecarter@houtech.locl. Below that you can see she’s now showing up in the Users container alongside the built-in accounts.

![image alt]()
![image alt]()
I repeated the same process and created the full set of domain users: 

![image alt]()
Now that I had users, I needed to organize them. I right-clicked the domain root **HOUTECH.LOCL** and selected **New > Organizational Unit**, naming it **Departments**. 

![image alt]()
Inside the **Departments** OU, I created five child OUs: **HR**, **IT**, **Finance**, **Marketing**, and **Sales**. I did this by right-clicking Departments and selecting New > Organizational Unit for each one.

![image alt]()
![image alt]()
With the OU structure built, I moved users into their correct department OUs. 

![image alt]()
![image alt]()
Now let’s group users the whole point of groups and permissions is to make sure the right people get access to the right resources, and nobody

![image alt]()
I’m adding members to the SalesShare group. I searched for Brandon Hill and added him. Below that I’m assigning him permissions to the share.

![image alt]()
I created different shared folders like ITShare, MarketingShare, FinanceShare, HRShare, and SalesShare, and linked them to the server paths.
This is how teams share files 

![image alt]()
![image alt]()
This allowed me to centralize files in one location and control access using group-based permissions instead of assigning permissions to individual users, making management easier and more secure.

![image alt]()
![image alt]()
![image alt]()
Confirming the ITshare settings before creating it. Below that shows all 7 shares are now live — ITShare, MarketingShare, FinanceShare, HRshare, and SalesShare all created and mapped to their correct paths on HOUTECH01.
