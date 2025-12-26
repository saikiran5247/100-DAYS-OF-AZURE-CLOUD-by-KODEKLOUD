# Day 1: Create SSH Key Pair for Azure Virtual Machine
## TASK
The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the Azure cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations. By breaking down the migration into smaller tasks, the Nautilus DevOps team can systematically progress through each stage, allowing for better control, risk mitigation, and optimization of resources throughout the migration process.  

For this task, create an SSH key pair with the following requirements:  
The name of the SSH key pair should be **nautilus-kp**.  
The key pair **type** must be **rsa**.  

Use below given Azure Credentials: (You can run the showcreds command on the azure-client host to retrieve these credentials)  
Portal URL:	https://portal.azure.com  
Username:	kk_lab_user_main-42d794ab7cd548f8@azurefreekmlprod.onmicrosoft.com  
Password:	Aa-JZf5P  
Start Time:	Fri Dec 26 08:13:18 UTC 2025  
End Time:	Fri Dec 26 09:13:18 UTC 2025  

## STEPS:
1. Click on the portal url from the given Azure credentials and enter the username and password to login. We will now be in Microsoft Azure console.
2. Search for SSH keys in search tab and click on SSH keys.
3. In the SSH keys section, click on create and create the keys entering:
   
   Resource group - select the existing one from drop-down menu
   Key pair name - **nautilus-kp**
   SSH key type - **RSA SSH Format**
   Click on **review+create** -> **create** -> **download and go to resources**
4. That's it, the SSH keys are created and the task it completed. You can view the SSH keys in the UI or even through the CLI on KodeKloud by entering: **az sshkey list**

5. **UI**
   <img width="1919" height="466" alt="image" src="https://github.com/user-attachments/assets/066fa624-d0c1-4fda-92d8-1cb746028c10" />

7.  **CLI**
   <img width="1895" height="387" alt="image" src="https://github.com/user-attachments/assets/5d516f61-5c22-4512-8e48-5063140f6d3c" />
