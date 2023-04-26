# Hacking-Game-Coach

## Setup instructions

1- Download files from the Setup folder 

2- Start Azure CloudShell

3- Upload to CloudShell the files downloaded from Stup folder 

4- If you have many subscriptions, set the subscription where you are going to deploy the environment. for this, you can use the cmd "AZ-SetContext".
    
    Example: Set-AzContext -SubscriptionId "79c2a240-1a7f-482f-a315-xxxxxxxxx"
    
5- Run the script deploy.ps1
  
  >**Note**: Don't worry about Warning messages

6- Once the deployment is done, share with attendees information about hack-vm that you get on the output section:
  - IPAddress
  - Login
  - Password 

## Solution

1- Connect to the hack-vm using RDP. Your coach will provide you with the Public IP address and credentials.

2- Use a tool from the toolbox to discover the private IP address of the workstation-vm.
  
  - Download and install Nmap from "https://nmap.org/download.html"
  - run Nmap to scan the local network of hack-vm 10.0.0.0/24
  - In the result you can see that the port rdp 3389 is open on the vm 10.0.0.100
 
3- Use a tool from the toolbox to find the login and password that will allow you to connect to the workstation-vm using RDP.
  - Download Hydra application from https://github.com/maaaaz/thc-hydra-windows
  - Download username.txt and password.txt files 
  - Using Hydra application run a brut force attack on rdp port of the vm 10.0.0.100. 
    
    cmd: 
    
  - After some attempt, the application will stop and you can see, the login and the password that have worked 
  - 



## Clean 
1- Run the script delete.ps1
