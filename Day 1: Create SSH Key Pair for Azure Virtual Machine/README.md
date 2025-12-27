# Day 1: Create SSH Key Pair for Azure Virtual Machine
## TASK
The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the Azure cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations. By breaking down the migration into smaller tasks, the Nautilus DevOps team can systematically progress through each stage, allowing for better control, risk mitigation, and optimization of resources throughout the migration process.  

For this task, create an SSH key pair with the following requirements:  
The name of the SSH key pair should be **nautilus-kp**.  
The key pair **type** must be **rsa**.   

## Theory  
### What is an SSH Key Pair in Azure?  
An SSH key pair in Azure is a set of cryptographic credentials used to securely authenticate users to Linux-based Azure Virtual Machines. It consists of:  
•  Public Key  
Stored in Azure and injected into the virtual machine during creation.  
•  Private Key  
Downloaded by the user at creation time and used to authenticate SSH access. This file must be kept secure.  
Azure uses asymmetric cryptography, where the private key proves identity without exposing sensitive credentials over the network.  

### Why is an SSH Key Pair Required?  
•  SSH key pairs provide secure, password-less authentication  
•  Password-based login is disabled by default for Linux virtual machines  
•  SSH keys significantly reduce the risk of brute-force and credential-based attacks  
Without a valid SSH key pair, secure access to a Linux Azure VM is not possible.  

### SSH Key Types in Azure  
Azure supports multiple SSH key formats. In this task, the RSA SSH key type was used.  
•  RSA  
Widely supported and compatible with OpenSSH  
Commonly used for Linux virtual machines  
Supported by most automation and configuration tools  

### SSH Key Use Cases  
•  Secure SSH access to Azure Virtual Machines  
•  Authentication during VM provisioning  
•  Used by automation tools such as Ansible, Terraform, and CI CD pipelines  
•  Access management in multi-user cloud environments  

### Security Best Practices  
•  Never commit private SSH key files to GitHub or public repositories  
•  Store private keys securely with restricted file permissions  
•  Rotate SSH keys if a private key is compromised or exposed  

### Outcome of This Task  
By completing this task, an RSA-based SSH key pair named nautilus-kp was created in Azure, enabling secure access to Linux virtual machines as part of the cloud migration strategy.  

### Steps Performed  
1.   Logged in to the Azure Portal using the provided credentials.  
2.   Searched for SSH keys in the Azure portal search bar and opened the SSH keys service.  
3.   Clicked Create and provided the following details:  
•  Resource group: Selected an existing resource group from the drop-down  
•  Key pair name: nautilus-kp  
•  SSH key type: RSA SSH format  
4.   Clicked Review + Create, then Create, and downloaded the private key file.  
5.   Verified key pair creation using the Azure CLI on the KodeKloud host:   **az sshkey list**

**Verification**  
*Azure Portal UI*
<img width="1919" height="466" alt="image" src="https://github.com/user-attachments/assets/066fa624-d0c1-4fda-92d8-1cb746028c10" />  

  
*Azure CLI*
<img width="1895" height="387" alt="image" src="https://github.com/user-attachments/assets/5d516f61-5c22-4512-8e48-5063140f6d3c" />  
