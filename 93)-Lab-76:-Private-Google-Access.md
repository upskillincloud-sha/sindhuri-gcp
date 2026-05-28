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


