<h1>Examining Networks Using an Azure Virtual Machine (Windows)</h1>
This tutorial outlines setting up an Azure Virtual Machine and using Command Prompt to examine different aspects of networking within an environment.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine)
- Remote Desktop
- Command Prompt

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 Pro (22H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create Resources in Azure
- Connect to the Virtual Machine
- Execute commands to examine the network
- Clean up

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1469" alt="Screenshot 2024-03-02 at 12 07 31 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/54c51d57-5bbc-47e2-aba3-45d43b8e6ac9">
</p>
<p>
1. Login to the Microsoft Azure Portal
</p>
<br />

<p>
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 12 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/0335fa22-b12d-40cf-aa28-bdc772749e15">
</p>
<p>
2. Go to "Resource Groups" at the top of the portal. If "Resource Groups" is not there, you can navigate to the page by searching for "Resource Groups" using the search bar.
</p>
<br />

<p>
<img width="1468" alt="Screenshot 2024-03-02 at 12 09 08 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/b6741544-d150-4da4-921a-931729580318">
</p>
<p>
3. Create a new resource group.
</p>
<br />

<p>
<img width="774" alt="Screenshot 2024-03-02 at 12 32 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/a44b4246-e962-45cd-8cc0-ab7aa7dff477">
</p>
<p>
4. Name your resource group and click on "Review + Create."
</p>
<br />

<p>
<img width="660" alt="Screenshot 2024-03-02 at 12 35 01 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/b62d4f93-9e3a-4750-88a5-2488f9aed6b9">
</p>
<p>
5. If there are any issues, use the tabs "Basic, Tags, and Review + Create" to navigate through the setup of the resource group to address any issues. If your validation passes, click "Create."
</p>
<br />

<p>
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 25 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/2875ab09-26b0-4764-8cdd-cc6e6cf6eb70">
</p>
<p>
6. Go back to the home page of the Azure Portal and click on "Virtual Machines" at the top of the screen. If it is not at the top of your screen, as pictured above, you can use the search bar to type in "Virtual Machines," and navigate to the page that way.
</p>
<br />

<p>
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 54 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/a2f24c87-6bb0-41b0-a296-5627dbc90d22">
</p>
<p>
7. Click "Create" and choose the first option "Azure Virtual Machine."
</p>
<br />

<p>
<img width="877" alt="Screenshot 2024-03-02 at 12 36 45 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/a263a78b-6c6c-4b15-aaf1-01d876a75236">
</p>
<p>
8. Connect your Virtual Machine to the resource group we just created by selecting it from the drop-down list. Name your virtual machine, in this case, we are naming it "VM1." Choose the OS (Operating System) we are using Windows 11 Pro and choose your disk size, we are using 4 VCPUs and 16 GiB memory.
</p>
<br />

<p>
<img width="845" alt="Screenshot 2024-03-02 at 12 37 53 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/3147e4e1-a7aa-4b37-a3f8-947e5286f016">
</p>
<p>
9. Create your username and password for VM1. Make sure you remember this information as you will need it to log in using Remote Desktop. Once finished, click on "Review + Create."
</p>
<br />

<p>
<img width="761" alt="Screenshot 2024-03-02 at 12 39 51 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/da4049d0-457a-4089-a83b-115257730c3f">
</p>
<p>
10. If there are any issues, use the tabs "Basic, Disks, Networking, Management, Advanced, Tags, and Review + Create" to navigate through the setup of the virtual machine to address any issues. If your validation passes, review the cost of the virtual machine, here it is $0.1920/hr, and click "Create."
</p>
<br />

<p>
<img width="69" alt="Screenshot 2024-03-02 at 12 42 16 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/f8f0c59a-70c0-44b3-b34c-d5b41a9660d9">
</p>
<p>
<img width="587" alt="Screenshot 2024-03-02 at 12 42 10 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/f2f8ad04-9d00-45a8-977a-759932337070">
</p>
<p>
11. Open up "Microsoft Remote Desktop" and click on "Add PC.
</p>
<br />

<p>
<img width="1341" alt="Screenshot 2024-03-02 at 12 43 58 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/86151bf4-05bd-490d-8c22-ca494fefb014">
</p>
<p>
12. Navigate back to the Azure portal, go to your virtual machines, and click on the virtual machine just created, VM1. This will open up all of the information and settings for VM1. On the page that opens you will see where it says "Public IP Address" and next to it will be your virtual machine's public IP address.
</p>
<br />

<p>
<img width="517" alt="Screenshot 2024-03-02 at 12 43 20 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/048578f8-c76b-4c02-b97a-33b3d6763cd7">
</p>
<p>
12. Type or paste your virtual machine's public IP address into the blank next to "PC name" and then click "Add."
</p>
<br />

<p>
<img width="578" alt="Screenshot 2024-03-02 at 12 54 42 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/a9c83078-0323-4e07-93d2-46a8f9e74a31">
</p>
<p>
13. Once added, a blank desktop will appear on the screen of "Microsoft Remote Desktop" with the IP address underneath. Click on it and a pop-up will appear for you to enter the login information for the virtual machine created when creating the virtual machine. Input the username and password and click connect.
</p>
<br />

<p>
<img width="588" alt="Screenshot 2024-03-02 at 12 54 53 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/0b9537ac-84c9-4baa-834b-9b62ecf8cebb">
</p>
<p>
14. Another pop-up will appear saying the connection may not be secure, click continue.
</p>
<br />

<p>
<img width="1678" alt="Screenshot 2024-03-02 at 12 57 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/0a242e2e-67d2-4061-93f3-619e0788cf13">
</p>
<p>
15. Your virtual machine will automatically boot up and bring up a new desktop on your computer. When your virtual machine first opens, there will be a lot of options you can choose to disable or enable. For what we are doing we don't need to worry about disabling or enabling anything here, so you can just skip past it by clicking "Accept."
</p>
<br />

<p>
<img width="902" alt="Screenshot 2024-03-02 at 12 58 06 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/cd5a63b5-e44a-4748-9563-04f5357cd99e">
</p>
<p>
16. Once you've logged into your virtual machine, navigate to the Windows icon at the bottom of the screen, type "cmd" into the search bar directly next to the Windows icon, and click on "Run as administrator."
</p>
<br />

<p>
<img width="463" alt="Screenshot 2024-03-02 at 1 22 18 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/e8a99b25-30b1-4fda-86c5-cd16e009b5e4">
</p>
<p>
17. Once Command Prompt opens, type in the command "nslookup www.google.com." This makes your computer ask the DNS server to find out what Google's IP address is.
</p>
<br />

<p>
<img width="1213" alt="Screenshot 2024-03-02 at 1 09 00 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/99734e8d-e023-4d93-bdc6-db3d58d8c00d">
</p>
<p>
18. Type in "ping www.google.com" into the command line. This sends the host, in this case www.google.com, ICMP packets and waits to see how long it takes for the host to send it back. This command is used to test network connectivity.
</p>
<br />

<p>
<img width="1198" alt="Screenshot 2024-03-02 at 1 16 55 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/564b8d3d-1604-4b64-b15c-654b48843ceb">
</p>
<p>
19. Type in the command "ipconfig." This command allows you to view and manage network configuration settings including your IPv4 and IPv6 addresses as well as your subnet mask.
</p>
<br />

<p>
<img width="776" alt="Screenshot 2024-03-02 at 1 17 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/06db0a0a-6b0d-40dc-8458-d978de9bbdf8">
</p>
<p>
20. Exit out of Command Prompt and click on the Windows icon at the bottom of your screen. Then click on the power icon and shut down the virtual machine. This may bring up an error message stating that the connection was lost so you have to close out of the window, in that case just click "Close."
</p>
<br />

<p>
<img width="1343" alt="Screenshot 2024-03-02 at 1 18 46 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/8dd39610-ed4e-4b43-af3a-ad0beeeef5a3">
</p>
<p>
21. Go to the Azure portal, navigate to your resource groups, and click on the one created for this. At the top. towards the middle, click on "Delete resource group" and a window should pop up on the side. To delete your resource group, and everything in it, you have to click on "Apply force delete for selected virtual machines and virtual machine scale sets," and then, under that check box, you have to type in the name of the resource group, and click "Delete."
</p>
<br />

<p>
<img width="587" alt="Screenshot 2024-03-02 at 1 19 05 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/de786827-6bd8-4946-b68f-a34ee67b98ef">
</p>
<p>
22. Inside the "Microsoft Remote Desktop" App click on the trash can that pops up when you hover over the desktop preview of your virtual machine, you can double-check that it's your virtual machine by looking at the IP address under the desktop preview.
</p>
<br />

<p>
<img width="340" alt="Screenshot 2024-03-02 at 1 19 12 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/91ab2b7c-d592-4724-8e38-fa641d300a59">
</p>
<p>
23. A message will pop up asking you if you're sure that you want to delete that remote desktop connection, stating also that it will not delete any user accounts or gateways used to access the PC. Click "Delete."
</p>
<br />

<p>
<img width="1456" alt="Screenshot 2024-03-02 at 1 26 21 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/4e1148a6-abe2-4110-99bd-e2d0aa39f2c6">
</p>
<p>
24. Navigate back to the Azure portal and go into your virtual machine and resource group sections to ensure that everything was deleted properly. Sometimes a new resource group will be created from one of the networking settings on the VM creates, so make sure everything is properly deleted.
</p>
<br />
