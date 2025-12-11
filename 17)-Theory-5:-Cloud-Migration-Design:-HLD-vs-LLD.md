# Cloud Migration Design: HLD vs LLD
In cloud migration projects, design documentation is critical for clarity, governance, and successful execution. This guide explains the difference between **High-Level Design (HLD)** and **Low-Level Design (LLD)**, their roles, and who prepares each.

## High-Level Design (HLD)

### Purpose
- Define migration objectives such as scalability, cost optimization, and security.
- Provide a clear architectural vision.
- Align stakeholders on scope and approach.

### Key Components
- Target cloud architecture (single-cloud, hybrid, or multi-cloud).
- Network topology (VPCs, subnets, peering).
- Identity & access model (IAM hierarchy, roles).
- Service mapping (on-prem workloads → cloud services).

### Prepared By
- Cloud/Enterprise Architects
- Solution Architects
- Reviewed by Project/Program Managers

### Audience
- Architects
- Project Managers
- Stakeholders

### Output
- Architecture diagrams
- Migration roadmap
- Governance principles
- Service mapping documentation

## Low-Level Design (LLD)

### Purpose
- Translate HLD into technical specifications and implementation steps.
- Ensure reproducibility and compliance.
- Serve as a reference for deployment and troubleshooting.

### Key Components
- CIDR ranges, firewall/security list rules, routing tables.
- VM instance types, storage tiers, autoscaling policies.
- IAM roles, policies, and least-privilege assignments.
- Step-by-step runbooks (CLI commands, Terraform scripts).

### Prepared By
- Cloud Engineers / DevOps Specialists
- System Administrators
- Network Engineers

### Audience
- Engineers
- DevOps teams
- Administrators

### Output
- Configuration files
- Infrastructure-as-code scripts
- Deployment runbooks
- Detailed technical specs

## HLD vs LLD Comparison

| Aspect              | HLD (High-Level Design) | LLD (Low-Level Design) |
|---------------------|--------------------------|-------------------------|
| **Focus**           | Architecture & strategy | Technical implementation |
| **Detail Level**    | Abstract, conceptual    | Concrete, step-by-step   |
| **Audience**        | Architects, managers    | Engineers, DevOps        |
| **Output**          | Diagrams, architecture docs | Config files, scripts, runbooks |
| **Purpose**         | Align vision & goals    | Execute migration safely |

## Best Practices
- Always create **HLD first**, then refine into **LLD**.
- Maintain traceability between HLD and LLD.
- Use diagrams in HLD and detailed runbooks in LLD.
- Review both documents regularly to ensure alignment with evolving cloud services.

## Conclusion
Think of **HLD as the migration blueprint** and **LLD as the construction manual**. Both are essential for a successful cloud migration. Clear documentation empowers teams, reduces risk, and ensures smooth execution.
