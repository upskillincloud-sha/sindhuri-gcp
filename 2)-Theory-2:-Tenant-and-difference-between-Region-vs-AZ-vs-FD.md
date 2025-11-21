# Tenant and difference between Region vs AZ vs FD
## Tenant
* A tenant in Azure represents a dedicated and trusted instance of Azure Active Directory (Azure AD) that your organization receives when it signs up for Microsoft cloud services (like Azure, Microsoft 365, or Dynamics 365).

* Each tenant is unique to an organization.

* It includes the user directory, domain(s), and identity management for that organization.

* Tenancy is about logical isolation — your resources, users, and data are isolated from other tenants, even though they share Microsoft’s global infrastructure.

### Directory 
A directory is a container for objects such as users, groups, and applications, and is used to manage access to resources in Azure. A directory is also associated with a unique directory ID, which is a GUID that identifies the directory in Azure AD.

### Domain
A domain is a name that identifies a group of resources on the internet, such as a website or an email server. In Azure, a domain is used to verify ownership of a custom domain name and to create user names and email addresses for users in a tenant. A domain can be associated with one or more tenants, and each tenant can have multiple domains.



## 🌍 Azure Region

An Azure Region is a geographical area that contains one or more datacenters connected through a low-latency network.
### Examples

* East US

* West Europe

* Southeast Asia

### Each region provides:

* Physical location for your resources.

* Regional redundancy options.

* Compliance with local data residency laws.

* You choose a region when deploying most Azure resources (VMs, storage accounts, etc.).

## 🧩 Availability Zone (AZ)

* An Availability Zone is a physically separate datacenter within a region, each with its own power, cooling, and networking.

* Each region typically has 3 Availability Zones (AZs), e.g., 1, 2, 3.

* They are connected by high-speed, low-latency fiber links.

* Using AZs helps you achieve high availability and fault tolerance within the same region.

### Example

Deploying VMs across AZ1, AZ2, and AZ3 in East US ensures that if one datacenter fails, your application remains available in the others.

## ⚙️ Fault Domain (FD)

* A Fault Domain represents a logical group of hardware within an Azure datacenter that shares a common power source and network switch.

* Fault domains are about physical separation within a single datacenter.

* Azure automatically distributes your VMs across multiple FDs (usually up to 3) when you use an Availability Set.

* This minimizes the impact of hardware failures, power interruptions, or network issues.


### In short:

Tenant = your organization’s identity boundary.

Region = where your resources live geographically.

Availability Zone (AZ) = separate datacenters in one region.

Fault Domain (FD) = hardware clusters within one datacenter.
