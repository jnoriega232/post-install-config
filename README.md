<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
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

- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create tickets
- Configure Agents
- Configure SLAs
- Configure Help Topics

<h2>Post-Install Configuration Steps</h2>

<h3>Step 1: Open osTicket and log in using credentials from installation tutorial</h3>

- If you need help installing osTicket, please see my tutorial [here](https://github.com/jnoriega232/osticket-prereqs)

<p align="center">
<img src="https://i.imgur.com/YQMB5ER.png" height="70%" width="70%" alt="Azure Free Account"/>	


<h3>Step 2: Configure Roles</h3>

- Make sure you are in the admin panel (top right shows the opposite of which panel you are in)
	- If the top right says "Agent Panel" you are in the admin panel
- Select the Agents tab > Roles > + Add New Role
	- Name : Supreme Admin
	- Select Permissions tab and check every box under the "Tickets", "Tasks" and "Knowledgebase" section
- Select Add New Role
	
<p align="center">
<img src="https://i.imgur.com/BAPmUx7.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/0G0PHeQ.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 3: Configure Departments</h3>

- Make sure you are in the admin panel
- Select the Agents tab > Departments > + Add New Department 
	- Name: System Administrators
- Select Create Dept. 


<p align="center">
<img src="https://i.imgur.com/eiGG7Hv.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/Z91ejYC.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 4: Configure Teams</h3>

- Make sure you are in the admin panel
- Select the Agents tab > Teams > + Add New Team
	- Name: Level II Support 
- Go to members tab and select yourself in "Select Agent" dropdown menu
- Select Create Team. 
	
<p align="center">
<img src="https://i.imgur.com/QPcsh6r.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/B99CkdV.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

<h3>Step 5: Allow anyone to create tickets</h3>

 Make sure you are in the admin panel
- Select the Settings > User Settings
	- Make sure box is unchecked: 
		- Registration Required: Require registration and login to create tickets 
		
<p align="center">
<img src="https://i.imgur.com/6a2rVoz.png" height="70%" width="70%" alt="Azure Free Account"/>		


<h3>Step 6: Configure Agents</h3>

-  Make sure you are in the admin panel
- Select the Agents tab > + Add New Agents
	- Name: Jane Doe
	- Email : jane.doe@osticket.com
	- Username: jane.doe
	- Click set password and uncheck box that says "send the agent a password reset email"
		- Set your password to anything you like
		- uncheck box that says "require password change at next login"
		- Select Set
		
<p align="center">
<img src="https://i.imgur.com/yeN2bdB.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/pExgPGk.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Select Access tab 
	- Under Primary Department 
		- Select department dropdown menu > System Administrators
		- Select Role dropdown menu > Supreme Admin
	- Extended Accesss 
		- Select Department > Support > Add > Supreme Admin
- Select Teams tab
	- Select team dropdown menu > Level II Support
	- Select Add
- Select Create	

	
<p align="center">
<img src="https://i.imgur.com/CBOfbj2.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/Iq9jEuB.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Create another agent named John Doe
	- Follow same steps as above except make some changes to Primary Department
		- Select department dropdown menu > Support
		- Select Role dropdown menu > View only
	- Extended Accesss 
		- Select Department > Support > Create
		
<p align="center">
<img src="https://i.imgur.com/Uy8fVdP.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/8owyJHJ.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>
 
     

<h3>Step 7: Configure Users</h3>

- Make sure you are in the agent panel
	- If the top right says "Admin Panel" you are in the agent panel
	
<p align="center">
<img src="https://i.imgur.com/LoyD72f.png" height="70%" width="70%" alt="Azure Free Account"/>		
	
- Select Users tab to create user
	- Email Address: Karen@osticket.com
	- Full Name - Karen Karen
	- Select Add User
	
<p align="center">
<img src="https://i.imgur.com/beupoPC.png" height="70%" width="70%" alt="Azure Free Account"/>			
	
 - Select user tab again to create another user
	- Email Address: Ken@osticket.com
	- Full Name - Ken Ken
	- Select Add User

<p align="center">
<img src="https://i.imgur.com/J7hvpl0.png" height="70%" width="70%" alt="Azure Free Account"/>		

<h3>Step 8: Configure Service Level Agreements (SLA)</h3>

- Make sure you are in the admin panel
- Select Manage tab > SLA > + Add New SLA Plan (We are creating 3)
	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/NbVc9AZ.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/ZEnf18l.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Name: SEV-B
- Grace Period: 4
- Schedule dropdown menu: 24/7
- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/9tQOgO6.png" height="70%" width="70%" alt="Azure Free Account"/>

- Name: SEV-C 
- Grace Period: 8
- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S Holidays
- Select Add Plan

<p align="center">
<img src="https://i.imgur.com/Fi5kgip.png" height="70%" width="70%" alt="Azure Free Account"/>



<h3>Finally: Configure Help Topics</h3>

-  Make sure you are in the admin panel
- Select Manage tab > Help Topics > Add New Help Topic (We will be adding 4)
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- Select Add Topic for each topic

<p align="center">
<img src="https://i.imgur.com/yG1AluY.png" height="70%" width="70%" alt="Azure Free Account"/>



🎉 **Congratulations! You have set up osTicket successfully** 🎉 Click [here](https://github.com/jnoriega232/ticket-lifecycle) to move on to the final part of this tutorial!
