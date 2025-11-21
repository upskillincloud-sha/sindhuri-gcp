# Cloud Networking
In cloud computing, the terms Public Network and Private Network describe how the underlying infrastructure is shared and accessed, which directly impacts security, cost, control, and scalability.

## Public Networking
A Public Cloud Network refers to the resources and infrastructure provided by a third-party cloud service provider (CSP) over the public internet. The key feature is multi-tenancy, meaning multiple customers share the same physical hardware, though their data and workloads are logically isolated.

* **Definition**: Services offered by a third-party vendor (like AWS, Azure, Google Cloud) over the public internet.

* **Accessibility**: Accessible to virtually anyone who subscribes, using standard public IP addresses and network connections.

* **Control**: Low. The cloud provider manages all underlying infrastructure (networking, hardware, maintenance).

* **Security**: Follows a Shared Responsibility Model. The provider secures the infrastructure of the cloud, but the customer is responsible for security in the cloud (data, applications, operating systems).

**Scalability:** Virtually Unlimited. Resources can be rapidly scaled up or down on demand due to the provider's massive global infrastructure.

**Cost Model:** Pay-as-you-go (Consumption-based). Lower upfront capital expenditure.

## Private Cloud networking
A Private Cloud Network is a computing environment dedicated exclusively to a single organization. It is not shared with other customers (single-tenant). It can be hosted on the company's own on-premises data center or managed by a third-party provider in a dedicated environment.

### RFC 1918(10.0.0.0/8, 172.16.0.0/12, and 192.168.0.0/16)
* RFC 1918,"Address Allocation for Private Internets," defines specific blocks of IPv4 addresses reserved for use in private networks.

Class A: \(10.0.0.0\) to \(10.255.255.255\)  

Class B: \(172.16.0.0\) to \(172.31.255.255\)  

Class C: \(192.168.0.0\) to \(192.168.255.255\)  
* These addresses are not globally routable on the public Internet, allowing organizations to use them internally.

<img width="741" height="223" alt="image" src="https://github.com/user-attachments/assets/3fae5a75-d2c4-4459-9b2a-dea031a8f7d4" />

### Advantages
* **Non-routable:** These addresses are "non-routable," meaning they are not allowed to be sent across the public internet. Network administrators set up routers to block traffic with these private addresses from leaving their network.
* **Security**: By keeping internal devices off the internet, RFC 1918 addresses create a layer of security, as those devices are not directly exposed to external threats.
* **Reusability**: Since these addresses are not used on the public internet, they can be reused across different private networks without causing conflicts, as long as the networks are not connected to each other.
