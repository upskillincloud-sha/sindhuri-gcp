## Custom Routes

### Custom route from Flip to Skillup
1. In project Picker Select Flip-network-Proj
2. Click on Navigational Menu -> VPC Network -> Routes
3. Now select Network as hub-vpc & region. Click on View

<img width="1908" height="961" alt="image" src="https://github.com/user-attachments/assets/f1394c7e-8a3d-4fd5-8d66-587cd812fdde" />

4. Now we need to route traffic through NVA for spoke to Spoke peering.
5. Click on Route management.
<img width="1874" height="955" alt="image" src="https://github.com/user-attachments/assets/7bb93213-060b-4d5b-8f1d-3cad0f9e4ef7" />
6. Click on Create Route.
7. Fill Name, Description, Network, Route type is static route, Ip version(IPV4), desctination CIDR, Priority, Next hop, Next hop instance.

* Note: While creating observed, Route type(Static route) is disabled because Network Connectivity API should be enabled.

<img width="1910" height="918" alt="image" src="https://github.com/user-attachments/assets/8ed1c257-b0b1-439b-99a1-cd56f18952b0" />

* Search for Network Connectivity API.

<img width="1821" height="973" alt="image" src="https://github.com/user-attachments/assets/649d3068-04e7-4ff7-8d72-fffca2ff91ab" />

* Click on Enable.

<img width="1919" height="916" alt="image" src="https://github.com/user-attachments/assets/b79f1d2e-12bc-498a-83d5-bdf49a5b1cc1" />

8. 

