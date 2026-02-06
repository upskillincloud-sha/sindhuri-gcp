## Make VM as NVA

* Log in to the server.
* Now give the below commands to make the VM as NVA.
* sudo sysctl -w net.ipv4.ip_forward=1
* Make it permanent across reboots:
echo &quot;net.ipv4.ip_forward = 1&quot; | sudo tee -a /etc/sysctl.conf
* Verify it&#39;s enabled:
cat /proc/sys/net/ipv4/ip_forward
Should output: 1

### Configure iptables on Hub-VM
Still on Hub-VM (same SSH session), run these commands:
1. Accept forwarding from Spoke to Spoke2:
sudo iptables -A FORWARD -s 172.17.0.0/24 -d 172.18.0.0/24 -j ACCEPT
2. Accept forwarding from Spoke2 to Spoke:
sudo iptables -A FORWARD -s 172.18.0.0/24 -d 172.17.0.0/24 -j ACCEPT
3. Allow established connections:
sudo iptables -A FORWARD -m state --state ESTABLISHED,RELATED -j ACCEPT
4. First we have to update the package list:
sudo apt-get update
5. Install iptables-persistent to save rules:
sudo apt-get install iptables-persistent -y
When prompted during installation:
&quot;Save current IPv4 rules?&quot; → Select Yes (press Tab to highlight Yes, then Enter)
&quot;Save current IPv6 rules?&quot; → Select Yes
6. Save the iptables rules:
sudo netfilter-persistent save
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

