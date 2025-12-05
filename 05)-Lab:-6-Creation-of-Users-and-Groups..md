# Users and Groups in Google Cloud Platform (GCP)

## 👤 Users
- **Definition**: Individual identities that access GCP resources.

- **Types**:

  - **Human users**: People logging in with Google accounts (Gmail or Google Workspace).

  - **Service accounts**: Non-human identities used by applications or services.

- **IAM Role Assignment**: Permissions are granted to users through IAM roles (e.g., Viewer, Editor, Owner).

- **Example**: Assigning `roles/storage.objectViewer` to a user allows them to read objects in a Cloud Storage bucket.

### Steps to create Users in GCP

1. Go to admin.google.com

<img width="1883" height="929" alt="image" src="https://github.com/user-attachments/assets/c7896779-ad7e-436a-aa5e-3b82d3d5550b" />

2. Click on "Add a user"

<img width="1916" height="922" alt="image" src="https://github.com/user-attachments/assets/710b46d4-e8cd-48c8-af39-1365b11a192a" />


 or click on directory and click on user.


<img width="1916" height="970" alt="image" src="https://github.com/user-attachments/assets/a4032230-bffc-4022-bebd-9e8ee2c0fac5" />

<img width="1916" height="970" alt="image" src="https://github.com/user-attachments/assets/af9a4955-8174-48bb-8c34-63d0dfc9ce8d" />


3.Enter first name, surname, emailaddress and click on "Continue".


<img width="1876" height="872" alt="image" src="https://github.com/user-attachments/assets/02e25dfe-63fd-4544-98a0-9af529af34db" />

<img width="1918" height="887" alt="image" src="https://github.com/user-attachments/assets/5f35b9c2-441c-4ad2-bcf6-8a9c4a8d33c6" />

<img width="1918" height="923" alt="image" src="https://github.com/user-attachments/assets/f138a320-e23d-4d59-b1dd-87af490bd72e" />

---

## 👥 Groups

- **Definition**: Collections of users and/or service accounts managed as a single entity.

- **Purpose**:

  - Simplify access management by assigning IAM roles to the group instead of each user.

  - Ensure consistent policy enforcement across multiple users.

- **Management**: Groups are created and managed in **Google Cloud Identity** or **Google Workspace Admin Console**.

- **Benefits**:

  - Centralized management: One role assignment applies to all group members.

  - Scalability: Easily add/remove users without changing IAM policies.

  - Security: Apply uniform policies across teams.

- **Example**: A group called *“DevOps Team”* can be granted `roles/compute.admin` so all members can manage Compute Engine resources.

### Steps to create Groups

1. Open admin.google.com

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/f76f5212-e655-4dce-9b03-63960edfbc36" />

2. Click on "Directory". click on "Groups"

<img width="1880" height="960" alt="image" src="https://github.com/user-attachments/assets/a4785ba8-a1d2-41bc-8404-098da421fef1" />
<img width="1911" height="1005" alt="image" src="https://github.com/user-attachments/assets/0657a5a8-b437-4303-862c-1d508d61c18f" />

3. Now click on "Create Group".


<img width="1911" height="1005" alt="image" src="https://github.com/user-attachments/assets/2e080b74-4edb-4368-a4ef-005ee4f111a3" />


4. Create group page is opened. Now fill the details, group name, group emaildescription


<img width="1911" height="1005" alt="image" src="https://github.com/user-attachments/assets/f1998e73-cdaf-4994-baa3-92a457d73e0c" />

<img width="1781" height="944" alt="image" src="https://github.com/user-attachments/assets/7aec2a13-9ad5-49fa-a860-7f74f09642a2" />

5. Click on "Next". 

<img width="1897" height="962" alt="image" src="https://github.com/user-attachments/assets/2552d0f2-4419-471c-bec2-ff9d222897c6" />

6. Click on Team, click on only invited users.

<img width="753" height="745" alt="image" src="https://github.com/user-attachments/assets/0b149281-1cbe-4258-b43d-5dd8835f68b2" />

7.click on "Create Group" button.

<img width="1899" height="955" alt="image" src="https://github.com/user-attachments/assets/992f854a-f01f-4680-87cd-db05ced9d8fc" />

#### Steps to add members in Group

1. 1. Open admin.google.com

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/f76f5212-e655-4dce-9b03-63960edfbc36" />

2. Click on "Directory". click on "Groups"

<img width="1880" height="960" alt="image" src="https://github.com/user-attachments/assets/a4785ba8-a1d2-41bc-8404-098da421fef1" />
<img width="1883" height="1004" alt="image" src="https://github.com/user-attachments/assets/ebc06249-68e1-4ec3-a40a-0d5a8430061a" />

3. Click on the Group you want to add members.

<img width="1919" height="965" alt="image" src="https://github.com/user-attachments/assets/4c45ff8c-d1ae-4068-8909-e1d3f3f3ad4d" />

4. Click on "Add Members".

<img width="1918" height="965" alt="image" src="https://github.com/user-attachments/assets/d770272f-7eca-44fe-925c-4bad35d963f9" />

5. Search for users and select them.

<img width="1830" height="958" alt="image" src="https://github.com/user-attachments/assets/42b919d6-a100-4798-bea1-80d1986e7647" />

6. Click on "Add to Group"

<img width="1894" height="977" alt="image" src="https://github.com/user-attachments/assets/8f8166be-0cc4-4106-b8ab-c210b5acd422" />

<img width="1896" height="897" alt="image" src="https://github.com/user-attachments/assets/5a62b752-9afc-4eb8-9805-9796430eab7f" />

7. To view the members in group. Click on Direct Members.

<img width="1882" height="940" alt="image" src="https://github.com/user-attachments/assets/301c2c07-905f-4e00-84fb-cdeeb8c0e406" />

<img width="1901" height="912" alt="image" src="https://github.com/user-attachments/assets/59ef742a-045a-4182-b3fc-8e9c705eafb7" />

---

## 📋 Key Differences

| Aspect        | Users | Groups |
|---------------|-------|--------|
| Identity type | Individual (human or service account) | Collection of users/service accounts |
| Management    | Google accounts or service accounts | Cloud Identity / Workspace Admin |
| IAM usage     | Roles assigned directly to user | Roles assigned to group, inherited by members |
| Best for      | Specific permissions | Team-based or role-based permissions |

---

## ✅ Summary

- **Users** = individual identities (people or service accounts).

- **Groups** = collections of users, used to manage permissions collectively.

- Both are IAM *principals* that can be granted roles to access resources.