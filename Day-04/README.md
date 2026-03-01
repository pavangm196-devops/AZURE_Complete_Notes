#  **Azure Virtual Machines & Jenkins Deployment**




**Topics Covered:** Virtualization, Azure VM Types, VMSS (Autoscaling), and Jenkins Setup.



**1. Understanding Virtualization**
Virtualization is the fundamental technology that powers Cloud Computing. It allows a single physical machine to act as multiple **"virtual"** machines.

**Hypervisor:** The software layer (like Hyper-V or VMware) that sits on the physical hardware to create and run VMs.

**Azure's Role:** Microsoft manages the hardware and hypervisor; you simply request the VM via the Azure Portal or CLI.




  **2. Azure Virtual Machine (VM) Types**
Azure offers different VM "families" optimized for specific workloads:
| VM Family | Best For |
| :--- | :--- |
| General Purpose (B, D series) | Testing, small databases, web servers. |
| Compute Optimized (F series) | Batch processing, high-traffic web servers. |
| Memory Optimized (E, M series) | Relational databases, in-memory caches (e.g., Redis). |
| GPU (N series) | Graphic rendering, Video editing, Deep Learning. |





## ***Series,Type,Best For,Real-World Example***

**B-Series,Bursting,"Low-cost, testing, and learning.",Personal lab or small dev projects.**

**D-Series,General Purpose,Balanced CPU and Memory.,Enterprise web servers.**

**F-Series,Compute Optimized,High CPU power.,Batch processing and gaming servers.**

**E/M-Series,Memory Optimized,High RAM capacity.,In-memory databases like Redis.**

**L-Series,Storage Optimized,High Disk I/O.,NoSQL databases (MongoDB/Cassandra).**

**N-Series,GPU Enabled,Graphics and Compute.,"Machine Learning, AI, and Video Editing."**







**3. Azure Virtual Machine Scale Sets (VMSS)**
VMSS allows you to create and manage a group of load-balanced VMs.

**High Availability:** Automatically distributes VMs across Availability Zones.

**Autoscaling:** Increases or decreases the number of VM instances based on demand (CPU usage, memory, or a schedule).

**Cost Efficiency:** You only pay for the VMs that are currently running.


**4. Hands-on:** Deploying Jenkins on Azure VM
Prerequisites
An active Azure Subscription.

A Linux VM (Ubuntu 22.04 LTS recommended).

Ports 8080 (Jenkins) and 22 (SSH) opened in the Network Security Group (NSG).

Steps to Install Jenkins
Accessing Jenkins
Copy your VM's Public IP address.

Open a browser and go to http://<your-public-ip>:8080.

Retrieve the initial admin password:

**5. Key Takeaways**
**IaaS:** Virtual Machines are a core Infrastructure-as-a-Service offering.

**Security:** Always use SSH keys instead of passwords for VM access.

**Automation:** Use VMSS for production workloads to handle traffic spikes automatically.




## **Jenkins Deployment on Azure**
This section provides a step-by-step guide on how to use the provided automation script to set up Jenkins on an Azure VM.

**1. Prerequisites**

**Azure Account:** You need an active Azure subscription.

 **Azure VM:** Create a Virtual Machine (Ubuntu 22.04 LTS recommended).

**Network Security Group (NSG):** * Ensure Port 22 is open for SSH access.

Ensure Port 8080 is open for Jenkins web access.

**2. Connect to your VM**
Open your terminal and SSH into your Azure VM:

**3. Clone and Execute the Script**
Once inside the VM, run the following commands to download and run the automation script:

**4. Post-Installation Steps**
After the script completes, follow these steps to finish the setup:

**Get the IP:** Copy the Public IP of your Azure VM.

**Access Jenkins:** Open your browser and navigate to http://<your-vm-public-ip>:8080.

**Unlock Jenkins:** The script will print your Initial Admin Password at the end. If you missed it, run:

**Install Plugins:** Select "Install suggested plugins" and create your first Admin User.



### ***💡 Troubleshooting Tip***

If you cannot access the Jenkins UI at port 8080, double-check your Inbound Port Rules in the Azure Portal:

Source: Any

Source port ranges: *

Destination: Any

Service: Custom

Port ranges: 8080

Protocol: TCP

Action: Allow



