# Routes in GCP
In Google Cloud Platform (GCP), route tables define how network traffic is directed within a Virtual Private Cloud (VPC). They determine the path packets take between subnets, instances, and external networks. Every VPC has an implicit route table that contains system-generated routes, and you can add custom routes for advanced traffic control.

🔑 Key Concepts
- System Routes: Automatically created by GCP for each subnet (e.g., local subnet route, default internet route if external IPs exist).
- Custom Routes: User-defined routes to control traffic flow (e.g., sending traffic to a VPN gateway or firewall appliance).
- Destination: CIDR block that defines where traffic is headed.
- Next Hop: Target for traffic (e.g., default internet gateway, VM instance, VPN tunnel, peering connection).
- Priority: Determines which route is chosen when multiple routes match. Lower numbers = higher priority.

📌 Types of Routes
- Default Routes: Direct traffic to the internet (0.0.0.0/0 → default internet gateway).
- Subnet Routes: Automatically created for each subnet CIDR block.
- Peering Routes: Enable communication between peered VPCs.
- VPN Routes: Direct traffic through Cloud VPN tunnels.
- Custom Static Routes: Manually defined for specific traffic redirection.

📂 Example: Default Route Table
Destination      Next Hop
10.0.0.0/24      Local Subnet
0.0.0.0/0        Default Internet Gateway


⚙️ Best Practices
- Keep default routes intact unless you have strict security needs.
- Use custom routes for hybrid connectivity (VPN, Cloud Interconnect).
- Audit routes regularly to avoid misconfigurations.
- Apply least privilege: restrict who can create/modify routes.
- Document route changes in your team wiki for governance.

⚠️ Risks & Considerations
- Misconfigured routes can cause traffic blackholes or expose resources unintentionally.
- Overlapping CIDR ranges may lead to unpredictable routing.
- Removing default internet routes can block external access.

## Steps to create Route

1. Click on Navigational Menu.

2. Click in VPC Network. Select Routes.

<img width="1891" height="960" alt="image" src="https://github.com/user-attachments/assets/9d50816c-478a-4ff7-ad8a-c32e06dcfbc3" />

<img width="1892" height="937" alt="image" src="https://github.com/user-attachments/assets/d8a5dc20-9dd0-44c7-8b9a-32881ddbb8e9" />

3. Click on Route Management.

<img width="1911" height="907" alt="image" src="https://github.com/user-attachments/assets/b31b92e6-de45-4d94-818c-42a1482a8d52" />

4. Click on "Create Route". Provide Name, description, Network, Destination Ip, Next hop as Default internet gateway. Click on Create.

<img width="1915" height="910" alt="image" src="https://github.com/user-attachments/assets/6584b252-1fc7-458e-a748-8342fb99cfcb" />

<img width="1902" height="857" alt="image" src="https://github.com/user-attachments/assets/e51bb759-0c8c-4d5d-83e7-a1c8b62265e5" />


