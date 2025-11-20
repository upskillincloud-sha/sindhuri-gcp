# Organization, Folder, Projects
In Google Cloud Platform (GCP), the Organization, Folders, and Projects create a resource hierarchy for managing cloud resources, with Organization at the top for a company, Folders used to group projects by department or environment, and Projects as the container for all GCP services and resources. This structure enables centralized control and policy inheritance, where rules set at a higher level are automatically applied to lower levels. 
## Organization
**Purpose:** Represents your company or a Google Cloud domain. It's the root node of the resource hierarchy.
**Function:**
* Owns all projects created within it.
* Centralizes management and visibility of all cloud resources.
* Allows for organization-wide policies and roles to be defined. 

<img width="1605" height="993" alt="image" src="https://github.com/user-attachments/assets/c036495c-5232-400c-a665-20e164a19721" />

## Folders
**Purpose:** Group related projects together. They provide an additional layer of organization within the hierarchy.
**Function:**
* Can be used to create boundaries for different teams, departments, or environments (e.g., Production, Staging, Development).
* Allows you to delegate administrative control of specific sets of projects to different teams by assigning the Folder Admin role.
* Can contain other folders or projects. 

## Steps to create a Folder
1. Click on Navigational menu/Burger menu.
<img width="1906" height="1025" alt="image" src="https://github.com/user-attachments/assets/805f223d-4e25-4a25-b620-d4067e63f967" />
<img width="1867" height="978" alt="image" src="https://github.com/user-attachments/assets/54580eb0-290b-4d8f-a335-2ed928b9aa34" />


2. Hover/Click on "IAM and admin".
<img width="1903" height="963" alt="image" src="https://github.com/user-attachments/assets/586e7dbb-341c-40cf-876d-a65436140741" />\

3.Click on Manage resources.
<img width="1903" height="963" alt="image" src="https://github.com/user-attachments/assets/c4577e2d-4651-4a9a-94d4-f2452ee5e521" />

<img width="1910" height="915" alt="image" src="https://github.com/user-attachments/assets/29a15fd1-b1b2-4bfc-94e3-6824da11eb90" />

4.Click on "Create Folder" dropdown. click on "Folder".

<img width="1807" height="951" alt="image" src="https://github.com/user-attachments/assets/5b97d168-c700-42b5-be2f-e0ec175d4ac3" />

<img width="1913" height="965" alt="image" src="https://github.com/user-attachments/assets/c02d2a20-7304-4da8-8bb8-f33110c4c4b9" />

5. Now new folder creation page will be displayed. Now fill the details

<img width="1911" height="859" alt="image" src="https://github.com/user-attachments/assets/60e24d3d-206d-43cc-b345-c9c81aa19791" />
6. Click on "create".
<img width="1911" height="859" alt="image" src="https://github.com/user-attachments/assets/564fab6b-aeb5-4f56-a1b1-aa3a1e6b5297" />

<img width="1913" height="976" alt="image" src="https://github.com/user-attachments/assets/0bec7898-8e38-46ab-b0a3-45a087fcc439" />


## Projects
**Purpose:** The fundamental container for your cloud resources, where you use and manage GCP services.
**Function:**
* Holds all resources like virtual machines, databases, and storage buckets.
* Is the level at which you manage IAM permissions for individual resources.
* Billing is also managed at the project level.
* Can be created inside folders or directly under an organization.

## Steps to Create to Project
1. Click on Navigational menu/Burger menu.
<img width="1906" height="1025" alt="image" src="https://github.com/user-attachments/assets/805f223d-4e25-4a25-b620-d4067e63f967" />
<img width="1867" height="978" alt="image" src="https://github.com/user-attachments/assets/54580eb0-290b-4d8f-a335-2ed928b9aa34" />


2. Hover/Click on "IAM and admin".
<img width="1903" height="963" alt="image" src="https://github.com/user-attachments/assets/586e7dbb-341c-40cf-876d-a65436140741" />\

3.Click on Manage resources.
<img width="1903" height="963" alt="image" src="https://github.com/user-attachments/assets/c4577e2d-4651-4a9a-94d4-f2452ee5e521" />

<img width="1910" height="915" alt="image" src="https://github.com/user-attachments/assets/29a15fd1-b1b2-4bfc-94e3-6824da11eb90" />

4.Click on "Create Project" dropdown. click on "Project".

<img width="1917" height="967" alt="image" src="https://github.com/user-attachments/assets/0aa043b5-dffb-450a-aa36-dec0e01ebc1f" />

<img width="1855" height="868" alt="image" src="https://github.com/user-attachments/assets/228ac1f0-8150-4b9f-b1a7-1f01f1fa1ec7" />

5. Click on "create".

<img width="1890" height="892" alt="image" src="https://github.com/user-attachments/assets/f7d8a267-3ecb-4a1d-9256-46befe0895e4" />

<img width="1891" height="797" alt="image" src="https://github.com/user-attachments/assets/9c256d5d-72aa-440a-bbcc-aa1b6ef26897" />


