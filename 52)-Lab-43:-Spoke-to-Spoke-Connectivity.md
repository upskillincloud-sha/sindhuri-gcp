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

* Click on networking. Click on enable IP forwarding.

<img width="1836" height="1011" alt="image" src="https://github.com/user-attachments/assets/e872fd93-ceab-4106-abf6-bd9509532588" />

* Click on new network interface

<img width="1541" height="1013" alt="image" src="https://github.com/user-attachments/assets/6e9ca052-1208-4877-9094-52b05ffb7415" />

* Add all the nic of all vcns(i.e hub, flip, spoke)

<img width="1410" height="937" alt="image" src="https://github.com/user-attachments/assets/482c1a79-ed21-47c6-83f3-6d0a6b7f4f15" />

* While creating nic, external Ipv4 address as none. for all the three nics.

<img width="1887" height="1010" alt="image" src="https://github.com/user-attachments/assets/8757851a-4d73-4ac2-bcff-2f7f5ae78476" />

* Click on create.

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

2. Click on connectivity tests.

<img width="1919" height="984" alt="image" src="https://github.com/user-attachments/assets/1018c021-c96f-442a-b222-88d9630aa8fa" />
 
3. Click on create connectivity test

<img width="1917" height="1018" alt="image" src="https://github.com/user-attachments/assets/5f719d64-0f19-4202-bcc0-0144551a07f8" />

4. Click on create.

Results before configuring Ip tables in NVA Server.

<img width="1830" height="1073" alt="image" src="https://github.com/user-attachments/assets/5d6bbf0c-3d6f-4b7a-895b-c4e54f5d4279" />

* The traffic is blocking at ingress of Flip server is because Flip-vcn traffic is not allowed in flip-vcn(since we are adding nic of flip hub and skillup in nva to route traffic. So we need to allow flip-vcn traffic in ingress of flip-vcn for traffic to be allowed inside nva.

<img width="1915" height="1017" alt="image" src="https://github.com/user-attachments/assets/561b67d7-6a05-4849-8143-247d8b9c82a1" />

<img width="1720" height="985" alt="image" src="https://github.com/user-attachments/assets/1ca927a3-51bb-4b0b-afc7-5f84f96eaded" />

<img width="1742" height="1021" alt="image" src="https://github.com/user-attachments/assets/56a400fe-90e6-413f-9159-1f5bc16a0e38" />

* We also need to configure ip tables in NVA server for traffic to flow to other spoke. Otherwise the connectivity tests in gcp shows successfull but traffic doesn't really flow.

<img width="1918" height="1017" alt="image" src="https://github.com/user-attachments/assets/de726d8a-7852-41df-83af-a5b3f82b38a4" />

The above connectivity test says the traffic could be sent. it didn't really confirm the connection and traffic flow is successful. Until and unless the ip tables are configured in nva server, the traffic does not flow even though the connectivity tests shows the spoke is reachable.

## Configure ip tables in NVA

1. Login to nva Server.

2. Click on SSH in connect. In GCP we connect to server in browser.

3. Follow the below steps and configure ip tables in NVA.

* Accept forwarding from Spoke to Spoke2:
sudo iptables -A FORWARD -s 192.168.2.0/24 -d 192.168.3.0/24 -j ACCEPT

* Accept forwarding from Spoke2 to Spoke:
sudo iptables -A FORWARD -s 192.168.3.0/24 -d 192.168.2.0/24 -j ACCEPT

* Allow established connections:
sudo iptables -A FORWARD -m state --state ESTABLISHED,RELATED -j ACCEPT

4.	First we have to update the package list:
sudo apt-get update

* Install iptables-persistent to save rules:
sudo apt-get install iptables-persistent -y

* When prompted during installation:

"Save current IPv4 rules?" → Select Yes (press Tab to highlight Yes, then Enter)
"Save current IPv6 rules?" → Select Yes

* Save the iptables rules:
sudo netfilter-persistent save


<img width="1913" height="1013" alt="image" src="https://github.com/user-attachments/assets/f4398fd8-7d1c-4552-a9d1-888432e0a5b5" />

5. Do ping to Spoke skillup, also do telnet ip of the server port.

<img width="512" height="408" alt="image" src="https://github.com/user-attachments/assets/47019c03-0d82-480c-910b-7ebccb049a2e" />


Connectivity tests results in NVA:

1. Repeat the connectivity test spoke to Spoke.

<img width="1915" height="1017" alt="image" src="https://github.com/user-attachments/assets/06db05a5-62f8-473a-9975-f8dbc06d82d5" />

<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/8a7398d5-4824-4452-b142-58c246cf9827" />

<img width="1897" height="1061" alt="image" src="https://github.com/user-attachments/assets/3b024638-5a42-49ad-9b0f-0187723e6067" />
