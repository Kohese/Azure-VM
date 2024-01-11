
# Azure-VM

This homelab is my first introduction to Azure and using it set up virtual machines. I was able to use Azure to confiure a Windows 10 virtual machine and use basic powershell scripting to send files from the VM to a storage account on Azure.

## Technologies Used

- Microsoft Azure

- Virtual Machine running Windows 10 Pro

- RDP

- Powershell


I was able to configure the VM and start the service with no problems. Azure gives users many differnt methods for connecting to these machines, so I was able to utilize the **Remote Desktop Connection** on my host machine to connect to the VM over **RDP** with the username and password of my Admin account.

<p align="center">
    <img src=assets/REMOTECONNECT.png width="400px" alt="remote connection" style="object-fit:contain"/>
  <img src=assets/PASSWORDAUTH.png width="400px" alt="remote connection"/>
</p>

Inside of Azure, I was able to create a storage account that would be used to store files sent from the VM.

<p align="center">
  
  <img src=assets/STORAGEACCOUNT.png width="700px" style="display:block; margin:auto;" alt="storage account"/>
</p>
To do this, I had to add a container inside of my storage account, and use the access contol within the container to give my VM permission to read and write files to the container.

<br />

From there, I could run a script in Powershell that takes a file as a parameter and writes the file to the storage container.

<div>

  <img src=assets/PS1SCRIPT.png alt="Powershell script" width="1000px"/>

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  
  <img src=assets/SENTFROMVM.png alt="File sent from VM" width="1000px"/>

</div>
