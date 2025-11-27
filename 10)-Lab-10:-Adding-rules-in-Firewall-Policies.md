# Adding rules in Firewall

## Steps to add Filewall Rules

1. Open Google Cloud Console
2. Click on the Burger Menu.
3. Click on "VPC Network" and Click on "VPC Networks"

<img width="1552" height="884" alt="image" src="https://github.com/user-attachments/assets/8a12fba3-db59-46eb-8af6-b5385a40dc80" />

4. Click on hub-VPC network

<img width="1905" height="892" alt="image" src="https://github.com/user-attachments/assets/3b1fc3f6-aaa5-4a4b-827a-0de8d6f4a9f2" />

5. Click on Firewall

<img width="1897" height="911" alt="image" src="https://github.com/user-attachments/assets/32b01e3a-84b5-4c4d-9d78-80dfe748ccc6" />

6. Click on "Create Firewall rule"

* Provide Name, Description
* Select Network as hub-vpc
* Direction of Traffic Ingress/Egress (Based on the requirement) Here selecting Ingress
* Action: Allow
* Targets : all instances in Network
* Protocols: Specified, TCP

<img width="1868" height="968" alt="image" src="https://github.com/user-attachments/assets/e0db67b0-74c6-4b6c-b912-751b46bff94f" />

<img width="1879" height="971" alt="image" src="https://github.com/user-attachments/assets/222bc4cf-429d-4e61-9574-a5dee9539b9a" />

<img width="1910" height="1007" alt="image" src="https://github.com/user-attachments/assets/a227018a-8419-4c4b-bd3d-9dc0cf71352d" />

7. Click on Create

<img width="1517" height="921" alt="image" src="https://github.com/user-attachments/assets/a3555918-ddd9-492c-93ed-7679755d8055" />

<img width="1499" height="857" alt="image" src="https://github.com/user-attachments/assets/914d823e-c19a-4545-ac54-16f22b0f31aa" />
