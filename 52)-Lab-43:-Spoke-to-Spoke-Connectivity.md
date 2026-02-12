## Make VM as NVA
## Create VPCs
* Create all networks in single Network project.
<img width="1873" height="1008" alt="image" src="https://github.com/user-attachments/assets/2fa5fad4-1157-426e-b775-4e0d63917985" />

## Create nva-server
* Click on 
* Enter details like name

<img width="1902" height="1020" alt="image" src="https://github.com/user-attachments/assets/5231907c-5317-4c1d-82a4-e8c075016e97" />

* Select N2 and select 4 core.

<img width="1917" height="1016" alt="image" src="https://github.com/user-attachments/assets/293906a8-20ee-40a5-9b8d-85bd96c6920e" />

Click on networking. Click on enable IP forwarding.

<img width="1836" height="1011" alt="image" src="https://github.com/user-attachments/assets/e872fd93-ceab-4106-abf6-bd9509532588" />

Click on new network interface

<img width="1541" height="1013" alt="image" src="https://github.com/user-attachments/assets/6e9ca052-1208-4877-9094-52b05ffb7415" />

Add all the nic of all vcns(i.e hub, flip, spoke)

<img width="1410" height="937" alt="image" src="https://github.com/user-attachments/assets/482c1a79-ed21-47c6-83f3-6d0a6b7f4f15" />

While creating nic, external Ipv4 address as none. for all the three nics.

<img width="1887" height="1010" alt="image" src="https://github.com/user-attachments/assets/8757851a-4d73-4ac2-bcff-2f7f5ae78476" />

Click on create.

<img width="1919" height="961" alt="image" src="https://github.com/user-attachments/assets/5b891da6-6a13-4a30-88d2-af85f9674656" />

## Shared VPC
* Click on VPC networks

<img width="1873" height="1008" alt="image" src="https://github.com/user-attachments/assets/1b6fc812-1f8e-4cf1-a41a-fb9738d184a6" />

* Click on Shared VPC

<img width="1911" height="964" alt="image" src="https://github.com/user-attachments/assets/ca542492-b51b-47e8-810b-0d7f02ee336f" />

* Click on set up shared VPC.

<img width="1860" height="928" alt="image" src="https://github.com/user-attachments/assets/cd248e5c-3c7e-4d1e-98fc-7740cdb4bbf9" />

* Click on "Enable and Continue".

<img width="1918" height="1020" alt="image" src="https://github.com/user-attachments/assets/0329d0ba-9364-4519-92dc-fea59ae0787b" />

* Click on Attach Projects

<img width="1915" height="967" alt="image" src="https://github.com/user-attachments/assets/6c990d93-8dd0-4d37-b832-f98a6a0898c5" />
<img width="1911" height="1005" alt="image" src="https://github.com/user-attachments/assets/70bba3ed-5530-4116-84da-d20345ae507f" />
<img width="1915" height="1002" alt="image" src="https://github.com/user-attachments/assets/7a59a320-0d6c-4d56-b5d0-86846d5a7f8d" />

## Custom Routes

### Custom route from Flip to Skillup

1. Click on navigantional menu. Click on VPC network. Click on Routes.

<img width="1902" height="996" alt="image" src="https://github.com/user-attachments/assets/dcdfb7cc-7987-4e36-9d2b-8cd3e308c231" />

2. Click on Route Management.

<img width="1919" height="985" alt="image" src="https://github.com/user-attachments/assets/df287c01-5830-4e8c-a5c6-8ecf70ac8df7" />

3. Click on Create Route. Give name. Select network as flip-vcn. destination cidr will be skillup cidr. Specify ip address of instance and next hop will be nic of flip-vcn.

<img width="1913" height="968" alt="image" src="https://github.com/user-attachments/assets/d586a889-fddc-48f9-8070-832cb18bc0b1" />

4. Click on create.

<img width="1917" height="988" alt="image" src="https://github.com/user-attachments/assets/f7724f00-7363-4cfd-8563-036eb0f32201" />

### Skillup-flip-route-via-NVA

<img width="1647" height="1020" alt="image" src="https://github.com/user-attachments/assets/d4a0c7c8-4a81-48f0-ae6f-fe5b56e681e4" />

<img width="1918" height="957" alt="image" src="https://github.com/user-attachments/assets/dfb29f3b-be4d-4a2c-a6c7-ea0898668007" />

## Connectivity Tests

1. Click on All products. Click on Networking -> Network intelligence.

<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/ca7906b1-f358-4b68-aaa7-d41e071eaa99" />

<img width="1896" height="986" alt="image" src="https://github.com/user-attachments/assets/41e20615-c19d-45d3-9ddd-e588be688f3f" />



2.Click on connectivity tests.

<img width="1919" height="984" alt="image" src="https://github.com/user-attachments/assets/1018c021-c96f-442a-b222-88d9630aa8fa" />
 
Click on create connectivity test

<img width="1917" height="1018" alt="image" src="https://github.com/user-attachments/assets/5f719d64-0f19-4202-bcc0-0144551a07f8" />

Click on create.



