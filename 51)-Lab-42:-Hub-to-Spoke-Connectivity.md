Create instances in Hub, Skillup, Flip

Hub Server

<img width="1918" height="899" alt="image" src="https://github.com/user-attachments/assets/bf32d49b-279d-4f1e-8c1a-7893f011fee5" />

Flip Server

<img width="1913" height="931" alt="image" src="https://github.com/user-attachments/assets/a98e6a72-0a7c-48b4-94d3-ae4f02a5338f" />

Skillup Server

<img width="1891" height="953" alt="image" src="https://github.com/user-attachments/assets/80882c1e-05e2-4d1a-9f46-26fd45ebe4eb" />

## VPC Network Peering

### Hub network project to Flip Network project
1. In project picker, select Hub network project. Click on navigational Menu. Click on VPC Network. Click on VPC network peering. 

<img width="1786" height="838" alt="image" src="https://github.com/user-attachments/assets/25c7b286-b963-4307-a8af-13f768232729" />

2. Click on "Create Connection"

<img width="1752" height="815" alt="image" src="https://github.com/user-attachments/assets/97eae2fc-1fa3-4841-b6cd-facc2e35434a" />

3. Fill the details. Peering connection name. VPC-network, peered vpc network, project id, vpc network name. Click on required check boxes.

<img width="1414" height="913" alt="image" src="https://github.com/user-attachments/assets/994794cb-4a67-40db-a5f7-53d42197f05a" />

4. Click on create.

<img width="1898" height="897" alt="image" src="https://github.com/user-attachments/assets/98dbcf0a-0dd6-41d8-8ae6-c7e5921cc493" />

Peering Status is inactive because the peering is still jot done from flip to hub.

### Flip network Project to Hub network Project peering

1. In project picker, select Flip network project. Click on navigational Menu. Click on VPC Network. Click on VPC network peering. 

<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/9160dfd1-4791-49d3-bba0-9cde85e8415f" />

2. Click on "Create Connection"

<img width="1403" height="813" alt="image" src="https://github.com/user-attachments/assets/50c0d1db-8e5a-4962-9203-907859bb24eb" />

3. Fill the details. Peering connection name. VPC-network, peered vpc network, project id, vpc network name. Click on required check boxes.

<img width="1714" height="911" alt="image" src="https://github.com/user-attachments/assets/7b9b8aed-57fa-4420-bc34-5b3b4b31785f" />

4. Click on Create.

<img width="1919" height="885" alt="image" src="https://github.com/user-attachments/assets/161182f4-6425-4405-a7a8-1a3281f3897e" />

Now refresh the page and we can see the peering status be become active.

<img width="1906" height="927" alt="image" src="https://github.com/user-attachments/assets/e6b7f1f7-2745-4773-97bc-9f326adede56" />

<img width="1905" height="834" alt="image" src="https://github.com/user-attachments/assets/3026dcb8-4020-4b89-a865-3af6d0a62f03" />

### Hub to Skillup Peering

<img width="1913" height="967" alt="image" src="https://github.com/user-attachments/assets/c33d3aba-1b40-4787-a6ae-febc37afa98e" />
<img width="1919" height="847" alt="image" src="https://github.com/user-attachments/assets/b5fb74f9-39b2-40b1-86f9-ac4464919c37" />
<img width="1884" height="898" alt="image" src="https://github.com/user-attachments/assets/48d50d79-8e25-4315-8440-837f5c4ca90b" />
<img width="1916" height="960" alt="image" src="https://github.com/user-attachments/assets/a86eb330-17aa-4038-8137-0193f66f383e" />
<img width="1913" height="858" alt="image" src="https://github.com/user-attachments/assets/4e9a9fb3-9bc6-43cf-b01a-81569dfeaf37" />
<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/ef6e8d1f-d139-4c75-a72c-67feefe5c4de" />

## Connectivity Test
### Hub-Flip Connectivity Test(TCP on port 22)

1. Search for Connectivity Test. Click on Enable.

<img width="1912" height="911" alt="image" src="https://github.com/user-attachments/assets/01ecc70b-82c1-40a8-9938-7051e91dc817" />

<img width="1916" height="975" alt="image" src="https://github.com/user-attachments/assets/e5fec267-408d-43b0-8446-acd15d5a4432" />

2. Click on Create Connectivity Test. Fill all the details.

<img width="1672" height="916" alt="image" src="https://github.com/user-attachments/assets/4050e073-3f30-48a4-868a-5912221262d8" />

3. Click on Create.

<img width="1915" height="908" alt="image" src="https://github.com/user-attachments/assets/24eeadd7-e949-4f0a-a6f3-337c4f634de7" />

4. Click on the connectivity to see details of connectivity test.

<img width="1913" height="1073" alt="image" src="https://github.com/user-attachments/assets/2f77486d-5eae-4652-ae88-a795e78a1955" />

<img width="1898" height="1009" alt="image" src="https://github.com/user-attachments/assets/9095172b-465c-45ee-9124-ca02e192dc8f" />

### Hub to Skillup connectivity test(TCP on port 22)

1. Search for Connectivity Test. Click on Enable.

Repeat the above steps and click on create.

<img width="1908" height="990" alt="image" src="https://github.com/user-attachments/assets/0d71eb2b-31ba-412e-86a3-9c21c250f9a3" />


<img width="1913" height="915" alt="image" src="https://github.com/user-attachments/assets/4c38955c-4f11-449e-969c-4fd77087c4fa" />

### Hub flip(ICMP)

<img width="1919" height="1012" alt="image" src="https://github.com/user-attachments/assets/ff3989a6-225d-40af-b849-8432da348b2c" />

<img width="1890" height="1026" alt="image" src="https://github.com/user-attachments/assets/ebdd3e9d-e7c2-4952-9c42-d658e6e2fdc0" />

### Hub-Skillup(ICMP) unsing IP address option

<img width="988" height="1018" alt="image" src="https://github.com/user-attachments/assets/98a3a2ac-19a3-4b79-ab61-4f042ceac4f1" />
<img width="1911" height="994" alt="image" src="https://github.com/user-attachments/assets/01e1bf0f-9b96-4eb4-83d6-7a46493c9481" />
<img width="1913" height="1043" alt="image" src="https://github.com/user-attachments/assets/99acf633-3a5f-4658-a2c1-d4db54909206" />
