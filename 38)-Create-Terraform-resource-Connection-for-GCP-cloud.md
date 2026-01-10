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


