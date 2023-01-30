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

<h3>First: Open osTicket and log in using credentials from installation tutorial </h3>

- If you need help installing osTicket, please see my tutorial [here](https://github.com/jnoriega232/osticket-prereqs)

<p align="center">
<img src="https://i.imgur.com/YQMB5ER.png" height="50%" width="50%" alt="Azure Free Account"/>	


<h3>Next: Configure Roles </h3>

- Make sure you are in admin panel (top right shows the opposite of which panel you are in)
	- If the top right says "Agent Panel" you are in the admin panel
- Select the Agents tab --> Roles --> + Add New Role
	- Name : Supreme Admin
	- Select Permissions tab and check every box under the "Tickets", "Tasks" and "Knowledgebase" section
- Select Add New Role
	
<p align="center">
<img src="https://i.imgur.com/BAPmUx7.png" height="50%" width="50%" alt="Azure Free Account"/> <img src="https://i.imgur.com/0G0PHeQ.png" height="50%" width="50%" alt="Azure Free Services"/>
</p>


<h3>Next: Configure Departments</h3>

- Make sure you are in admin panel
- Select the Agents tab --> Departments --> + Add New Department 
	- Name: System Administrators
- Select Create Dept. 


<p align="center">
<img src="https://i.imgur.com/eiGG7Hv.png" height="50%" width="50%" alt="Azure Free Account"/> <img src="https://i.imgur.com/Z91ejYC.png" height="50%" width="50%" alt="Azure Free Services"/>
</p>


<h3>Next:  Configure Teams
</h3>

- Make sure you are in admin panel
- Select the Agents tab --> Teams --> Add New Team
	- Name: Level II Support 
- Go to members tab and select yourself in "Select Agent" dropdown menu
- Select create team. 
	
<p align="center">
<img src="https://i.imgur.com/v6zzN3N.png" height="50%" width="50%" alt="Azure Free Account"/> <img src="https://i.imgur.com/4IieS80.png" height="50%" width="50%" alt="Azure Free Services"/>
</p>

<h3>Next: Allow anyone to create tickets</h3>

 Make sure you are in admin panel
- Select the Settings --> User Settings
	- Make sure box is unchecked: 
		- Registration Required: Require registration and login to create tickets 
		
<p align="center">
<img src="https://i.imgur.com/kcd1jRf.png" height="50%" width="50%" alt="Azure Free Account"/>		


<h3>Next: Configure Agents</h3>

-  Make sure you are in admin panel
- Select the Agents tab -> Add New Agents
	- Name: Jane Doe
	- Email : jane.doe@osticket.com
	- Username: jane.doe
	- Click set password and uncheck box that says "send the agent a password reset email
		- Set your password to anything you like
		- uncheck box that says "require password change at next login"
		- Select set
		
<p align="center">
<img src="https://i.imgur.com/fTvI0Ru.png" height="50%" width="50%" alt="Azure Free Account"/> <img src="https://i.imgur.com/6OU5KqX.png" height="50%" width="50%" alt="Azure Free Services"/>
</p>

- Select Access tab 
	- Under Primary Department 
		- Select department dropdown menu -> System Administrators
		- Select Role dropdown menu -> Supreme Admin
	- Extended Accesss 
		- Select Department -> Support -> Add -> Supreme Admin
- Select Teams tab
	- Select team dropdown menu -> Level II Support
	- Select Add
- Select Create	

	
<p align="center">
<img src="https://i.imgur.com/HPSPHNU.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/hotx1wo.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- Create another agent and replace Jane with John.
	- Follow same steps as above except make some changes to Primary Department
		- Select department dropdown menu -> Support
		- Select Role dropdown menu -> View only
	- Extended Accesss 
		- Select Department -> Support -> Save Changes
		
<p align="center">
<img src="https://i.imgur.com/qQ8ckBr.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/KVPsUb4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>
 
     

<h3>Next: Configure Users
</h3>

- Make sure you are in Agent panel
	- If the top right says "admin" you are in the agent panel
	
<p align="center">
<img src="https://i.imgur.com/UUqCK1d.png" height="80%" width="80%" alt="Azure Free Account"/>		
	
- Select Users tab to create user
	- Email Address: Karen@osticket.com
	- Full Name - Karen Karen
	- Select Add User
	
<p align="center">
<img src="https://i.imgur.com/wpTn12W.png" height="80%" width="80%" alt="Azure Free Account"/>			
	
 - Select user tab again to create another user
	- Email Address: Ken@osticket.com
	- Full Name - Ken Ken
	- Select Add User

<p align="center">
<img src="https://i.imgur.com/EXyy5Gq.png" height="80%" width="80%" alt="Azure Free Account"/>		

<h3>Step 8:  Configure Service Level Agreements (SLA)
</h3>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select Manage tab -> SLA -> Add New SLA Plan (We are creating 3)
	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/fMR4yMR.png" height="80%" width="80%" alt="Azure Free Account"/> <img src="https://i.imgur.com/3tQnihq.png" height="80%" width="80%" alt="Azure Free Services"/>
</p>

- Name: SEV-B
- Grace Period: 4
- Schedule dropdown menu: 24/7
- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/pAbQPEP.png" height="80%" width="80%" alt="Azure Free Account"/>

- Name: SEV-C 
- Grace Period: 8
- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S Holidays
- Select Add Plan

<p align="center">
<img src="https://i.imgur.com/5cgn0oz.png" height="80%" width="80%" alt="Azure Free Account"/>



<h3>Step 9:   Configure Help Topics
</h3>

-  Make sure you are in admin panel (check top right to see which panel you are in)
- Select Manage tab -> Help Topics -> Add New Help Topic (We will be adding 4)
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- Select Add Topic for each topic

<p align="center">
<img src="https://i.imgur.com/uFmSyqK.png" height="80%" width="80%" alt="Azure Free Account"/>



🎉Congratulations! You have set up osTicket succesfully
