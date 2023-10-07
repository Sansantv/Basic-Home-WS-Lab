<h1>Setting up a basic home lab with Windows Server and Powershell.</h1>



<h2>Description</h2>
<b>In this Lab, I will be creating a Simple Home Lab using Windows server to make a Domain Controller and manage an internal Network. A Powershell script is used to make multiple user accound to similate accounts under an Organization.
</b>
<br />
<br />
<h2>Languages Used</h2>

- <b>PowerShell:</b> Creation of Multiple User Accounts  
<h2>Utilities Used</h2>

- <b>Oracle Vm VirtualBox:</b> Home of the Virtual Machines
- <b>Windows Server:</b> Used to Host and create the Domain

<h2>Setting up the First VM</h2>
The First Virtual machine is going to be our Domain Controller. We set this up with 3 cores and 2048gb of RAM. I installed Windows Server using the Windows Server iso and set it up regularly.

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/a5039570-530c-4b23-aefb-0af61158dafa)

<br />
<br />
<h2>Naming the Internet and Internal Networks</h2>
I made sure to name both networks noticiable difference to make sure that there wouldn't be any mistakes later. 

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/c53eff40-deea-4748-b8f5-ec51b9939f69)
![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/255e4e3d-8eae-409e-9b8c-bc215e51ad30)
![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/1044a280-a052-4058-b7d7-c206a34f0f4a)
<br />
<h2>Set an Ip Address to the Interal NIC</h2>
I assigned the NIC an IP and also put the DNS as the Same so it would refer to itself(you can also use 126.0.0.1 for the DNS)
![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/658ac726-c45e-4029-a61e-c18b97bedb8c)

<br />
<h2>Created a Domain Controller and assigned it KindomHearts.com</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/1dff2ec7-5230-4924-9f94-240300043ee7)
<br />
<h2>Created a User account with admin privileges</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/177231f9-b277-4b9a-b196-b958f9d51c0f)
<br />
<h2>Enabled Remote access and created a NAT to the Internal NIC</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/e06f5956-326d-41c9-b074-c56ca2d7a784)
<br />
<h2>Using a Script to create multiple fake users through PowerShell.</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/4769c959-a7fe-4679-86eb-246016b908d8)

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/0d74da47-29a2-46bc-b7e4-c97cf1f4eb13)
<br />
<h2>Created a second Vm (Sora) as the “Client” within the server.</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/c2085945-8423-480e-b618-7831f9940a63)
<br />
<h2>Sora is connected to the network</h2>
Sora(Client) is able to connect to the internet through KingdomHearts.com(Domain Controller). It was able to ping google and the Domain Controller.

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/aaa2df92-e103-4e8b-97f2-bb21cf49920c)
<br />
<h2>Sora (Client) Joined the Domain Server.</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/4f4250bc-3071-4809-b085-00427ff8691f)
<br />
<h2>On the Domain Controller DHCP Page, Sora was Given an IP address with a Lease that last for 8 days.</h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/17a328a0-dc47-48d0-b4b0-4889745016bb)
<br />
<h2>Using the User Created by the PowerShell Script to log on to Sora since it is apart of the Domain. </h2>

![image](https://github.com/Sansantv/Basic-Home-WS-Lab/assets/143445179/571675c4-846a-47f6-947e-76721cb651e9)
<br />

<h2>Thats the end of this lab but the beginning of a bigger project! Hope to Have you along for the ride. Time to start piecing things together!</h2>
