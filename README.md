
![6320f4525eab744205bc21b6_Microsoft-Azure-Logo](https://github.com/user-attachments/assets/9cd1e085-8a21-48c1-bab9-07e21fd18ded)

<h1> Creating Virtual Networks and Virtual Machines </h1>


This tutorial provides a comprehensive guide to creating resource groups for virtual machines. We will be using Azure Virtual Machine and Windows Remote Desktop. Finally, we’ll perform various network-related tasks using the virtual machines, giving you hands-on experience managing and configuring network activities.

<h2>Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 Pro (22H2)
- Linux, Ubuntu Server 24.04 LTS - x64 Gen 2. 

<h2>Creating Our Resources & Virtual Machines </h2> 
<br>

<h3>Create The Resource Group</h3>

![image](https://github.com/user-attachments/assets/5feed575-279e-4c40-b8be-2be160231aea)
<br>
  
- Go to https://portal.azure.com/#home to get started
  
- Search or find Resource Groups and click on create
  
- I used RG-Network for my Resource Group. For the region, I selected East US 2, as I am located on the East Coast.
  <br><br>

<h3>Create The Windows Virtual Machine With The Virtual Network</h3>


- Here is the created resource group
  
![image](https://github.com/user-attachments/assets/da868e7e-1873-496c-8a13-7af77673b6f5)
 <br><br>

![image](https://github.com/user-attachments/assets/1264f732-91e1-4394-ade8-8025a60f3583)
<br><br>

- Search for Virtual Machines and hit create 

- Select your resource group(RG-Network), for the virtual machine name I named it Windows-VM
  
- Set Region to East US2.

- Set image to Windows 10 Pro, version 22H2 x64 Gen2

![image](https://github.com/user-attachments/assets/dcafaaf2-dccb-4d32-8e5d-d7b22dccbc8a)
<br><br>
  
- Select Size - You want at least 2 vcpus or the Virtual Machine will run slow in Azure

- Create a password and username and then record them down for safekeeping.

  
<br><br>

![image](https://github.com/user-attachments/assets/c4c69167-a218-4fe6-9646-a666a149c435)
<br><br>
- Click on the box to confirm licensing.

<br><br>

![image](https://github.com/user-attachments/assets/a91c4d10-f950-4d09-a0ef-cec6f0f9b1d1)

<br><br>

- Under the "Networking" tab, my virtual network name was automatically assigned. To create a new one, click on “Create New.”
  
<br><br>

![image](https://github.com/user-attachments/assets/43188b88-b3e6-4e58-933d-12bd8b8afdbf)

<br><br>

- I have named it to Lab-Vnet. Please confirm by pressing OK, and this will be the new name for the virtual network.
  
<br><br>

![image](https://github.com/user-attachments/assets/46191026-8d56-4d13-9d2a-c7a73dd8e8cd)

<br><br>

![image](https://github.com/user-attachments/assets/4c6c7cdd-1f38-4701-9c8f-fa10515484b6)
<br><br>

- Click on Create and the Virtual Machine will be created.

<h3>Create The Linux Server Virtual Machine</h3>

<br>

![image](https://github.com/user-attachments/assets/1835a4c7-acc7-405b-97bc-4211f4376c2b)
<br><br>

- Create another Virtual Machine.
- Selected RG-Network for Resource Group.
- Region - East US 2
- Choose Unbuntu Server 24.22
<br>

![image](https://github.com/user-attachments/assets/8d5bab90-883e-4f9d-8543-d7d514849bda)
<br><br>

- Choose 2vcpu option
- Click on Password for Authentication type.
- Create a password.

<br>

![image](https://github.com/user-attachments/assets/c59c1db5-6327-47ab-af96-9fb067e84cc2)
<br><br>

- Under the "Networking" tabs. Select Lab-Vnet for Virtual Network.
- Click Review + Create, and a New Virtual Machine will be created.
  
<br>


<br><br>

![image](https://github.com/user-attachments/assets/38cf8d3a-fb28-4c31-ac67-f94d5d599445)
<br><br>

- Here are the 2 Virtual Machines.
  
<br><br>
![image](https://github.com/user-attachments/assets/8271269c-5cdb-46f9-939e-7329d53c9c04)
<br>>br>

- If you are confident that you have entered all the information accurately, yet you are still unable to establish a remote desktop connection to the virtual machine, the issue may be related to the password.

- To reset your password, please access the Azure portal. Select your Windows virtual machine, navigate to the "Help" section, and click on "Reset password." Enter your new password and then select "Update." This process should effectively resolve the issue.

<br>

<h3>Accessing Virtual Machines Through Windows Remote Desktop</h3>

![image](https://github.com/user-attachments/assets/06db41ea-506b-49d9-9a51-4f5630c99c14)
<br><br>

- In the Azure portal Copy the Windows-VM public IP address.

<br>

![image](https://github.com/user-attachments/assets/b2c68eae-3e05-4498-a73a-32ac4bce4152)
<br><br>

-Click the start window and search for Remote Desktop. Open Remote Desktop Communications.

<br>

![image](https://github.com/user-attachments/assets/e3c82e14-432c-41f0-b6ba-4dd4be9e3905)

![image](https://github.com/user-attachments/assets/7253116c-32ec-446e-9481-8252cf598f29)

<br><br>

- Paste the IP address in the Remote Desktop and click connect.
- Type in Username and password.

<br>

![image](https://github.com/user-attachments/assets/2a7c11af-2b05-47ae-9904-8677d350783f)


<br><br>

- Here is the Virtual Machine in Windows 10
  
<br><br>

<h2>Performing Activities on the Network</h2>
<br>

<h3>Download Wireshark </h3>

![image](https://github.com/user-attachments/assets/1dc4d169-5fbb-4fcb-aecd-ef42a1f9e948)

- Download Wireshark on this virtual machine, here is the link https://www.wireshark.org

- Download Windowsx64 Installer.
- When it is done downloading open the file and go through the procedure for installing the software which we will mostly say yes and agree

- Wireshark is a protocol analyzer that lets us do traffic examination and observe traffic between the 2 virtual machines.
<be>

![image](https://github.com/user-attachments/assets/d0da1325-9e9d-4063-80ec-26d3ade876be)

<br><br>

- Open Wireshark. Click and highlight "Ethernet" and Click on the blue sharkfin on the top left.

<br>


![image](https://github.com/user-attachments/assets/c2c99b94-5ca7-472a-8386-823b103f4611)
<br><br>

- This is how the screen will look. To zoom in, click on the magnifier with the + on it.
  
- This is all the network traffic that is happening on the back end of the computer
   

<br><br>
<h3>Filter for ICMP Traffic </h3>

- The next thing we will do is filter for ICMP traffic, first type ICMP in the search bar this will show only ICMP or ping traffic

- This traffic is what ping uses, the ping command is what we use to test connectivity between 2 devices



![image](https://github.com/user-attachments/assets/c68120e5-d864-4ac6-af3b-553b7f4cdcb2)
<br><br>

-The Linux VM Private IP address is 10.0.0.5
  
![image](https://github.com/user-attachments/assets/fe671af4-d031-4f11-8ce3-ba41dbe7cc8e)


<h3>Launch Windows Powershell </h3>

![image](https://github.com/user-attachments/assets/3986c37a-4341-489f-b259-c3cc00a4ed7a)

![image](https://github.com/user-attachments/assets/b446b4a4-2ac9-4242-950d-b44a9eb972d9)



- Type ping in the Windows Powershell application, then type the private IP address of the Linux Virtual Machine 10.0.0.5.

- We will attempt to ping this IP address from the Windows Virtual Machine

- The feedback we will get from The Linux VM is reply, reply, reply, reply in the Powershell and traffic Wireshark.


<br><br>

![image](https://github.com/user-attachments/assets/7b974787-db50-4a52-b556-331d3509fd57)


- Press the green shark fin under Edit in Wireshark called "Restart Current Capture" then press continue without saving.

- Redo ping again in Powershell, you may see just 4 events happen in there for example reply, reply, reply but in Wireshark you see 8 events. That is because it captured both the request from the Windows computer, source - 10.0.0.4, and captured the reply from the Destination - 10.0.0.5, Linux computer, another request from the Windows computer and reply from the Linux Computer.


<br><br>

<img width="1363" alt="Screenshot 2024-10-27 at 4 51 10 PM" src="https://github.com/user-attachments/assets/26c5add5-c7f5-44fe-abe4-8ccae110cf34">

- Click on a traffic.

- On the left side beneath the data, Expand Ethernet II tab and you see the Source and Destination MAC Address. It refers to the Physical address in Powershell

- It is a layer 2 addressing in the OSI Model
  
- In Windows Powershell type ipconfig /all and hit enter

![image](https://github.com/user-attachments/assets/6ae85533-ec3d-4c46-9f56-6f0897b3a865)
<br><br>

- The Physical Address highlighted is also the Source for the MAC address of the Windows VM and back to Wireshark the data above Source: is the Linux computer destination MAC address that we pinged
  
<br><be>
![image](https://github.com/user-attachments/assets/98b52a5c-57aa-4101-8646-5409680a279d)

<br><br>

- When you expand the Internet Protocol, this is representative of the network layer of the OSI model layer 3 you can see the source address and destination address

- The Windows virtual machine source address 10.0.0.4 is the private IP address that would be the IPv4 highlighted in the Windows Power shell with 10.0.0.5 in Wireshark being the Linux VM's Private IP address


<br>

![image](https://github.com/user-attachments/assets/dfe9b716-6772-47d5-a71f-37ea0c83d6ce)
<br><br>

- When you expand the Internet Control Message Protocol (ICMP) you can see data the actual payload of the data that was sent in the ping

- What you see here is the ICMP Echo request from the Windows computer. The next packet is the Echo reply from the Linux computer

- The data in here will essentially be reversed the source and destination possibly being flipped and the IP address source becomes the destination and this keeps going on throughout all the pings

![image](https://github.com/user-attachments/assets/cbfea7d6-bf8a-433d-889b-08a84fc1d039)
<be><br>

- Type in ping 10.0.0.5 -t will cause a non-stop ping 

<br><br>
<h3>Configuring a firewall to Block all incoming ping traffic </h3>

- In this step, we are going to block all incoming ping traffic coming from the Windows Virtual Machine to the Linux Virtual Machine and then observe what happens afterward

![image](https://github.com/user-attachments/assets/900450d7-834b-4bc2-b030-84e7c88b79bb)

<br><br>
![image](https://github.com/user-attachments/assets/2e50c253-8426-49b8-92d4-11a87c831bc9)

<br><br>

![image](https://github.com/user-attachments/assets/b7553ea9-1212-4c64-bee6-48df140ec388)
<br><br>

- Go to the Azure portal and search for Network Security Groups, Click on your Linux-VM , Click on Settings
- Click on inbound security rule.

- This is the firewall for the Linux computer

- For this step hit the drop-down arrow for settings and click on inbound security rules, with this we will create a rule for traffic coming inbound to the virtual machine
  <br><br>
  
- Click on Add to begin the process of creating a rule
<br><br>

![image](https://github.com/user-attachments/assets/7c566fe1-8661-4b0f-83d4-c02a503d626d)
<br><br>

- What I have inputted for this lab

- There is an asterisk, which is referred to as any, placed in the destination port since ICMP doesn’t use a port

- Deny is selected to prevent ICMP from being pinged so the firewall will drop the traffic

- Priority is set to 290 because it would allow the rule to be evaluated first

- Then hit add

<br>

![image](https://github.com/user-attachments/assets/5f6b9f88-ac33-4d50-b721-2e8d28c12077)


- As you can see once the rule takes effect in Powershell everything will start to time out because the Linux virtual machine will begin to ignore the traffic and not reply to it.

- The rule we made denies incoming ICMP traffic from any source to any destination for the Linux virtual machine.

- In Wireshark what also changed is that instead of getting a steady request/ reply response it changed to just request because no response was found and the firewall is blocking the replies.

- This can go on forever.
  

<br><br>


![image](https://github.com/user-attachments/assets/26340cb5-5737-4f94-a0ca-aee710a4de90)
<br><br>

- We will be turning back on the Allow action for ICMP so that it can get a reply, to do that go back to Inbound security rules delete or edit the rule.
    
- Once the Azure resource manager picks up the requests then everything will flow back to normal like before we made that Deny (firewall) rule.

- Stop the ping activity with Control + C before moving on to the next step.

<br><br>


<h3>Observe SSH traffic </h3>

<img width="1060" alt="22" src="https://github.com/user-attachments/assets/4c1357e8-9119-4725-865e-f082e03ca728">

- SSH (Secure Shell) is used to make a secure connection from 1 computer to another computer, it uses TCP port 22

- In Wireshark, we are going to type in SSH to filter for that traffic

- Go to your Linux VM and copy the private IP address located in Overview -> Properties 

- go back to your Windows VM and Open Windows Powershell, type in ssh labuser@10.0.0.5, and press enter to connect to the Linux VM with SSH, confirm a yes again to continue connecting

- Finally enter the password you made for labuser
  
<br><br>

<img width="639" alt="23" src="https://github.com/user-attachments/assets/abef1814-17fd-4e1b-9f5e-c637cc6ed52a">


- The prompt looks different now because we are connected to the Linux machine


<br><br>

<img width="607" alt="24" src="https://github.com/user-attachments/assets/41e6663f-0a91-4104-92f4-737a257abb67">

- Type id this is our user id labuser

- Type hostname mine is Linux VM2

- Type uname -a this will give out stuff about the operating system

- Type pwd shows the labuser file path

- Type touch file.txt this creates a file on the Linux machine

- Type ls shows that the file was created

<br><br>

<img width="1114" alt="28" src="https://github.com/user-attachments/assets/9dda896b-60a9-4bcb-8d56-b88ae75335d9">

- Instead of SSH In Wireshark type in tcp.port==22 this will filter out all of the traffic that uses TCP port 22 
  
- Type in PowerShell ls and press enter because SSH uses TCP port 22 we can see in Wireshark it is being filtered out 
<br><br>

<img width="236" alt="26" src="https://github.com/user-attachments/assets/c38cb7e6-761a-40fd-a25b-9ba52c6b0bf0">

- Type in Powershell exit this will drop the connection and log us out
  
- Type in hostname to verify which VM you are back in
  
<br><br>

<h3>&#9320; Observe DHCP traffic </h3>


<img width="934" alt="30" src="https://github.com/user-attachments/assets/bb7359ca-ae43-4fbf-8594-47413b23cb72">

- In Wireshark, we are going to filter for DHCP traffic only

- DHCP uses ports 67 and 68 this protocol is used for the computer to assign itself an IP address to devices when they are first connected to the network

- Clear out what is in the filter and type in DHCP at the top of Wireshark you will not see any traffic running 

- Open Powershell as an administrator and type in ipconfig /renew then hit enter, if the discover packet did not show up then you have to filter out more

<br><br>
<img width="127" alt="Screenshot 2024-10-27 at 5 45 50 PM" src="https://github.com/user-attachments/assets/06a1c269-90f1-48d3-b47f-6bcbedb10dbf">
<br>


<img width="203" alt="Screenshot 2024-10-27 at 5 46 38 PM" src="https://github.com/user-attachments/assets/cb8f1f65-4057-419f-95d9-f5621ceb67dc">

<br>

<img width="121" alt="Screenshot 2024-10-27 at 5 47 27 PM" src="https://github.com/user-attachments/assets/3d0ddf6a-0dd0-4b48-a720-0e6819b60964">

<br>

<img width="210" alt="Screenshot 2024-10-27 at 5 47 57 PM" src="https://github.com/user-attachments/assets/6f1c8761-41f4-484b-8612-8f6221d91463">
<br><br>

- We will begin running a script
   
- Open Notepad and type in ipconfig /release underneath that ipconfig /renew

- Save what we typed out file -> save

- When the Save As options show up at the top type in c:\programdata

- Save the file name as dhcp.bat

- We will run this in Powershell to have it release all the IP addresses and then it should renew automatically coming back up after killing the network connection 
<br><br>

<img width="544" alt="Screenshot 2024-11-07 at 2 12 52 PM" src="https://github.com/user-attachments/assets/a39cfb36-aedc-4091-8ea8-f138d7bf237d">


- Type in Powershell cd c:\programdata to be inside the programdata

<br><br>

  <img width="533" alt="Screenshot 2024-11-07 at 2 13 10 PM" src="https://github.com/user-attachments/assets/9945f15d-973a-40ab-84ca-94fac1c8605c">


- Type ls for list and you can see dhcp.bat is in the program data that we saved

  <br><br>
  
<img width="650" alt="Screenshot 2024-11-07 at 2 14 36 PM" src="https://github.com/user-attachments/assets/b360088f-e9b4-4076-8b44-d38b533c0d44">

- To run dhcp you will first clear out the data in Wireshark then head back into Powershell and type in .\dhcp.bat and press enter

<br><br>

<img width="1015" alt="Screenshot 2024-11-07 at 2 15 41 PM" src="https://github.com/user-attachments/assets/eae60aa4-cfd2-4038-a86b-80db2b535a1b">

- The connection will die after you hit enter because Ipconfig \release happened but then automatically ipconfig \renew will kick in and restore the connection

- This is the DHCP traffic that was captured in Wireshark

- When release occurred the release packet was sent from the source computer (Windows) to the destination computer

- After the release script command of DHCP was executing the script executed ipconfig /renew making it no need to type that out cause there is no network connection anymore but the command still ran

- Discover happened with that occurring along with the other packets and so the source became zero because the IP address was released and the connection was dropped with the destination address as 255.255.255.255 a.k.a broadcast

- The DHCP server broadcasted back to my computer with a DHCP Offer request and then my computer sent a DHCP request packet to the DHCP server

- Finally, the DHCP server acknowledged the requests from them to my computer, and then an acknowledge request was sent which had my computer now acquire a new IP address 


<br><br>



<img width="644" alt="Screenshot 2024-11-07 at 2 16 50 PM" src="https://github.com/user-attachments/assets/ac6e3034-97da-4306-9133-ee6e5508fac4">

- This address was released and then re-requested by the computer

  
<br><br>


<h3>&#9321; Observe DNS traffic </h3>

<img width="1120" alt="31" src="https://github.com/user-attachments/assets/08659088-37f5-4340-a534-b810ef861dd2">

- First, we are going to filter out DNS traffic
  
- Type in the filter dns hit enter

- There will be a lot of DNS activity to make our own hit the green sharkfin at the top to restart this capture then press continue without saving to start fresh
<br><br>

<img width="600" alt="33" src="https://github.com/user-attachments/assets/0a348b78-6e73-4f50-b24e-b0e17dd1b30b">

- we are going to look for the IP address of disney.com

- In PowerShell type in nslookup disney.com and hit enter

- Once the computer reaches out to the DNS server the DNS server will find out and then tell us the IP address with a bunch of traffic following up behind


- Disney.com resolves to the IP address 130.211.198.204

<br><br>

<img width="1143" alt="32" src="https://github.com/user-attachments/assets/16281162-e100-407f-8ff9-2d1d4ede39e3">


- This is spam that happened on the back end of the nslookup for Disney

- DNS (resolves host names like human-readable names into IP addresses)

<br><br>


<img width="1002" alt="Screenshot 2024-10-27 at 5 54 22 PM" src="https://github.com/user-attachments/assets/a71ce1cc-3ab0-48b8-871a-b090c94a1d46">



- If you copy and paste the address 130.211.198.204 in a browser it will show something in correlation to Disney sometimes

- Sometimes you can load a modern website based on the IP address


<br><br>



<img width="1149" alt="34" src="https://github.com/user-attachments/assets/f8452888-503c-4793-8ef9-cb49428530c2">

- DNS uses TCP and UDP port 53

- In Wireshark type in udp.port==53 and you will still see all the DNS traffic the double equal sign means or

- DNS uses TCP in between DNS servers when they are sharing information, but when your computer looks up DNS records it uses UDP 

<br><br>

<h3>&#9322; Observe RDP traffic </h3>

<img width="599" alt="35" src="https://github.com/user-attachments/assets/7d7c7176-6bc4-46e3-8901-64485e385795">

- RDP (is used when remotely connecting from 1 computer to another to gain a remote desktop  GUI, the computer being connected is typically "listening" for a connection on TCP port 3389

- This remote desktop that we are using is an RDP connection

<br><br>

<img width="1034" alt="Screenshot 2024-11-07 at 2 31 36 PM" src="https://github.com/user-attachments/assets/bccfaf7c-3987-468e-9ab3-ad3835c48bbe">

- When filtering for tcp.port==3389 as you see there is a lot of spam because RDP is constantly streaming a picture from the server to our local machine; constantly sending stuff

- Compared to SSH which only sends traffic when your doing a single keystroke, it sends the keystroke to the server your connected too but RDP has to send an actual photograph

<h2> Congrats on Finishing the Tutorial! 🎉 </h2>


You’ve successfully navigated the process of creating resource groups, setting up virtual machines, and gaining remote desktop access from macOS. By following this tutorial, you’ve gained valuable hands-on experience in managing virtual networks and configuring network tasks. Well done on completing these essential steps—your newly acquired skills are a fantastic addition to your tech toolkit, and I’m confident they’ll serve you well in your future projects. Keep up the great work and continue exploring the endless possibilities of virtual network management!
