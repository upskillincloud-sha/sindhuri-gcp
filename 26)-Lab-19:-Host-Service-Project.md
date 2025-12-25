# Shared VPC
In Google Cloud (GCP), a Host Project and Service Project setup, known as Shared VPC, allows multiple projects (service projects) to use a common network (VPC) defined in the host project, centralizing network management for better security and IP control, while teams manage their applications in separate service projects. The host project owns the shared network and subnets, and service projects attach to it to consume IPs from those subnets for resources like VMs, enabling secure communication within the shared network. 

Host Project: The "Owner" of the network. It contains the Shared VPC networks, subnets, firewall rules, and hybrid connectivity (like Cloud VPN or Interconnect).

Service Project: The "Consumer" of the network. These projects are attached to the Host Project. They do not have their own VPCs; instead, they spin up resources (like VM instances or GKE clusters) that "plug into" the subnets provided by the Host Project.

* Select/Create a Host Project: Enable the Shared VPC item in the Networking menu.

* Attach Service Projects: Link your application projects to this Host.

* Share Subnets: Choose which subnets from the Host project are visible to which Service projects.

* Deploy Resources: In the Service Project, when creating a VM, select the "Shared VPC".

### Steps to Create Shared VPC networks( Host project: Hub-Network-project; Service Project: Hub-ComputeAndStorage-Project)

1. In Project Picker, Select Hub-Network-project(we have created a VPC in this project already).

2. Click on Burger Menu. Hover on VPC Network. Click on VPC Networks. 

<img width="1609" height="890" alt="image" src="https://github.com/user-attachments/assets/f4fc41bc-3907-4425-8849-d61c47c4811c" />

3. Click on "Shared VPC". Click on "Set uo Shared VPC".

<img width="1761" height="852" alt="image" src="https://github.com/user-attachments/assets/36c5ef59-2131-4816-ae28-17b9c63fdf43" />

4. Click on "Enable and Continue" button.( I alread have access to shared VPC. If you dont have access. Give in organizational level, give compute Shared VPC Admin(roles/compute.xpnAdmin) role.

<img width="1874" height="852" alt="image" src="https://github.com/user-attachments/assets/f6cd578a-8311-4672-a326-0bd9959a5ddb" />

5. Click on "Continue". In Grant access, Click on individual subnets. Click on Save.

<img width="1915" height="906" alt="image" src="https://github.com/user-attachments/assets/907eb9b7-c2ca-4aa3-87ce-003330d782ad" />

<img width="1902" height="901" alt="image" src="https://github.com/user-attachments/assets/c913b750-adbc-4897-b7f1-c0bbc300b2e2" />

