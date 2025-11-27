# Create a firewall rule which allow Incoming traffic from 10.0.0.0/16 on port 53/UDP excluding 10.0.3.0/24

## Goal
* We want to allow Incoming traffic from 10.0.0.0/16 on port 53/UDP excluding 10.0.3.0/24

## CIDR Breakdown
We want:
- Allow: 10.0.0.0/16 (covers 10.0.0.0 – 10.0.255.255)
- Exclude: 10.0.3.0/24 (covers 10.0.3.0 – 10.0.3.255)

## Deny 10.0.3.0/24 Ingress

1. Open Google Cloud Console
2. Click on the Burger Menu.
3. Click on "VPC Network" and Click on "VPC Networks"

<img width="1552" height="884" alt="image" src="https://github.com/user-attachments/assets/8a12fba3-db59-46eb-8af6-b5385a40dc80" />

4. Click on hub-VPC network

<img width="1905" height="892" alt="image" src="https://github.com/user-attachments/assets/3b1fc3f6-aaa5-4a4b-827a-0de8d6f4a9f2" />

5. Click on Firewall

<img width="1897" height="911" alt="image" src="https://github.com/user-attachments/assets/32b01e3a-84b5-4c4d-9d78-80dfe748ccc6" />

6. Click on "Create Firewall rule"

<img width="1455" height="954" alt="image" src="https://github.com/user-attachments/assets/58e4a1c4-dc80-4eb6-b9ca-ef73dec2413a" />

<img width="1675" height="979" alt="image" src="https://github.com/user-attachments/assets/bf4eff41-8bb7-4cb1-a801-029aff8d4c07" />

<img width="1607" height="910" alt="image" src="https://github.com/user-attachments/assets/f4e8d456-fc44-4d6c-a94a-ce7fd9d1b9ea" />

7. click on create.

<img width="1837" height="955" alt="image" src="https://github.com/user-attachments/assets/1a9d0161-622b-4bb4-93e1-1bae67f358b4" />

## Allow 10.0.0.0/16 ingress

1. Click on "Create Firewall rule"

<img width="1873" height="871" alt="image" src="https://github.com/user-attachments/assets/7e80fdd9-4458-4af7-a594-8a366637d5b7" />

<img width="1502" height="911" alt="image" src="https://github.com/user-attachments/assets/508dfecb-9ab6-40da-bd76-a11459784f41" />

<img width="1661" height="977" alt="image" src="https://github.com/user-attachments/assets/03200935-d5a5-4f59-ae2e-4537d689a02e" />

2. click on create

<img width="1565" height="988" alt="image" src="https://github.com/user-attachments/assets/87f70fe2-29df-46fa-b6df-559cc3d42174" />

