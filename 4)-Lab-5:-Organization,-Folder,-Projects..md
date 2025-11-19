# Organization, Folder, Projects
In Google Cloud Platform (GCP), the Organization, Folders, and Projects create a resource hierarchy for managing cloud resources, with Organization at the top for a company, Folders used to group projects by department or environment, and Projects as the container for all GCP services and resources. This structure enables centralized control and policy inheritance, where rules set at a higher level are automatically applied to lower levels. 
## Organization
**Purpose:** Represents your company or a Google Cloud domain. It's the root node of the resource hierarchy.
**Function:**
* Owns all projects created within it.
* Centralizes management and visibility of all cloud resources.
* Allows for organization-wide policies and roles to be defined. 
## Folders
**Purpose:** Group related projects together. They provide an additional layer of organization within the hierarchy.
**Function:**
* Can be used to create boundaries for different teams, departments, or environments (e.g., Production, Staging, Development).
* Allows you to delegate administrative control of specific sets of projects to different teams by assigning the Folder Admin role.
* Can contain other folders or projects. 
## Projects
**Purpose:** The fundamental container for your cloud resources, where you use and manage GCP services.
**Function:**
* Holds all resources like virtual machines, databases, and storage buckets.
* Is the level at which you manage IAM permissions for individual resources.
* Billing is also managed at the project level.
* Can be created inside folders or directly under an organization.