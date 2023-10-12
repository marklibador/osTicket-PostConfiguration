<p align="center">

![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/14ba8812-83a0-407e-8086-fdb957078492)



</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles and Departments
-  Configure Teams and allow anyone to create tickets
- Now we will configure agents/workers and user/customers
- Configure SLA
- Configure Help Topics

<h2>Prerequisites and Installation</h2>

- _This Tutorial assumes that you went through the <a href="https://github.com/marklibador/osticket-prereqs">"Prerequisites and Installation"</a> tutorial to be inside osTicket._

---
<h1>Configuration Steps</h1>


**osTicket Admin Panel Configuration Guide**

**Welcome to osTicket! Let's start setting up your admin panel for efficient support ticket management.**

> **Note***
>**Admin vs Agent:** *Admin Panel is used by the Administrator of the osTicketing System whereas Agent is used by the Workers (Helpdesk Professionals).*

<h3>&#9312;Creating Roles</h3>

>**Note***
>*Roles are the permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments.*
- Enter Admin Role through the `Admin Panel`

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/bc663ade-d739-42e0-a1ed-fd84f27e53f4)



- Head to `Agents` 

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/f3763f48-d7e5-4f19-8068-4de208b2859c)



- Add a new role called **Supreme Admin**
  
> **Note***
>This role should have all permissions over the Ticketing System!

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/616c62d3-f8fa-40f9-8cfc-4150f930e6ad)



---

<h3>&#9313Creating Departments</h3>

>**Note***
>*Departments are collections of Agents in a department.* 

- Click the `Admin Panel` on the top-right of the page.
- Click `Agents`
- Click `Departments`
- Click `Add a New Department`

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/95b0f69e-af7e-479f-b725-69259266c3c5)


- Create a Department called **System Administrators**
- Click `Create Dept`

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/6ae41c46-d8cf-487a-bc4b-3fd244178bdd)


<h3>&#9314Creating Teams</h3>

>**Note***
>*Having Agents from different Departments assigned to a Team will supersede the parameters of the Agents’ Department rules. For example, you can create a Help Topic associated with a particular product you produce, and assign it to a Team of specialist Agents from different Departments.*
- Inside the `Admin Panel`
- Click on `Agents`
- Click on `Teams`
- Click on `Add New Teams`

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/538cf87d-1dff-483b-bf92-7cfd054b8b23)


- Create a Team called **Level II Support**
- Click on `Create Team`

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/b62beb8e-f87c-4d7d-94e7-4a2f2499350f)


<h3>&#9314Creating Agents</h3>

>**Note***
>*Agents are given access to the help desk with the intent to respond and resolve the tickets.*

- Inside the `Admin Panel`
- Click on `Agents`
- CLick on `Agent`
- Click on `Add a New Agent`

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/4f1f2bad-07d6-427b-8774-f3a16c700fa1)


- Using the Required Credenitals **(In Bold)**
     - `First Name:` **Jane**
     - `Last Name:` **Doe**
     - `Email Address:` **jane.doe@osTicket.com**
     - `Username:` **jane.doe**
     - Click on `Set Password` 

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/4f15f7e0-b4db-4d4e-90fb-8b8fa0417206)


 - Uncheck "Send the agent a password reset email"
 - Create a Password
 - Uncheck "Require password change at next login"
 - CLick `Set`

 ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/b89e5b68-6541-4c24-bc8c-987fbfb1906b)


- CLick the `Access` tab:
   - Assign Jane's `Primary Department` to **System Administrators**
   - Assign Jane's `Role` to **Supreme Admin**
- Underneath `Extended Access`tab:
    - Assign Jane to `Support Department`
    - Assign Jane's `Role` to **Supreme Admin**
    - Click `Save Changes`

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/1fa94ad4-2448-4d37-9784-9af05227829c)


- Click the `Teams` tab:
  - Assign Jane to **Level II Support**
-  Click on `Create`

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/d1acc2f4-a6d8-4b0a-a7d2-c3b155eec0eb)

- Create another Agent following the same steps, using the name **John Doe**

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/0157ad60-414f-4470-8a6c-07ac9408104e)

- Make John's `Department`: **Level I Support**
- Assign John's `Role`: View Only
- Underneath `Extended Access`: Support
- Click on `Create`

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/62c95383-8b87-4c48-b3e4-f9537090af11)

<h3>&#9315Creating Users</h3>

>**Note***
>*Users are the individuals who submit tickets to your support team.*

- Click on the `Agent Panel`
- Navigate to `Users`
- Click `Add User` 

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/67bc9568-7e05-4f80-8407-e594bc9f5dd2)


- Make the User's `Email Address`: **karen@osticket.com**
- `Username`: **Karen Karen**
- Click `Add User`

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/e32cd67b-b900-4983-9cf2-1d1ebaa927ba)

- Create another user, following the same steps but `Email address`: **ken@osticket.com**
- `Username`: **Ken Ken**
- Click `Add User`

![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/9ef34fbd-e2d2-4f64-97e0-82646cc0b5b2)

<h3>&#9316Creating SLA</h3>

>**Note***
>*The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.*


- Click on the `Admin Panel`
- Navigate to `Manage` tab
- Click `SLA`
- Click `Add New SLA Plan`

![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/c4165a75-30b3-408a-bba3-75255902695b)


- Create the following plans:
  - **SEV-A**
    - Grace Period: **1 hour** *(Amount, in hours, before tickets with tis SLA will become overdue if not closed in allotted time.)*
    - Schedule: **24/7**
  - **SEV-B**
     - Grace Period: **4 hours**
     - Schedule: **24/7**
  - **SEV-C**
      - Grace Period: **8 hours**
      - Schedule: **Monday - Friday: 8 a.m - 5 p.m (with U.S Holidays)**
- Click `Add Plan` for each

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/0a54a84a-8342-4ec7-9522-ffdb2790a35a)


  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/e9eca7cf-a46f-4f41-b6d6-ce59c2355876)

<h3>&#9317Creating Help Topics</h3>

>**Note***
>*Help Topics will determine what Department the ticket is routed to which will determine which Agents have access to the ticket. The Help Topic also can determine other configurations of the ticket, such as the ticket’s SLA (or Service Level Agreement) and priority of a ticket, i.e. Emergency to Low.*

- Click on the `Admin Panel`
- Navigate to the `Manage` tab
- Click on `Help Topic`
- Click `Add New Help Topic`

  ![image](https://github.com/marklibador/osTicket-PostConfiguration/assets/37192566/7877b8e3-0f5a-4e80-8c50-3011eea27c3e)


- Create Help Topics with the following names:
    - **Business Critical Outage**
    - **Personal Computer Issues**
    - **Equipment Request**
    - **Password Reset**
- `Internal Notes` can be used, but not necessary
- Click `Add Topic`

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/f162a73d-063f-440e-94de-27c026b6a7eb)

  ![image](https://github.com/CarlosAlvarado0718/osTicket-PostConfig/assets/140138198/ec00fd9d-f9dc-4aec-a2ae-a03427a1535b)

---

  <h1>ALL DONE!! CONGRATS!! </h1>

  <h3>NEXT TUTORIAL:  <a href="https://github.com/marklibador/osTicket-Ticket-Lifecycle-Examples/blob/main/README.md">"Ticket Lifecycle Examples"</a>  </h3>
