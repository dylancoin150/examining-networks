<p align="center">
<img src=https://www.appdynamics.com/c/r/appdynamics/solutions/azure-monitoring/index/jcr:content/Title/blade_copy_172843868/bladeContents1/image/image.img.png/1670878360555.png>
</p>

<h1>Analyzing Networks Using an Azure Virtual Machine (Windows)</h1>
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

<p align="center">
<img width="1469" alt="Screenshot 2024-03-02 at 12 07 31 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/1544830c-d5af-4de4-9e1d-6b9fab1758e1">
</p>
<p align="center">
1. Login to the Microsoft Azure Portal
</p>
<br />

<p align="center">
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 12 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/815e70fc-1074-40c6-a507-76ac4434c237">
</p>
<p align="center">
2. Click on "Resource Groups" at the top of the portal (1). If "Resource Groups" is not there, you can navigate to the page by searching for "Resource Groups" using the search bar.
</p>
<br />

<p align="center">
<img width="1468" alt="Screenshot 2024-03-02 at 12 09 08 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/d8e5609b-a1a9-4289-bc0e-246f09b69d93">
</p>
<p align="center">
3. Click on "Create," (1) to create a new resource group.
</p>
<br />

<p align="center">
<img width="774" alt="Screenshot 2024-03-02 at 12 32 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/efdb8fa3-1c80-48b0-8b3d-647d05cbdc93">
</p>
<p align="center">
4. Name your resource group (1) and click on "Review + Create.," (2).
</p>
<br />

<p align="center">
<img width="660" alt="Screenshot 2024-03-02 at 12 35 01 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/6b877cc3-cd2d-40dd-b1a0-8b75c6662f82">
</p>
<p align="center">
5. If there are any issues, use the tabs "Basic, Tags, and Review + Create" (1) to navigate through the setup of the resource group to address any issues. If your validation passes, click "Create," (2).
</p>
<br />

<p align="center">
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 25 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/3371da2e-112b-4ce0-bef1-27af58a1b542">
</p>
<p align="center">
6. Go back to the home page of the Azure Portal (1) and click on "Virtual Machines" (2) at the top of the screen. If it is not at the top of your screen, as pictured above, you can use the search bar to type in "Virtual Machines," and navigate to the page that way.
</p>
<br />

<p align="center">
<img width="1464" alt="Screenshot 2024-03-02 at 12 11 54 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/02003e91-5efc-4447-9f77-fec4563ee107">
</p>
<p align="center">
7. Click "Create" (1) and choose the first option "Azure Virtual Machine," (1).
</p>
<br />

<p align="center">
<img width="877" alt="Screenshot 2024-03-02 at 12 36 45 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/df09e92d-1a38-4b6d-841d-da8d1a99bf07">
</p>
<p align="center">
8. Connect your Virtual Machine to the resource group we created by selecting it from the drop-down list (1). Name your virtual machine, in this case, we are naming it "VM1," (2). Choose the OS (Operating System), we are using Windows 11 Pro (3), and choose your disk size, we are using 4 VCPUs and 16 GiB memory (4).
</p>
<br />

<p align="center">
<img width="845" alt="Screenshot 2024-03-02 at 12 37 53 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/d0645ca2-0461-4fb2-a7ea-fcf37ab6ce79">
</p>
<p align="center">
9. Create your username and password for VM1 (1). Because we are using Windows you will need to check the box stating that you have a Windows license (2), if you have questions about that, you can click the hyperlink underneath the checkbox. Make sure you remember this information as you will need it to log in using Remote Desktop. Once finished, click on "Review + Create," (3).
</p>
<br />

<p align="center">
<img width="761" alt="Screenshot 2024-03-02 at 12 39 51 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/0cc05282-711f-4c29-8a1e-6744e6a1638b">
</p>
<p align="center">
10. If there are any issues, use the tabs "Basic, Disks, Networking, Management, Advanced, Tags, and Review + Create" (1) to navigate through the setup of the virtual machine to address any issues. If your validation passes, review the cost of the virtual machine, here it is $0.1920/hr, and click "Create," (2).
</p>
<br />

<p align="center">
<img width="69" alt="Screenshot 2024-03-02 at 12 42 16 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/f8f0c59a-70c0-44b3-b34c-d5b41a9660d9">
</p>
<p align="center">
11.  Open up "Microsoft Remote Desktop"
</p>
<br />

<p align="center">
<img width="587" alt="Screenshot 2024-03-02 at 12 42 10 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/e9da9f33-cc2e-4a0b-b5d6-5a09a2d4b779">
</p>
<p align="center">
12.  Click on "Add PC," (1).
</p>
<br />

<p align="center">
<img width="1341" alt="Screenshot 2024-03-02 at 12 43 58 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/62eadd9e-b99e-4db0-8d15-579960ffdcbf">
</p>
<p align="center">
13. Navigate back to the Azure portal (step 1), go to your virtual machines (step 6), and click on the virtual machine just created, VM1. This will open up all of the information and settings for VM1, shown above. On this page, you will see where it says "Public IP Address" and next to it will be your virtual machine's public IP address (1).
</p>
<br />

<p align="center">
<img width="517" alt="Screenshot 2024-03-02 at 12 43 20 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/fccd909e-636c-44f1-a947-2e6148742bc3">
</p>
<p align="center">
14. Back in Microsoft Remote Desktop, type or paste your virtual machine's public IP address into the blank next to "PC name" (1) and then click "Add," (2).
</p>
<br />

<p align="center">
<img width="578" alt="Screenshot 2024-03-02 at 12 54 42 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/b95914c3-7afb-4115-bf7e-aa29d0e2314c">
</p>
<p align="center">
15. Once added, a blank desktop will appear on the screen of "Microsoft Remote Desktop" with the IP address underneath (1). Click on it and a pop-up will appear for you to enter the login information for the virtual machine created when creating the virtual machine. Input the username and password (2) and click "Continue," (3).
</p>
<br />

<p align="center">
<img width="588" alt="Screenshot 2024-03-02 at 12 54 53 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/e5a653eb-b2e3-4023-9551-65acb67ac464">
</p>
<p align="center">
16. Another pop-up will appear saying the connection may not be secure, click "Continue," (1).
</p>
<br />

<p align="center">
<img width="1678" alt="Screenshot 2024-03-02 at 12 57 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/411df593-3707-44fe-a7bb-3b03f2590b2e">
</p>
<p align="center">
17. Your virtual machine will automatically boot up and bring up a new desktop on your computer. When your virtual machine first opens, there will be a lot of options you can choose to disable or enable. For what we are doing we don't need to worry about disabling or enabling anything here, so you can skip past it by clicking "Accept," (1).
</p>
<br />

<p align="center">
<img width="902" alt="Screenshot 2024-03-02 at 12 58 06 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/c12d035a-36e7-4458-a598-8ae35691a82a">
</p>
<p align="center">
18. Once you've logged into your virtual machine, navigate to the Windows icon at the bottom of the screen (1), type "cmd" into the search bar directly next to the Windows icon (2), and click on "Run as administrator," (3).
</p>
<br />

<p align="center">
<img width="463" alt="Screenshot 2024-03-02 at 1 22 18 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/3d634a47-b08a-4a1b-8ce8-3a5dd93918f5">
</p>
<p align="center">
19. Once Command Prompt opens, type in the command "nslookup www.google.com," (1). This makes your computer ask the DNS server to find out what Google's IP address is.
</p>
<br />

<p align="center">
<img width="1213" alt="Screenshot 2024-03-02 at 1 09 00 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/07af9a4e-8966-4c7e-88c0-90047545c9b2">
</p>
<p align="center">
20. Type in "ping www.google.com" into the command line (1). This sends the host, in this case www.google.com, ICMP packets and waits to see how long it takes for the host to send it back. This command is used to test network connectivity.
</p>
<br />

<p align="center">
<img width="1198" alt="Screenshot 2024-03-02 at 1 16 55 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/f5848647-5630-4b44-a2e4-e3585eb2abcc">
</p>
<p align="center">
21. Type in the command "ipconfig," (1). This command allows you to view and manage network configuration settings including your IPv4 and IPv6 addresses as well as your subnet mask.
</p>
<br />

<p align="center">
<img width="776" alt="Screenshot 2024-03-02 at 1 17 24 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/659e22ab-c4f1-4ca6-9b10-bb0ea56a3c8b">
</p>
<p align="center">
22. Exit out of Command Prompt and click on the Windows icon at the bottom of your screen (1). Then click the power icon and shut down the virtual machine (2). This may bring up an error message stating that the connection was lost so you have to close out of the window, in that case click "Close."
</p>
<br />

<p align="center">
<img width="1343" alt="Screenshot 2024-03-02 at 1 18 46 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/90841ec9-88c5-4429-abc9-eab8cc4ee9d6">
</p>
<p align="center">
23. Go to the Azure portal (step 1), navigate to your resource groups (step 2), and click on the one created for this. At the top. towards the middle, click on "Delete resource group" (1) and a window should pop up on the side. To delete your resource group, and everything in it, you have to click on "Apply force delete for selected virtual machines and virtual machine scale sets," (2), and then, under that check box, you have to type in the name of the resource group (3), and click "Delete," (4).
</p>
<br />

<p align="center">
<img width="587" alt="Screenshot 2024-03-02 at 1 19 05 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/aee1c921-1eb4-4766-b9de-76d3c1e609c4">
</p>
<p align="center">
24. Inside the "Microsoft Remote Desktop" app click on the trash can that pops up when you hover over the desktop preview of your virtual machine (1), you can double-check that it's your virtual machine by looking at the IP address under the desktop preview (2).
</p>
<br />

<p align="center">
<img width="340" alt="Screenshot 2024-03-02 at 1 19 12 PM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/fe1030bf-c42f-4440-b375-b7bda4879ae5">
</p>
<p align="center">
25. A message will pop up asking you if you're sure that you want to delete that remote desktop connection, stating also that it will not delete any user accounts or gateways used to access the PC. Click "Delete," (1).
</p>
<br />

<p align="center">
<img width="1462" alt="Screenshot 2024-03-22 at 10 53 12 AM" src="https://github.com/dylancoin150/examining-networks/assets/159479498/d68802b2-75ab-443c-9b04-478a7510a7a8">
</p>
<p align="center">
26. Navigate back to the Azure portal (step 1) and go into your subscription, virtual machine, and resource group sections (1) to look at costs and to ensure that everything was deleted properly. Sometimes a new resource group will be created from one of the networking settings on the VM, so always make sure everything is properly deleted.
</p>
<br />
