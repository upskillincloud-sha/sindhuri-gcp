# Tags in GCP
Tags in Google Cloud Platform (GCP) are key-value pairs that can be attached to resources. They provide a way to organize, govern, and control access across your cloud environment. Unlike labels, tags are hierarchical and can be inherited across projects and folders.

## 🔑 Key Concepts

- Tag Key: Defines the category (e.g., env, team).

- Tag Value: Defines the specific value (e.g., prod, finance).

- Inheritance: Tags applied at the organization, folder, or project level automatically propagate to child resources.

- Central Management: Tags are managed as resources, making them reusable and consistent across environments.

### Use Cases

- Access Control: Apply IAM policies based on tags (e.g., restrict deletion of env=prod resources).

- Cost Allocation: Group resources by tags for billing reports (e.g., team=finance).

- Governance: Enforce compliance by tagging sensitive workloads (e.g., data=PII).

- Automation: Use tags in Terraform or scripts to dynamically manage resources.

### ⚙️ Best Practices

- Define a standardized taxonomy (e.g., env, team, project).

- Use tags for governance/IAM and labels for billing/metadata.

- Apply tags at higher levels (organization/folder) for consistency.

- Audit tags regularly to avoid unused or inconsistent values.

## Steps to Create Tags in GCP

1. Open console.cloud.google.com. In Project Picket select the required Project. 

2. Click on Navigational Menu. Go to IAM and Admin and Click on Tags.

<img width="1877" height="932" alt="image" src="https://github.com/user-attachments/assets/6448ea68-36d4-4f82-94e5-30745a51be8e" />

<img width="1913" height="913" alt="image" src="https://github.com/user-attachments/assets/dee4a6f9-8be1-4430-8c63-f0ab8810af2e" />

3. Click on "Create". Click on "Create tag Key". Tag is created.


<img width="1906" height="859" alt="image" src="https://github.com/user-attachments/assets/c72e9140-3b33-4e2a-8528-a0432538618a" />

<img width="1584" height="874" alt="image" src="https://github.com/user-attachments/assets/95f39c79-2a52-4f74-a6c7-83fc8e1cb182" />

<img width="1890" height="858" alt="image" src="https://github.com/user-attachments/assets/cebdce2f-29cb-4c9e-89e0-e501b48a3cb9" />

<img width="1907" height="878" alt="image" src="https://github.com/user-attachments/assets/e74836dd-ba20-49cd-a9c9-673cb023a023" />

<img width="1867" height="815" alt="image" src="https://github.com/user-attachments/assets/3022832b-9a18-488f-89e2-061189edd25b" />

# Labels in GCP

Labels in GCP are user-defined key-value metadata pairs that you attach directly to resources. They are lightweight and flexible, designed for organization, filtering, and cost tracking. Unlike tags, labels do not inherit across projects or folders.

## 🔑 Key Concepts

- Key: Defines the category (e.g., env, team, project).

- Value: Defines the specific value (e.g., prod, finance, alpha).

- Scope: Applied directly to resources; no hierarchical inheritance.

- Flexibility: Labels can be added, updated, or removed at any time.

### Use Cases

- Cost Tracking: Assign labels like cost-center=1234 to group billing data.

- Filtering: Quickly find resources by label in the console or CLI.

- Ownership: Add labels like owner=pavan to identify responsible teams.

- Automation: Use labels in Terraform or scripts to dynamically manage resources.

### ⚙️ Best Practices

- Define a consistent taxonomy (e.g., env, team, project).

- Limit the number of labels per resource to avoid clutter.

- Use labels for billing/metadata and tags for IAM/governance.

- Regularly audit labels to ensure accuracy.

## Steps to Create Labels

1. Open console.cloud.google.com. In Project Picket select the required Project. 

2. Click on Navigational Menu. Go to IAM and Admin and Click on Labels


<img width="1919" height="925" alt="image" src="https://github.com/user-attachments/assets/93038919-8ad7-47fc-b908-354a36e6ac2f" />

<img width="1907" height="862" alt="image" src="https://github.com/user-attachments/assets/05e86a2e-9ea0-406e-acad-e764c2f6fa81" />


3. Click on Add Label. Add labels which are required for the project.


<img width="1911" height="859" alt="image" src="https://github.com/user-attachments/assets/10489b5a-6a1a-4c23-9cfa-02841a5c4ff3" />


4. Click on Save.

<img width="1803" height="744" alt="image" src="https://github.com/user-attachments/assets/0d8a7ed6-4c5c-4b61-94f0-8c8f1bc3faef" />

