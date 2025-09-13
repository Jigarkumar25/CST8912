## LAB 1 (pate1595)
# Lab Instructions: Provisioning and Managing an Azure Virtual Machine

### Task 1: Create a Virtual Machine

1.	Sign in to the Azure Portal
2.	In the search bar, type Virtual Machines and select Virtual Machines from the results.
3.	Click + Create → Azure Virtual Machine.
4.	Under Basics:

Subscription: Select your subscription.

Resource Group: Create a new resource group or use an existing one.

Virtual Machine Name: Enter a unique VM name.

Region: Select Canada Central.

Image: From the Marketplace, choose Ubuntu Server 18.04 LTS.

Size: Select Standard_B1s (1 vCPU, 1 GiB memory).

Authentication type: Choose SSH public key and provide your key.

![alt text](lab1%20photos/Screenshot%202025-09-11%20173453.png)


---
### Task 2: Configure Disks

In the Disks tab, select Premium SSD as the OS disk type.

![alt text](lab1%20photos/Screenshot%202025-09-11%20173717.png)

--- 
### Task 3: Configure Networking

In the Networking tab, create a new Virtual Network (leave default settings).

Keep default subnet, public IP, and NIC settings.

![alt text](lab1%20photos/Screenshot%202025-09-11%20173453.png)

---

### Task 4: Review Additional Settings

Leave default options for Management, Advanced, and Tags tabs.

Click Review + Create and then Create to deploy the VM.

![alt text](lab1%20photos/Screenshot%202025-09-11%20174533.png)


---
### Task 5: Perform Basic VM Operations

Once the VM is deployed, go to Virtual Machines in the portal.

Select your VM and perform the following actions:

Start

Stop

Restart

Delete (optional, end of lab)

![alt text](lab1%20photos/Screenshot%202025-09-11%20175526.png)

---
### Task 6: Create a Log Analytics Workspace

In the Azure portal, search for Log Analytics Workspaces.

Click + Create.

Under Basics:

Resource Group: Use the same one as your VM.

Region: Select Canada Central (must match VM region).

Enter a workspace name.

Click Review + Create, then Create.

![alt text](lab1%20photos/Screenshot%202025-09-11%20180030.png)

---
### Task 7: Connect VM to Log Analytics

Navigate to your Virtual Machine in the Azure portal.

In the left-hand menu, under Monitoring, select Insights or Logs.

Choose Enable monitoring and select the Log Analytics workspace you just created.

Wait for the monitoring solution to be provisioned.

![alt text](lab1%20photos/Screenshot%202025-09-11%20180957.png)

---
### Task 8 SSH into the VM
- Add a task where users must connect to the VM using SSH:
- Verify the VM is reachable.

![alt text](lab1%20photos/Screenshot%202025-09-11%20184344.png)


- Run basic commands (uname -a, top, df -h) to check system health.

![alt text](lab1%20photos/Screenshot%202025-09-11%20184351.png)  
![alt text](lab1%20photos/Screenshot%202025-09-11%20184400.png)  
![alt text](lab1%20photos/Screenshot%202025-09-11%20184409.png)  


- create a new file or folder as a test.

![alt text](lab1%20photos/Screenshot%202025-09-11%20184416.png)

---
### Task 9. Delete all the resources – clean and delete resources 
 I deleted all

