# Lab 2 <br> Subject: Cloud Solution Architecture  <br> Name: Jigarkumar Dilipkumar Patel <br> Id: pate1595


## Resource Group creation
![alt text](lab2 photos/1.png)

## Virtual Networks
1) VNet0
 ![alt text](lab2 photos/2.png)
2) VNet1
 ![alt text](lab2 photos/4.png)
3)VNet2
 ![alt text](lab2 photos/6.png)


## Peering configuration 
1) VNet0
![alt text](lab2 photos/3.png)
2) VNet1
![alt text](lab2 photos/5.png) 
3)VNet2
![alt text](lab2 photos/7.png) 



## VM deployments
1) VMm0
![alt text](lab2 photos/8.png)
2) VM1
![alt text](lab2 photos/9.png)
3) VM2
![alt text](lab2 photos/10.png)


## PowerShell Test-NetConnection results
1) VM0 -> VM1 & VM0 --> VM2
![alt text](lab2 photos/11.png)

2) VM1 -> VM2
![alt text](lab2 photos/12.png)

## Findings & Analysis

1. Why VNet peering is important?<br>
VNet peering is essential because it enables smooth communication across virtual networks using private IP addresses that are located in different or adjacent areas. Internet-based routing and VPN gateways are no longer required as a result. Peering makes it easier to connect, lowers latency, and ensures safe communication between resources like virtual machines, databases, and applications by making the VNets act as though they were a single network.

2. How private IP communication was established? <br>
Private IP communication was enabled through the VNet peering connections configured in the lab. Each VM was deployed into a different VNet with unique, non-overlapping IP address spaces. Once peering was established, the Azure backbone automatically routed traffic between these VNets without traversing the public internet. The PowerShell Test-NetConnection command verified successful connectivity between VM0, VM1, and VM2 over their private IP addresses, confirming that the traffic stayed internal to the Azure network.

3. Benefits of global peering (performance & security)?<br>
Global VNet peering provides cross-region connectivity without requiring public IPs or traffic to leave the CSP’s private backbone. The benefits are:

- Performance: Traffic flows through Microsoft’s high-speed, low-latency private backbone, ensuring reliable and efficient communication across regions.

- Security: Data never traverses the public internet, reducing exposure to threats such as man-in-the-middle attacks. This improves compliance with organizational security standards.


- Resiliency: Global peering supports redundant communication paths between regions, enhancing business continuity and disaster recovery strategies.
