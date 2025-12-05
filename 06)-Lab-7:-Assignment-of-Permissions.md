# Permissions in Google Cloud Platform (GCP)

## 🔑 Overview

Permissions in GCP are managed through **Identity and Access Management (IAM)**.  

IAM lets you control **who (principal)** has **what access (role/permission)** to **which resource**.

---

## 👤 Principals

Principals are identities that can be granted access:

- **Users**: Individual Google accounts (e.g., Gmail or Workspace accounts).

- **Groups**: Collections of users managed together.

- **Service Accounts**: Non-human identities used by applications/services.

- **Cloud Identity Domains**: Organizational accounts that manage users and groups.

---

## 🎭 Roles

Permissions are bundled into **roles**. Roles are assigned to principals at different levels (organization, folder, project, resource).

### Types of Roles

- **Primitive Roles** (legacy):

  - `roles/owner` → Full control, including IAM.

  - `roles/editor` → Read/write access to most resources.

  - `roles/viewer` → Read-only access.

- **Predefined Roles**:

  - Fine-grained roles created by Google (e.g., `roles/storage.objectViewer`, `roles/compute.admin`).

- **Custom Roles**:

  - User-defined roles with a specific set of permissions.

---

## 📋 Permissions

Permissions are the **lowest-level building blocks** in IAM.  

Each permission allows a specific action on a resource (e.g., `compute.instances.start`).

- Permissions are **not assigned directly** to users.

- Instead, they are **granted through roles**.

- Example:

  - Permission: `storage.buckets.create`

  - Role: `roles/storage.admin` (includes the permission)

  - Principal: User or group assigned the role

---

## 🏛 Resource Hierarchy

Permissions flow down the resource hierarchy:

1. **Organization**

2. **Folder**

3. **Project**

4. **Resource**

Roles granted at a higher level are **inherited** by lower levels.

---

## ⚙️ Best Practices

- Use **least privilege**: assign only the roles needed.

- Prefer **predefined roles** over primitive roles.

- Assign roles to **groups** instead of individuals for easier management.

- Regularly **audit IAM policies** to ensure compliance.

- Use **custom roles** only when predefined roles don’t meet requirements.

---
## 👣 Steps in the Cloud Console

1. **Log in** to the [Google Cloud Console](https://console.cloud.google.com).


<img width="1910" height="977" alt="image" src="https://github.com/user-attachments/assets/96b23ba2-62ec-479c-ae5a-bf639d27f724" />


2. Navigate to **IAM & Admin > IAM**.

<img width="1902" height="909" alt="image" src="https://github.com/user-attachments/assets/ae80fac4-30f8-4ea9-8f38-0b7cffdef3f9" />

3. Select the **resource level** where you want to grant access:

   - Organization: For organization level, select organization in Open Project picker dropdown.
 
<img width="1918" height="916" alt="image" src="https://github.com/user-attachments/assets/84d0ee82-772e-4906-b040-c603b7bcc13b" />


   - Folder: For Folder level, click on the Open Project picker. Now Resource selector Ui will appear. From that select the folder you need to give permissions.


<img width="1903" height="805" alt="image" src="https://github.com/user-attachments/assets/5c351c5e-94d8-4bb6-86a4-d67c63f758b4" />


   - Project: For Project level, click on the Open Project picker. Now Resource selector Ui will appear. From that select the Project you need to give permissions.

<img width="1902" height="809" alt="image" src="https://github.com/user-attachments/assets/8e838e84-101c-4f9d-9319-ab86fbc0af47" />


   - Specific resource (e.g., Storage bucket, Compute instance)


4. Click **+ Grant Access**. (In this eg. Granting a group permission on Organization level)

<img width="1906" height="811" alt="image" src="https://github.com/user-attachments/assets/039b4d77-1caa-4845-b14b-a91a093f24d8" />


5. Enter the **principal’s email address**:

   - User (Google account)

   - Group (Google Group email)

   - Service account

<img width="1879" height="963" alt="image" src="https://github.com/user-attachments/assets/63d93d31-5323-4dd2-bbb1-936f4672b84e" />

6. Choose the **role(s)** to assign:

   - Predefined roles (e.g., `roles/storage.objectViewer`)

   - Primitive roles (`Viewer`, `Editor`, `Owner`)

   - Custom roles (if created)

<img width="1889" height="902" alt="image" src="https://github.com/user-attachments/assets/a55c8f3f-d19e-452d-9d32-46055615cf24" />

7. Click **Save**.  

   → The principal now has the assigned permissions.

<img width="1913" height="973" alt="image" src="https://github.com/user-attachments/assets/5233c2eb-d4b8-4223-a421-ef56bb368eb2" />

8. Folder level access eg:

<img width="1915" height="935" alt="image" src="https://github.com/user-attachments/assets/fb1a31d8-6fbf-4b08-948f-5270c608ebf5" />
<img width="1897" height="910" alt="image" src="https://github.com/user-attachments/assets/1d3b9a88-3aea-411f-bea4-77248bc2dced" />

9. Project Level Access:(eg)

<img width="1908" height="1022" alt="image" src="https://github.com/user-attachments/assets/9e838351-df7f-4826-9ab1-30e81e25cda4" />
<img width="1007" height="905" alt="image" src="https://github.com/user-attachments/assets/1786710b-5cd2-4059-86ce-335477e37c1c" />
<img width="1903" height="911" alt="image" src="https://github.com/user-attachments/assets/67c472a0-f7f6-4e6d-91e4-4691df2f0a65" />


## ✅ Summary

- **Permissions** = specific actions (e.g., `compute.instances.start`).

- **Roles** = bundles of permissions (e.g., `roles/compute.admin`).

- **Principals** = identities (users, groups, service accounts).

- Permissions are always granted **via roles**, never directly.

- Roles can be applied at **organization, folder, project, or resource** level, and are inherited down the hierarchy.