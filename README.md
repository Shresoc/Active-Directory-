# Active-Directory-
Home Lab Running Active Directory (Oracle VirtualBox) | Add Users w/PowerShell


![Intro](https://github.com/Shresoc/Active-Directory-/assets/168186856/f7caf615-cbb7-4f43-ba13-3ac8e4d71433)

# Software Installation:

- Begin by downloading and installing Oracle VirtualBox on your personal computer
- Download the ISO files for Windows 10 and Windows Server 2019 that will be used to set up the virtual machines
- Create the first virtual machine in VirtualBox, which will act as the domain controller. Assign it two network adapters; one for external internet access and one for the private network.
- Install Windows Server 2019 on the newly created domain controller virtual machine.

# Configure Network Settings:

![Network Connection Details](https://github.com/Shresoc/Active-Directory-/assets/168186856/f4d2d28c-91b0-4192-91d1-e969b0555eb0)

- Assign IP addressing to the internal network adapter of the domain controller. The external adapter should automatically receive IP addressing from your home network.

  
![Assigning IP on the Internal Network](https://github.com/Shresoc/Active-Directory-/assets/168186856/69af2023-4239-4993-bf58-272513a914e7)
- Name the server and activate the installation.
# Install Active Directory and Setup Domain:
![Installing AD Domanin Services](https://github.com/Shresoc/Active-Directory-/assets/168186856/f8d659e0-4c5d-432a-8071-3229857c97c6)


![Domain Configuration](https://github.com/Shresoc/Active-Directory-/assets/168186856/766c31e9-b4be-40bb-9d1e-78e294b93531)

- Install Active Digital and set up a new domain on the domain controller.
  - With remote access setups :![Setting Up RAS](https://github.com/Shresoc/Active-Directory-/assets/168186856/a2cc46e7-c838-4ad4-8f6c-0868e7213a3d) , ![Setting up RAS2](https://github.com/Shresoc/Active-Directory-/assets/168186856/b8d1f44a-1aea-4567-8c7a-abf66019c3be)
  - Further Rounting the remote access setup: ![Routing and Remote access setup](https://github.com/Shresoc/Active-Directory-/assets/168186856/c3bd662d-0554-4576-9964-6d10314c6e26)
 
# Setup DHCP:

![DHCP Configured](https://github.com/Shresoc/Active-Directory-/assets/168186856/ad0cb305-4571-48b3-ba99-a14757a83453)

- Configure DHCP on the domain controller to assign IP addresses automatically to the internal network

- Setup the DHCP Server : ![Installing DHCP Server](https://github.com/Shresoc/Active-Directory-/assets/168186856/d398111f-302f-4e5a-bd46-4d9f1ab04bb7)
- Setup DHCP Scope: ![Setting up DHCP Scope ](https://github.com/Shresoc/Active-Directory-/assets/168186856/baea4686-c5fe-4ab2-a3f4-9f838dcfea1a)

# Script Creation of Users: 
- Write and execute a PowerShell script to automatically create a thousand users in Active Directory.

![PowerShell Scripts for Creating Users](https://github.com/Shresoc/Active-Directory-/assets/168186856/368a4777-bc33-411d-8c6d-14373b7fdf26)

# Prepare Second Virtual Machine:
- Set up another virtual machine in VirtualBox for Windows 10. This VM will also connect to the private network.
  - Install Windows 10: Install Windows 10 on the second virtual machine.
  - Join Domain: Configure the Windows 10 VM to join the domain set up on the domain controller.
  - Final Configurations: Complete any final configurations and ensure both machines are communicating correctly over the network.
  - Test Connectivity: Test internet connectivity and network settings on both virtual machines to ensure they are configured correctly.
  - Create Organizational Units: Back in the domain controller, create organizational units in Active category to organize the users and computers within the domain.
  - Domain Administration: Create a domain admin account and demonstrate how to manage the domain.
  - Networking Services Setup: Install and configure additional networking services like NAT and routing on the domain controller to allow the client VM network access to the internet.
  - Validate Network Configuration: Ensure that all network configurations, including DHCP and DNS settings, are working correctly and that the domain controller can manage traffic appropriately.
 
These steps summarize the entire setup process described, providing a structured way to understand and implement an Active Directory lab using VirtualBox.

# Validate User Creation:
- Use Active Directory Users and Computers on the domain controller to check that the users were created by the PowerShell script. Ensure that everything is populated correctly and that the organizational units are set up.

  ![User Creation with powershell](https://github.com/Shresoc/Active-Directory-/assets/168186856/2997f7da-f95c-47c4-a830-ca40a22827ad)

# Profile Setup and Login: 

Set up user profiles on the Windows 10 VM and log in using the credentials of the Active Directory users created by the PowerShell script to ensure they are functional.


![Users Added to rth](https://github.com/Shresoc/Active-Directory-/assets/168186856/9e375cc2-8d71-4b03-8ebe-ae41bdc19350)


These steps provide a comprehensive guide through the remainder of the setup and management of a virtual Active Directory lab, ensuring a robust understanding and practical skill set for managing and troubleshooting a networked environment using VirtualBox.







