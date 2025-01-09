<hr>
Project Title: *Secure Remote Access Setup and Configuration for Virtual Machines*<br>
Duration: 3 weeks<br>
*Objective:*<br>
The objective of this project is to enable you to understand, configure, and secure remote access to virtual machines (VMs) running Windows operating systems.<br>
This group will be responsible for setting up a VM, ensuring it is securely accessible from a physical computer, and documenting the process and security measures.<br>
<hr>
TASK 1.<br>
Virtual Machine Setup:<br>
- Create a Windows-based virtual machine using your Azure portal.<br>
- Configure the network settings of the VM to ensure it is accessible from the network.<br>
<br>
In azure portal's search bar<BR>
Search for virtual machines, click on "Virtual machines" under Services<BR>
On the next page, Click on create and select Azure virtual machine, Leading to virtual machine configuration page(Basic Tab).<br>
<br>
<br>The Basic Tab(VM configuration)<br>
<br>
Project Details.<br>
Select Subscription then Resource group(create a new Resource group if required).<br>
<br>
Instance Details.<br>
Vm Name: mymm<br>
Region: East US<br>
Availability Option: No Infrastructure Redundancy Required.<br>
Security Type: Standard<br>
Image: Windows Server 2022 Datacenter<br>
<img width="961" alt="BASIC TAB IMAGE" src="https://github.com/user-attachments/assets/e87e71a6-6dce-439b-8885-ec3a16a60bba" /><BR>
Vm Architecture: X64.<br>
Size: Standard_D2S_V3 - 2Vcpus,8 GiB memory.<br>
<img width="961" alt="ARC ADMIN" src="https://github.com/user-attachments/assets/61ca4416-e84f-46ca-9de4-2fdce6030aec" /><br>
Administrator Account.<br>
Username: myVm.<br>
Password: enter password.<br> 
Confirm password: enter password.<br>
<br>
<br>
Inbound port rules<br>
Public inbound ports: Allow selected ports.<br> 
Select inbound ports: RDP(3389).<br>
<img width="961" alt="INBOUND RDP" src="https://github.com/user-attachments/assets/e1c6275d-867b-4be5-9f02-7b6fd020a489" /><br>  
<br>
Disks Tab(VM configuration).<br>
OS disk size: Image default(127GiB).<br>  
OS disk type: Premium SSD.<br> 
Delete with VM: check.<br> 
Key management: Platform-managed key.<br>
<img width="961" alt="Diskstab" src="https://github.com/user-attachments/assets/8cf63dde-ab0d-4e51-9872-e60bd292e1b2" /><br>
<br>
<br>
Networking Tab.(VM configuration)<br>
<br>
Virtual Network: MyVm-vnet<br>
Subnet: Default(10.0.0.0/24).<br> 
Public IP: myvm-ip.<br> 
NIC network security group: Basic.<br>
Public inbound ports: Allow selected ports.<br> 
Select inbound ports: RDP(3389).<br>
Load balancing options: None.<br>
<img width="961" alt="NETWORKING TAB" src="https://github.com/user-attachments/assets/75c1b253-abbd-4fd9-99c8-702421930db0" /><br>
Then, click "Review + create"<br> 
<br>
Validation passed... Initializing deployment...<br>
<img width="961" alt="Valid Passed" src="https://github.com/user-attachments/assets/48268c3b-0aba-49c4-a53f-a8697ca9c8c7" /><br>
<br>
Deployment succeeded, click on "Go to resouce"<br>
<img width="961" alt="Deployment Succeeded" src="https://github.com/user-attachments/assets/2f2d7d58-0003-47f9-8ebf-324cfd215462" /><br>
<br>
<br>Download,locate the RDP file and double click on it to loggon...<br>
<img width="961" alt="Download RDP" src="https://github.com/user-attachments/assets/212f9023-219f-4903-8321-b5b2be53a857" /><br>
<br>
<br>

<img width="961" alt="MyVm" src="https://github.com/user-attachments/assets/66d3884e-d8c3-48e2-bddb-4a268cc1f27c" /><br>
Logging RDP<b>
<hr>
Task 2.<br>
User Account Management<br>
- Create user accounts on the Windows VM for each group member.<br>
- Assign appropriate permissions based on the principle of least privilege.<br>
<br>
On the running virtual machine...<br>
<br>
Using the Windows search bar, type in "Computer Management" then enter to open the computer managerment tool.<br>
On the left-hand-side, Click on "System Tools drop-down",<br>
Click on "Local Users and Groups drop-down",<br>
Right-click "Users" then select "New User" to add users.<br>
<img width="961" alt="Com mngmnt" src="https://github.com/user-attachments/assets/a1050ba4-8afb-4725-ba57-36af4c5644d5" /><br>
<br>
<br>
Fill the information of a group member, then click "Create" to add a user.
<img width="570" alt="ADD USERS" src="https://github.com/user-attachments/assets/bebe910a-0c13-4eaa-b4e6-141b440743b1"/><br>
<br>
<img width="353" alt="Success" src="https://github.com/user-attachments/assets/5cd4c2d4-728d-4fba-b180-6d63f5f803fd"/><br>
Admin Success belongs to admin group and is requested to change password on next log-on.<br>
<br>
<img width="353" alt="Gab" src="https://github.com/user-attachments/assets/b7b0806b-9930-4e0c-94e7-a0c5630b803d"/><br>
Angel Gabriel belongs to the admin group and is requested to change password on next log-on.<br>
<br>
<img width="395" alt="Okonola Babatunde" src="https://github.com/user-attachments/assets/df079643-9581-4205-baa7-a7e8b2b27b07" /><br>
Babatunde belongs to the users group and cannot change passwords.<br>
<br>
<img width="353" alt="Danita Okoye" src="https://github.com/user-attachments/assets/7c5818ad-5f58-4956-a8e0-257f809fb0bc" /><br>
Danita Okoye belongs to the users group and do not have access to passwords.<br>
<br>
<img width="353" alt="Oghenesuvwe Omashone" src="https://github.com/user-attachments/assets/f9aca71d-202a-4d60-9d6b-a5093b9a74aa" /><br>
Oghenesuvwe Omashone belongs to the users group and cannot change passwords<br>
<br>
<img width="353" alt="Iyke" src="https://github.com/user-attachments/assets/2e28814a-7523-4c2a-b4cd-c5563b53680b"/><br>
Iyke Kc belongs to the users group and do not have access to passwords.<br>
<br>
<img width="353" alt="Ola" src="https://github.com/user-attachments/assets/897d6cac-7fb0-4b74-8158-c926fc230198"/><br>
Ola is not in admin group and cannot change passwords.<br>
<br>
<img width="393" alt="Mr Victor" src="https://github.com/user-attachments/assets/1cff599d-b0aa-4a0b-8757-70f1db61f82c" /><br>
Mr Victor belongs to the users group and cannot change passwords.<br>
<hr>
Task 3.<br>
Enable Remote Desktop Protocol(RDP)<br>
- Enable RDP on the Windows VM.<br>
- Configure the firewall to allow RDP connections (default port TCP/3389).<br>
<br>
<br>
- Enable RDP on the Windows virtual machine.<br>
<br>
On the running virtual machine.<br>
<br>
Using the "Win + R" open the "Run" dialog box.<br>
<br>
type "sysdm.cpl" then enter. to open System Properties tool.<br>
click on the "Remote" tab at the top-right...<br>
<br>

<br>
<img width="407" alt="Remote" src="https://github.com/user-attachments/assets/66c87655-fced-4fd7-8669-04745f469e0e" /><br>
Under "Remote Desktop" > "Allow remote connections to this computer"<br>
then OK...<br>
<br>

<br>
- Configure the firewall to allow RDP connections (default port TCP/3389).<br>
<br>
On the running virtual machine<br>
<br>
Using the Windows search bar, search for "Windows Defender Firewall" and enter to open the firewall tool.<br>
<img width="1044" alt="Windows defender firewall" src="https://github.com/user-attachments/assets/64f34575-b8a1-47ad-a8e6-3216cae8a48b" /><br>
On the left-hand pane, click on "Inbound Rules"<br>
then, on the right-hand pane, click on "New Rule"<br>
<img width="1036" alt="New Rule" src="https://github.com/user-attachments/assets/c573fe50-5fd3-4b82-b9f4-ef8a2bc4a3a6" /><br>
<br>
"Rule Type" select "Port"<br>
<img width="708" alt="PORT" src="https://github.com/user-attachments/assets/3cdc25c7-2d4a-4abe-86e4-14351d07d531" /><br>
then down below, select "Next".<br>
<br>
Does this rule apply to, select "TCP"<br>
Specific local Port enter "3389"<br>
<img width="713" alt="Specific local port" src="https://github.com/user-attachments/assets/6b7db285-41bd-4850-b829-8d934d2b2530" /><br>
then select "Next" down below.<br>
<br>
"Action" select "Allow the connection."<br>
then select "Next" below<br>
<br>
"Profile" check for "Private and Public"<br>
then select "Next" below<br>
<br>
Name "Allow"<br>
then, click "Finish" down below.<br>
<hr>
Task4.<br>
Secure the Connection:<br>
- Set a Network Security Group (NSG) to restrict access to the VM to specific IP addresses.<br>
<br>
<br>
Create inbound security rule.
<br>
<br>
In the azure portal, search for NSG in the azure search bar.<br>
in the NSG overview page, Click "Inbound security rules" under "Settings" on the left-hand.<br>
Then, Create a new rule.<br>
<br>
Source:  "IP Addresses".<Br>
Source IP Addresses/Cidr Ranges: "Enter virtual machine's IP Address".<Br>
Destination: "Any".<Br>
Service: "Rdp"<Br>
Action: "Allow"<Br> 
Priority: "100"<Br> 
Name: "AllowRDPFromSpecificIP"<br>
Save the rule.<br>
<img width="579" alt="Inbound Rules" src="https://github.com/user-attachments/assets/eb016845-6a4d-45f2-8f4a-79e91b3acc36" /><br>
<br>

<br>
Create Outbound Security Rules:  
<br>

<br>
In the azure portal, search for NSG in the azure search bar.<br>
in the NSG overview page, Click "Outbound security rules" under "Settings" on the left-hand.<br>
Then, Create a new rule.<br>
<img width="579" alt="AllowAnyDNS Outbound" src="https://github.com/user-attachments/assets/7a3aaf0a-2134-4dbb-a8c4-55d910245830" /><br>
Source:  "Any"<br>
Destination:  "IP Addresses"<br>
Destination IP Addresses/CIDR Ranges: "Enter virtual machine's IP Address"<br>  
Service "TCP"<br>
Action:  "Allow"<br> 
Priority: "200"<br>
Name: "AllowOutboundToSpecificIP"<br>
Save the rule<br>
<hr>
TASK 5.<br>
Test Remote Access:<br>
- Each group member should test remote access to the Windows virtual machine using RDP.<br>
- Troubleshoot and resolve any connection issues.<br>
<hr>
TASK 6.<br> 
*Monitoring and Logging:*<br>
- Enable and configure logging in the Windows Event Viewer to track remote access attempts.<br>
- Monitor the logs for any unauthorized access attempts and document the findings.<br>
<br>
<br>
On the running virtual machine<br>
<br>
Using "Win + R", open the "Run" dialog box.<br>
<br>
Type "eventvwr.msc" into the "Run" dialog box to open the "Event Viewer" tool.<br>
<br>
Right in the "Event Viewer",<br>
On the left-hand pane, click on "Windows Logs" drop-down, then click Security<br>
<img width="1014" alt="EventVwr" src="https://github.com/user-attachments/assets/c0f55593-dbc7-42d1-86f1-37cc2668c10d" />
<br>
Then, on the right-hand pane, click on "Filter Current Log.<br>
<br>
For logon events<br>
4624 for successful log-ons<br>
<img width="439" alt="Success Logon" src="https://github.com/user-attachments/assets/7329ee08-5d4f-4665-90a0-02130687d1f9" />
<br>
4625 for failed log-ons<br>
<img width="444" alt="Failed Loggon" src="https://github.com/user-attachments/assets/d0ebf79b-49cf-40d8-b20b-45ddbd71fe5e" />
<br>
4648 Logon attempt using explicit credentials.<br>
<img width="442" alt="Explicit Loggon" src="https://github.com/user-attachments/assets/fc59e6a3-640a-4b4e-b127-50e29d72a892" /><br>
<br>

<br>

<br>
- Monitor the logs for any unauthorized access attempts and document the findings.<br>
<br>
<br>
Below is filtered log for event ID "4625". a Failed Log-on from Event Log<br>
<br>
<img width="620" alt="Event 4625" src="https://github.com/user-attachments/assets/347b6e19-81a1-4674-878b-96aa79a64f0d" /><br>

<br>
<br>
With the log information below<br>
<br>
Log Name:      Security<br>
Source:        Microsoft-Windows-Security-Auditing<br>
Date:          12/18/2024 12:55:28 PM<br>
Event ID:      4625<br>
Task Category: Logon<br>
Level:         Information<br>
Keywords:      Audit Failure<br>
User:          N/A<br>
Computer:      Machine<br>
Description:<br>
An account failed to log on.<br>
<br>
Subject:<br>
Security ID:		SYSTEM<br>
Account Name:		MACHINE$<br>
Account Domain:		WORKGROUP<br>
Logon ID:		0x3E7<br>
<br>
Logon Type:			2<br>


<br>
<br>
Account For Which Logon Failed:<br>
Security ID:		NULL SID<br>
Account Name:		machine<br>
Account Domain:		<br>
<br>
Failure Information:<br>
Failure Reason:		Unknown user name or bad password.<br>
Status:			0xC000006D<br>
Sub Status:		0xC0000064<br>
<br>
Process Information:<br>
Caller Process ID:	0x1c8<br>
Caller Process Name:	C:\Windows\System32\svchost.exe.
<hr>
