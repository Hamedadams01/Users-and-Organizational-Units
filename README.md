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

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-11_131152.webp)

I opened Active Directory Users and Computers, and I can see my domain `houtech.locl` with all the default folders. From here, I’m getting ready to create my first user.”

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-11_131225.webp)

I right-clicked the **Users** container and selected **New > User** to open the New Object - User form. The

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-11_131640.webp)

I created a user named Emily Carter with the logon name Ecarter@houtech.locl. Below that you can see she’s now showing up in the Users container alongside the built-in accounts.

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-12_105058.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-12_105207.webp)

I repeated the same process and created the full set of domain users: 

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-12_113102.webp)

Now that I had users, I needed to organize them. I right-clicked the domain root **HOUTECH.LOCL** and selected **New > Organizational Unit**, naming it **Departments**. 

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-13_162547.webp)

Inside the **Departments** OU, I created five child OUs: **HR**, **IT**, **Finance**, **Marketing**, and **Sales**. I did this by right-clicking Departments and selecting New > Organizational Unit for each one.

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-13_162443.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-13_163701%20(1).webp)

With the OU structure built, I moved users into their correct department OUs. 

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-13_163301.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/9a019e6f475cb33ae1d0de26ec8c7c0bf17f8822/Screenshot_2026-03-13_163351.webp)

Now let’s group users the whole point of groups and permissions is to make sure the right people get access to the right resources, and nobody

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-13_164234.webp)

I’m adding members to the SalesShare group. I searched for Brandon Hill and added him. Below that I’m assigning him permissions to the share.

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-13_164357.webp)

I created different shared folders like ITShare, MarketingShare, FinanceShare, HRShare, and SalesShare, and linked them to the server paths.
This is how teams share files 

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_095917.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_100317.webp)

This allowed me to centralize files in one location and control access using group-based permissions instead of assigning permissions to individual users, making management easier and more secure.

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_100425.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_100600.webp)
![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_100632.webp)

Confirming the ITshare settings before creating it. Below that shows all 7 shares are now live — ITShare, MarketingShare, FinanceShare, HRshare, and SalesShare all created and mapped to their correct paths on HOUTECH01.

![image alt](https://github.com/Hamedadams01/Users-and-Organizational-Units/blob/c50816b4f2a9d22c9940c1966f9d3241af20e4c3/Screenshot_2026-03-14_103221.webp)
