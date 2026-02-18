# Organization and difference between Region vs AZ vs FD

## 1. Organization

An Organization represents the company or enterprise account in GCP.

### Characteristics

* Root-level container for all resources

* Linked to corporate identity domain

* Controls billing and policies

* Contains folders and projects

### Usage

* Used by enterprises to centrally manage users, projects, and policies.

## 2. Project

A Project is the primary working container where resources are created.

### Characteristics

* All resources belong to a project

* Billing is tracked at project level

* Permissions are often assigned per project

* Projects isolate environments or workloads

### Example Uses

* Production project

* Development project

* Testing project

## 3. Region

A Region is a geographic location where GCP hosts data centers.

## Characteristics

* Each region contains multiple zones

* Regions are geographically separated

* Used for latency and disaster recovery planning

### Example Regions

* asia-south1 (Mumbai)

* us-central1

* europe-west1

## 4. Zone (Equivalent to Availability Domain)

A Zone is a deployment area within a region.

### Characteristics

* Independent infrastructure within a region

* Used to deploy compute resources

* Regions typically contain multiple zones

### Example

Region: asia-south1
Zones:

* asia-south1-a

* asia-south1-b

* asia-south1-c

Fault Domain in GCP

* GCP does not expose fault domains. Hardware fault isolation is handled automatically, and users achieve availability by deploying across zones.

Explanation

* Hardware fault separation is automatically managed by Google.

* Users deploy across zones for availability instead of selecting fault domains.