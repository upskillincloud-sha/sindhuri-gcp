# Google Private Access

Private Google Access (PGA) is a Google Cloud networking feature that allows VM instances with only internal (private) IP addresses to reach the public IP addresses of Google APIs and services.
### Key Features
* Internal-Only Reachability: Specifically designed for VMs that do not have external IP addresses.
* Service Support: Provides access to most Google services, including Cloud Storage, BigQuery, Cloud Run, and Pub/Sub.Traffic Security: Traffic remains entirely within Google’s private network backbone and does not traverse the public internet.
* Configuration: Enabled on a per-subnet basis.

### Prerequisites for Use
To use PGA, your VPC network must meet these requirements:
* No External IP: The VM must only have an internal IP address.
* Subnet Setting: The subnet where the VM resides must have "Private Google Access" set to On.
* Default Route: The VPC must have a default route (dest: 0.0.0.0/0) with the default internet gateway as the next hop.
* DNS Support: By default, APIs resolve to public IPs, but traffic is automatically routed internally once PGA is active.

## Introduction to Classes in GCP cloud Storage Classes
Google Cloud Storage offers four primary object storage classes.Each class optimizes the trade-off between monthly storage costs and data retrieval fees. They cater to everything from frequently accessed "hot" data to infrequently accessed backups.

## Core Storage Classes

### Standard Storage
* Best Used For: Hot data, active websites, streaming, and mobile apps.
* Access Frequency: Highly frequent access with low latency.
* Cost Profile: Highest storage costs, lowest (or zero) retrieval fees.
* Minimum Duration: None.

### Nearline Storage
* Best Used For: Data accessed less than once a month.
* Access Frequency: Infrequent access and bulk data modifications.
* Cost Profile: Lower storage costs, higher retrieval fees than Standard.
* Minimum Duration: 30 days.

###Coldline Storage
* Best Used For: Disaster recovery and archival data accessed less than once a quarter.
* Access Frequency: Rare access and long-term backups.
* Cost Profile: Very low storage costs, significant retrieval/operation fees.
* Minimum Duration: 90 days.

### Archive Storage
* Best Used For: Long-term compliance, regulation retention, and data accessed less than once a year.
* Access Frequency: Coldest data with the longest first-byte retrieval latency.
* Cost Profile: Lowest storage costs, highest retrieval/operation fees.
* Minimum Duration: 365 days.

### Key Features and Specifications
* System PerformanceDurability: 99.999999999% (11 9s) across all classes.
* Capacity: Unlimited maximum storage capacities.
* Availability: Same global accessibility for all tiers.

### Additional Configuration Options
* Autoclass: Automatically transitions objects to lower-cost storage tiers based on access patterns to reduce manual lifecycle management operations.
* Dual-Region & Multi-Region: Allows Standard, Nearline, and Coldline data to be stored across multiple geographic regions for increased availability and redundancy.

Steps to Create a Cloud Storage Bucket:

1. Click on Navigation Menu. Click on Cloud Storage. Click on Bucket.

<img width="934" height="1012" alt="image" src="https://github.com/user-attachments/assets/e4cc6eb7-923b-4368-8c02-157a1454300f" />

2. Click on Create Bucket. Give a name to the Bucket and Click on continue.

<img width="1165" height="957" alt="image" src="https://github.com/user-attachments/assets/980d93e9-71fd-4805-aef3-9fb283058b3a" />

3. Click on Regional( I have selected need clarification from Darsh on what will be the real time scenario.
<img width="1045" height="875" alt="image" src="https://github.com/user-attachments/assets/168cda85-b605-4a3a-a81f-7e663af58080" />
If you select on Add- cross bucket replication you need tp select a bucket. I think i have created this bucket earlier when i tried and i have deleted. But buckets in GCP are global So need to check if this still exist in my organization.

<img width="1792" height="997" alt="image" src="https://github.com/user-attachments/assets/34b90949-9229-463d-99ac-7ad897d8dadc" />

But I am not selecting the Cross bucket replication. So removing the option again.
<img width="947" height="648" alt="image" src="https://github.com/user-attachments/assets/9489ce5b-18cf-4bd4-a775-1679ea40b13e" />

4. Click on Continue. Select a class. I am going with Default option which is "Standard"

<img width="1452" height="1012" alt="image" src="https://github.com/user-attachments/assets/2379fbc3-626a-4d6e-806e-5550023fc8bf" />

We usually do not enable Hierarchical Namespace

5. Click on Continue.  Select default "Uniform" access control.

<img width="1541" height="1025" alt="image" src="https://github.com/user-attachments/assets/e0c9ea76-7674-4e44-881d-2e1a4f859e4e" />

Ask clarification the note GCP is saying 

6. Click on continue and select the retension policy.
<img width="1737" height="1012" alt="image" src="https://github.com/user-attachments/assets/9613b5fa-fe3c-460f-9811-d595b3041e7d" />

for now i am oing with soft delete. If it is custom what will be the general retention period. for different classes? Ask what other options below it is about?


7. Click on Data encryption. Select GCP managed keys or customer keys. for customer keys please enable the allowed for customer keys below.
Ask Darsh on this?

<img width="1440" height="980" alt="image" src="https://github.com/user-attachments/assets/bc9b735e-862e-4271-a42e-2e799e02d3a2" />
8. Click on Create. select the check box to prevent public access on this bucket.
<img width="1918" height="933" alt="image" src="https://github.com/user-attachments/assets/a1d76bc8-839c-4899-8b9a-69ef6eb350b7" />

9. Click on confirm.

<img width="1911" height="930" alt="image" src="https://github.com/user-attachments/assets/cfe553b7-0796-44b2-9c3a-b04e1124a7ab" />

10.Earlier i have a bucket created in this compartment so it showed in the cross bucket replication.

### Upload a File through Console:

* Click on upload button and select any file.

<img width="1918" height="992" alt="image" src="https://github.com/user-attachments/assets/a2369ef7-89ac-48c0-9f68-7f1622bd7c1e" />

### Access Bucket through VM:

* Create a VM.
<img width="1541" height="686" alt="image" src="https://github.com/user-attachments/assets/176a52dd-c055-4e1b-a180-38b3c292895a" />

* SSH into the VM

<img width="607" height="485" alt="image" src="https://github.com/user-attachments/assets/0d96d2a3-0ff1-4c47-9c4d-20239191e9c7" />

* Open the Flip-app-subnet in Flip_VPC network. Private Google access is off. { Private google access is similar to service gateway in OCI. Private network connection to services in GCP}

<img width="1500" height="962" alt="image" src="https://github.com/user-attachments/assets/5b70fa7f-37ce-4317-ab80-a6516589d86b" />

* Execute Command in VM
```
gcloud storage ls gs://bucketname/
```

<img width="720" height="803" alt="image" src="https://github.com/user-attachments/assets/422bcb88-fd16-417e-8b3d-b16abcea8ee8" />

* The VM is unable to access the bucket. VM is private and also Bucket is private.

* Now enable the Private Google Access in the subnet. 

<img width="1350" height="912" alt="image" src="https://github.com/user-attachments/assets/d337d3e3-36c7-4b6f-b951-ef90fed5fa86" />

* Now try the same command in the VM.

Still I cannot login into the bucket.
<img width="1066" height="661" alt="image" src="https://github.com/user-attachments/assets/cdf337ce-d0e7-40d4-a5cd-79a75a6b629b" />

* IAM Role is missing. Lets try adding it.
* Click on IAM -> Service accounts.
<img width="1911" height="788" alt="image" src="https://github.com/user-attachments/assets/f43b0c5d-d5b0-48e1-a154-e8606c3a3b48" />

* Open the Service account. Click on Permissions. Click on Manage Access.

<img width="1821" height="896" alt="image" src="https://github.com/user-attachments/assets/4ac9ee36-b999-4573-b76e-fbf7caaa81dd" />

<img width="1907" height="1012" alt="image" src="https://github.com/user-attachments/assets/b25fd00b-a76c-486b-87d7-ecbf29a71fe0" />

* Click on Add Role. Assign Storage Object user role. Save it.

<img width="1918" height="945" alt="image" src="https://github.com/user-attachments/assets/197ed46c-79df-4070-918a-e6a615668854" />

*  Try again the command.
<img width="1101" height="887" alt="image" src="https://github.com/user-attachments/assets/b584f586-c61d-4be6-b8d4-7a2cf4e4fc43" />
* the issue is VM is created ion US Central.I have enable PGA access in Flipapp-subnet which is in US east 1. But the VM is created in US central and it is not enabled in the default subnet.

* Created another VM in US east 1 region. SSH into the VM and execute the gcloud ls command. It displays list of files in the bucket.

<img width="1083" height="762" alt="image" src="https://github.com/user-attachments/assets/54df68c4-d066-42bb-857d-77ac895e5a3d" />


* To Copy or upload files.
```
gcloud storage cp test.txt gs://flipapp-bucket

```
<img width="963" height="708" alt="image" src="https://github.com/user-attachments/assets/9060c1a6-9b61-4cf1-bc67-c23becb9e5c2" />
<img width="1632" height="658" alt="image" src="https://github.com/user-attachments/assets/e2bce2aa-eed5-48a0-8b93-d184b21b8c67" />

IAM Permissions are there for the service account. 
AI is saying the issue is with VMs cloud API access scope. Here it is default access. It is asking to give full access. It says it not an issue it gives full control to IAM.

<img width="1907" height="1017" alt="image" src="https://github.com/user-attachments/assets/d8ab93c4-8c35-40db-97b1-9d0feb037fbd" />

* So stop the VM and Edit the access and try to copy files into storage bucket.
Due do some reson i am junable to edit the instance. So created a new instance in same region with full access to cloud APIs.

<img width="1801" height="1022" alt="image" src="https://github.com/user-attachments/assets/d60b3e43-3c6e-42c3-95d1-8d977fd709cd" />

* Now SSH to the VM, create a file and copy it tp bucket.

<img width="1112" height="668" alt="image" src="https://github.com/user-attachments/assets/1fbc7715-1657-4ca6-8d68-c2ea8839f201" />

Successfully uploaded file into the bucket lets check it in console.
<img width="1707" height="862" alt="image" src="https://github.com/user-attachments/assets/79037f83-e84f-4474-b6a9-11bbf94522c7" />
<img width="1010" height="737" alt="image" src="https://github.com/user-attachments/assets/0f47502f-81bc-48ba-b661-0488c7368248" />









