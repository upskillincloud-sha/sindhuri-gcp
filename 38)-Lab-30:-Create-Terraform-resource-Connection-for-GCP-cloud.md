## Creating Terraform.tf file
1. Create a new file gcp-terraform.tf
2. Search for terraform.tf code for GCP. Copy and paste in the gcp-terrqaform.tf file.
<img width="1483" height="832" alt="image" src="https://github.com/user-attachments/assets/384d0bb3-7e7e-437e-8e7b-d9607a0223ca" />

## Create Provider.tf file
1. Create a Provider.tf file. 
2. Search for provider.tf code for GCP. Copy and paste it in provider.tf file.

<img width="1284" height="768" alt="image" src="https://github.com/user-attachments/assets/ca8f8471-94f9-4313-b642-194d560f5999" />

3. In the above code. For project, give a existing project name in GCP(this project should have billing enabled)

<img width="1688" height="851" alt="image" src="https://github.com/user-attachments/assets/dde040be-df95-4f85-80cb-700a48433122" />


### Creating SA user in GCP:
1. Open Console.google.com.

2. Click on Navigational Menu. Hover on IAM and Admin. Click on Service Accounts

<img width="1760" height="993" alt="image" src="https://github.com/user-attachments/assets/43cb8732-9a11-46a8-83a6-66c74014c4cc" />

<img width="1919" height="926" alt="image" src="https://github.com/user-attachments/assets/375bfc5a-b704-45e3-83db-96999924bddd" />

3. Now Select the project which is given in provider.tf file

<img width="1891" height="377" alt="image" src="https://github.com/user-attachments/assets/0918989d-5f66-4c7a-82b5-b0322d5c21ad" />

4. click on create Service account.

<img width="1308" height="790" alt="image" src="https://github.com/user-attachments/assets/4eb5ceb8-c89d-4cde-97d6-b445a6b59511" />

5. Provide name and click on create and continue. 

<img width="1918" height="813" alt="image" src="https://github.com/user-attachments/assets/0d63ea93-efdd-4ac9-9d7a-39d8d37e17d0" />

6. Search for the role and click on continue. Then Click on Done.

<img width="1541" height="726" alt="image" src="https://github.com/user-attachments/assets/533893b1-040c-4bfe-b2db-9b635f15e90f" />
<img width="1916" height="803" alt="image" src="https://github.com/user-attachments/assets/917eb25e-4cbd-4b84-a0a4-891a6c778800" />
<img width="1852" height="763" alt="image" src="https://github.com/user-attachments/assets/fd3ab3bf-1b83-40d6-ad24-87a25cb1cba7" />
7. Click on the user and go to key section.

<img width="1694" height="784" alt="image" src="https://github.com/user-attachments/assets/f0c66914-5938-4b75-b811-18ca811b6910" />
<img width="1861" height="829" alt="image" src="https://github.com/user-attachments/assets/1c5cebd8-c0f4-4de4-bff6-2e90116ec978" />


8. click on Add Key. Click on Create new Key. Select json. Click on create.

<img width="1324" height="738" alt="image" src="https://github.com/user-attachments/assets/f9a7554e-5b80-46e8-af60-a8d57a8c18f1" />

<img width="1629" height="771" alt="image" src="https://github.com/user-attachments/assets/ccccd62c-45b2-47bc-8bc1-f1fc012fa30e" />

<img width="1902" height="984" alt="image" src="https://github.com/user-attachments/assets/1e23fd42-ab41-4460-8a49-b129cf7b333c" />

9. Now save the above json in s folder and give the path of key in the provider.tf as credentials.

<img width="1644" height="798" alt="image" src="https://github.com/user-attachments/assets/951c5aa2-a5ed-4e1d-b176-e70db8373ab0" />

10. Now we need to give access to the sa user which we have created earlier to create folder and project.

11. Click on Navigational Menu. Click on view products. click on API and services. Click on Library.

<img width="1792" height="1022" alt="image" src="https://github.com/user-attachments/assets/6a7ec9e5-0bbb-4888-ab33-17920cbdc1e8" />

<img width="1686" height="985" alt="image" src="https://github.com/user-attachments/assets/bb68ccb5-f43d-4ad2-bdf7-71dd9f79e516" />

<img width="1902" height="1002" alt="image" src="https://github.com/user-attachments/assets/b4ceab20-e155-4fda-9033-8e2138184245" />

12. In Search bar, search cloud resource manager api. click on cloud resource manager api. click on enable.

<img width="1897" height="913" alt="image" src="https://github.com/user-attachments/assets/c09c0d1b-53d8-4cf8-a8ed-3a254d5b201c" />

<img width="1905" height="900" alt="image" src="https://github.com/user-attachments/assets/48b34205-0dff-4925-a498-8e362b9afdb3" />

<img width="1896" height="900" alt="image" src="https://github.com/user-attachments/assets/20594730-94dd-4cc9-b30a-8a4254bbcc17" />

<img width="1867" height="872" alt="image" src="https://github.com/user-attachments/assets/be6bfd1a-26b3-464a-830a-09c36bcca61c" />

13. Now we need to give the sa user roles at orginational level to create resources, projects.

14. Select organization in project picker.

<img width="1907" height="951" alt="image" src="https://github.com/user-attachments/assets/745e9a56-2b25-49d0-83be-5a31cb3f8fac" />

15.Click on Navigational Menu. CLick on IAM & Admin. click on IAM. click on grant access. Give the sauser email. give the appropriate role. click on Save.

<img width="1873" height="951" alt="image" src="https://github.com/user-attachments/assets/68fec89f-cfaf-4592-a66e-a33f738e4a30" />

<img width="1905" height="958" alt="image" src="https://github.com/user-attachments/assets/b56f3978-79cc-4a03-aa3f-f500235ed141" />



 