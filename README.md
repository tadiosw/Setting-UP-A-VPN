<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>

<p align="center">
    <img src="https://i.imgur.com/Grb44gD.png" height="70%" width="70%" alt="ProtonVPN logo"/>
</p>

<h1>Proton VPN - Setup and Usage</h1>
<p>This tutorial will guide you through the process of retrieving and observing IP addresses of computers in different locations. We will first observe your own desktop's IP address, then the IP addresses inside a Microsoft Azure virtual machine (VM). Finally, we'll use Proton VPN to change the IP address and observe the changes.</p>

<h2>Video Demonstration</h2>
<p>For a visual guide on how to install Proton VPN, check out the video below:</p>
<ul>
    <li><a href="https://clipchamp.com/watch/owUcTrGNUxf">How To Install Proton VPN with Prerequisites</a></li>
</ul>

<h2>Environments and Technologies Used</h2>
<ul>
    <li>Microsoft Azure (Virtual Machines/Compute)</li>
    <li>Remote Desktop</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
    <li>Windows 10 (21H2)</li>
</ul>

<h2>Installation Steps</h2>

<h3>Step 1: Check Your Desktop IP Address</h3>
<p>On your desktop, open a browser and go to <a href="https://whatismyipaddress.com/">https://whatismyipaddress.com/</a>. Here, you can view your current IPv4 address and location.</p>
<p align="center">
    <img src="https://i.imgur.com/37yHrFL.png" height="80%" width="80%" alt="Proton VPN Setup"/>
</p>
<p>Note down your IPv4 address and location for future reference.</p>

<h3>Step 2: Create a Virtual Machine (VM) in Azure</h3>
<p>In your Azure portal, create a new Virtual Machine with the following settings:</p>
<ul>
    <li>VM Name: VPNPractice</li>
    <li>Region: Europe (France Central)</li>
    <li>Image: Windows 10</li>
    <li>Size: 2 vCPUs</li>
    <li>Username: labuser</li>
    <li>Password: (Create a memorable password)</li>
</ul>
<p>Once you've filled in the details, click "Review + Create" to finalize the VM creation process.</p>
<p align="center">
    <img src="https://i.imgur.com/65vRsY7.png" height="80%" width="80%" alt="Create Virtual Machine"/>
</p>

<h3>Step 3: Connect to the VM via Remote Desktop</h3>
<p>After your VM is created, copy the VM’s "Public IP Address" from the Azure portal.</p>
<p align="center">
    <img src="https://i.imgur.com/vhO3b4K.png" height="50%" width="50%" alt="Copy Public IP"/>
</p>
<p>On your computer, open the "Remote Desktop" application (Windows) or "Microsoft Remote Desktop" (Mac). Paste the IP address into the application, and enter the username and password you created earlier.</p>
<p align="center">
    <img src="https://i.imgur.com/JHkENa8.png" height="70%" width="70%" alt="Remote Desktop Connection"/>
</p>

<h3>Step 4: Check the VM’s IP Address</h3>
<p>Once connected to the VM, open a browser inside the VM and go to <a href="https://whatismyipaddress.com/">https://whatismyipaddress.com/</a> again to check the IPv4 address and location.</p>
<p align="center">
    <img src="https://i.imgur.com/XVa490G.png" height="80%" width="80%" alt="VM IP Address"/>
</p>
<p>The location should show "Paris, France." Take note of the IPv4 address for future comparison.</p>

<h3>Step 5: Create a Proton VPN Account</h3>
<p>On your personal computer (not inside the VM), go to <a href="https://protonvpn.com/">https://protonvpn.com/</a> and click "Create a free account."</p>
<p align="center">
    <img src="https://i.imgur.com/0cqZPPT.png" height="80%" width="80%" alt="Create Proton VPN Account"/>
</p>
<p>On the Proton VPN website, scroll down to find the free plan and click "Get VPN Free." Then proceed to create your personal account.</p>
<p align="center">
    <img src="https://i.imgur.com/XnQFxbS.png" height="80%" width="80%" alt="Get Free VPN"/>
</p>

<h3>Step 6: Download Proton VPN</h3>
<p>Now, go back to your VM and log in to your Proton VPN account. From the dashboard, click on the "Downloads" tab on the left side. Find the Windows option and click "Download."</p>
<p align="center">
    <img src="https://i.imgur.com/hTC0mJk.png" height="80%" width="80%" alt="Download Proton VPN"/>
</p>
<p>After downloading, follow the instructions to install Proton VPN on your VM.</p>

<h3>Step 7: Connect to a VPN Server (Japan)</h3>
<p>Once Proton VPN is installed, open the app. You'll see the main screen with an option to connect. Hover over "Japan" in the list of available countries and click "Connect." This will route your internet connection through the Japan server.</p>
<p align="center">
    <img src="https://i.imgur.com/88VzKS8.png" height="80%" width="80%" alt="Connect to Japan VPN"/>
</p>
<p>If your remote desktop connection freezes, simply reload Remote Desktop. You should now be connected to the Japan VPN server.</p>

<h3>Step 8: Verify the IP Address Change</h3>
<p>Go back to <a href="https://whatismyipaddress.com/">https://whatismyipaddress.com/</a> and check the IP address again. You should see that your virtual machine's IP address has changed to Japan!</p>
<p align="center">
    <img src="https://i.imgur.com/jglmi2J.png" height="80%" width="80%" alt="New Japan IP"/>
</p>

<h3>Step 9: Browse Websites</h3>
<p>Now that you're connected to the Japan VPN, you can browse the web with a new IP address. Try searching on websites like Google, Netflix, or Starbucks to see the difference in location-based results.</p>
<p align="center">
    <img src="https://i.imgur.com/voXnfNz.jpg" height="80%" width="80%" alt="Browse Websites"/>
    <img src="https://i.imgur.com/DdruEyP.jpg" height="80%" width="80%" alt="Browsing Websites"/>
</p>

<h3>Step 10: Delete the Virtual Machine</h3>
<p>Once you're done, remember to delete your VM and the resource group in Azure to avoid unnecessary charges. Afterward, log off from Remote Desktop, and you're all set!</p>
<p align="center">
    <img src="https://i.imgur.com/DPBJBdT.png" height="80%" width="80%" alt="Delete Virtual Machine"/>
    <img src="https://i.imgur.com/T2VpIPn.png" height="80%" width="80%" alt="Delete Resources"/>
</p>

</body>
</html>
