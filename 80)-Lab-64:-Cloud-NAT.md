# Cloud NAT

* Downloading softwares into Private VM needs internet access. Since Private VM doesn't have External IP(public IP), it cannot connect to internet and download packages/software.
* We cannot assign VMs in private Network external IP because of Security reasons.
* We fix this issue by using Cloud NAT

* Create a Private VM.
<img width="1917" height="668" alt="image" src="https://github.com/user-attachments/assets/f67caa46-0f96-41f6-a2df-520c3d0404cd" />

* SSH into a Private VM. Authorize.
<img width="941" height="638" alt="image" src="https://github.com/user-attachments/assets/aa442d39-6463-4e11-a64f-cea653fbcdbe" />
<img width="1095" height="861" alt="image" src="https://github.com/user-attachments/assets/72cb4074-ebe7-4726-80f8-bbc85e7b38a5" />

* Try to install apache httpd service.
```
sudo apt install apache2 -y
```
<img width="1876" height="873" alt="image" src="https://github.com/user-attachments/assets/16b27278-7f7f-4d53-972f-8e65ff5d5cd7" />

So we need Cloud NAT to fix this issue.

## Cloud NAT
Cloud NAT in Google Cloud is a managed service that provides outbound internet access for private resources (VMs, GKE clusters, Cloud Run, etc.) without assigning them public IPs. It ensures secure, scalable, and controlled connectivity while blocking unsolicited inbound traffic.

* Cloud NAT (Network Address Translation) is a regional, managed gateway in Google Cloud.

* It allows resources in private subnets (no external IPs) to initiate outbound connections to the internet or other networks.

* It translates internal private IPs into external IPs for outbound traffic.

* Inbound traffic is not allowed unless it is a response to an outbound request.
Benefits
Security: No need to expose VMs with public IPs.

Scalability: Fully managed, scales automatically with traffic.

High Availability: Built-in redundancy, no need for custom NAT VMs.

Cost Efficiency: Pay only for NAT IP usage and data processed.

Flexibility: Supports both Public NAT (internet access) and Private NAT (internal VPC-to-VPC connectivity).

⚠️ Considerations
Per VPC, per region: You need a separate Cloud NAT for each VPC and region.

Firewall rules: Outbound traffic must be allowed by firewall rules.

No unsolicited inbound: Cloud NAT cannot be used to host public-facing services.

## Steps to Create Cloud NAT

1. Login to GCP (console.cloud.google.com).
2. Go to Network Services. Click on Cloud NAT. Select Project.

<img width="1631" height="792" alt="image" src="https://github.com/user-attachments/assets/c7522ee7-bfdc-4eb2-9466-6dc11df2c7db" />

3. Click on Get Started.

<img width="1803" height="911" alt="image" src="https://github.com/user-attachments/assets/97b866f7-926b-4742-bb34-1db76d4b1739" />

4. Fill the Gateway Name. NAT type as Public since we need to communicate with internet.
5. In Select Cloud reouter section, Select the VPC in Network,Region( must be same region as VM), Click on Create New Cloud Router. 

<img width="1411" height="1017" alt="image" src="https://github.com/user-attachments/assets/8b6023c0-8c02-4cbc-937f-a899668c1810" />
<img width="1255" height="1019" alt="image" src="https://github.com/user-attachments/assets/5d88cd92-4184-4f38-8bcc-bad74d8913a7" />

6. Click on Create.
<img width="1646" height="901" alt="image" src="https://github.com/user-attachments/assets/a6d4c7ab-df16-4fb2-8562-f57d5b02fd37" />
<img width="984" height="918" alt="image" src="https://github.com/user-attachments/assets/faef0c0a-20db-4a8b-a7c7-53e4fe887a08" />

7. Now install again httpd service.

```
sudo apt install apache2 -y
```
<img width="1540" height="872" alt="image" src="https://github.com/user-attachments/assets/842e62e5-a2f0-40ea-ba56-c16fba1c2297" />

8. Check the status of the service.
```
sudo systemctl status apache2

```  
<img width="1047" height="351" alt="image" src="https://github.com/user-attachments/assets/348655a8-1c66-4e41-8b81-78d8e0554a38" />
