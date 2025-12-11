# OCPU vs vCPU

## What Is an OCPU?
An **OCPU (Oracle CPU)** is Oracle Cloud Infrastructure’s compute unit.  
It represents the full performance of **one physical CPU core**, including **two hardware execution threads**.

### Key Points
- 1 OCPU = 1 physical core  
- 1 OCPU = 2 vCPUs (threads)  
- Billed per core  
- Higher compute per unit compared to vCPU‑based billing

---

## What Is a vCPU?
A **vCPU (virtual CPU)** is used by AWS, Azure, GCP, and other cloud providers.  
A vCPU typically represents **one hardware thread** of a physical CPU core.

### Key Points
- 1 vCPU = 1 hardware thread  
- 2 vCPUs = 1 physical core  
- Billed per thread  
- Lower compute per unit compared to OCPU

---

## Comparison Table

### OCPU vs vCPU Differences

| Feature | OCPU (Oracle) | vCPU (AWS/Azure/GCP) |
|--------|----------------|-----------------------|
| Represents | 1 physical core | 1 hardware thread |
| Threads | 2 threads | 1 thread |
| Billing | Per core | Per thread |
| Performance per unit | Higher | Lower |

---

## Why This Matters

### Practical Impact
- Oracle provides **double the threads** per unit compared to vCPU‑based clouds.  
- OCPU pricing may appear higher, but you receive **more compute capacity**.  
- Ideal for CPU‑intensive workloads such as databases, analytics, and microservices.
