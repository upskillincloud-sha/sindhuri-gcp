# Steps to Create Bastion Server

1. Login to Console.Google.com

2. Click on Compute Engine. Click on VM instances.

<img width="1827" height="1018" alt="image" src="https://github.com/user-attachments/assets/cb31d15f-1f14-4395-b399-91e49614087e" />

3. Click on the Project in which we need to create VM( here Hub-ComputeAndStorage-Project). Click on the project.

<img width="1908" height="902" alt="image" src="https://github.com/user-attachments/assets/298b6e52-23c1-4d37-a0cb-0549f5ad3e65" />

4. Enable Compute Engine API.

<img width="1917" height="907" alt="image" src="https://github.com/user-attachments/assets/92c31624-c016-462d-9e77-b92da5206a58" />

<img width="1909" height="950" alt="image" src="https://github.com/user-attachments/assets/3c41e69c-9565-4d46-af6f-0036ab561beb" />

5.Hover on VPC Network, Click on VPC Networks. Delete Default VPC network. Click on the "default" vpc network and click on Delete VPC Network.

<img width="1616" height="1018" alt="image" src="https://github.com/user-attachments/assets/cbbff35f-1328-49a0-8666-db77e4da9f1b" />

<img width="1468" height="898" alt="image" src="https://github.com/user-attachments/assets/0901fe8e-4310-495c-9961-cd1c08e99a80" />

<img width="1742" height="896" alt="image" src="https://github.com/user-attachments/assets/6b4f13c4-b6c7-4a45-ad2c-8805c8fffd7d" />

<img width="1781" height="792" alt="image" src="https://github.com/user-attachments/assets/d266ec13-2514-4edf-b085-6378169a6828" />

6. Now again go to VM instances(repeat Step 2). 

7. Click on "Create instance". 

8. In Machine Configuration. Give Name of the instance, Select region, Zone.

<img width="1850" height="907" alt="image" src="https://github.com/user-attachments/assets/ac699b22-98c9-4049-b2f7-ac6022276220" />

<img width="1510" height="890" alt="image" src="https://github.com/user-attachments/assets/e64dd5c9-adb4-475b-91ee-42ebc8507572" />

9. Click on OS and Storage. Click on Change. Make required changes like changing the size. Click on Select.

<img width="1886" height="902" alt="image" src="https://github.com/user-attachments/assets/32cdd3a2-2485-40a1-a4c1-8ea2df48c5e8" />

10.Click on Data Protection. Click on Snapshot schedules.


<img width="1893" height="908" alt="image" src="https://github.com/user-attachments/assets/e10d7848-7fe0-435d-af74-a96c9620b317" />

11. Click on "Networking". As we have deleted the default VPC network in this project. There are no network to be selected.

<img width="1907" height="900" alt="image" src="https://github.com/user-attachments/assets/2f27302b-f7ee-4819-bed3-02497407de92" />

So Solved this issue we will do the process of Shared VPC networks.

### Steps to Create Shared VPC networks

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

[Lets continue back to the creation of Server. Now by using the shared VPC. Now as we have created a shared VPC. Attached that to this project(Hub-ComputeAndStorage-Project) we should see VPC in networking.](repeat 1 to 11 steps)

12. Click on Networking. In Network=hub-vpc, Sub-Network = hub-public-subnet

<img width="1908" height="899" alt="image" src="https://github.com/user-attachments/assets/84ae6683-a418-4802-a1e5-cd8c69f6de66" />

<img width="1831" height="872" alt="image" src="https://github.com/user-attachments/assets/6353b0c5-9aee-4990-9324-29eaa172148b" />

13. Click on Observerability. 

<img width="1831" height="872" alt="image" src="https://github.com/user-attachments/assets/d2a51923-b738-4256-8a45-9dbb6d1b8426" />

14. Click on Security.

<img width="1746" height="908" alt="image" src="https://github.com/user-attachments/assets/d074d925-b423-4b13-9f2c-18118708c372" />

15. Click on Advanced. Add labels and tags.

<img width="1770" height="909" alt="image" src="https://github.com/user-attachments/assets/36cdd98c-6a95-48af-8baf-c77a359b89af" />
<img width="1815" height="817" alt="image" src="https://github.com/user-attachments/assets/f6e537dc-2197-4fae-9bd9-ac5ce6b7770f" />

16. Click on Create.

<img width="1902" height="906" alt="image" src="https://github.com/user-attachments/assets/66d34f11-f32e-44ba-bd4d-3c98f2813a14" />

17. Click on dropdown in connect. Click on open in browser.

<img width="1852" height="911" alt="image" src="https://github.com/user-attachments/assets/c832bbeb-9ba3-41f7-8c01-13999aade708" />

18. Click on Authorize. Authorize your login.

<img width="1086" height="872" alt="image" src="https://github.com/user-attachments/assets/03da12cc-2df9-4a4b-a6ed-e9a667985c5b" />

<img width="1113" height="896" alt="image" src="https://github.com/user-attachments/assets/dc528bee-a4a9-43e8-aa75-ad6b71f5c88b" />
