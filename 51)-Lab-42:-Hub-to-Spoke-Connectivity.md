Create instances in Hub, Skillup, Flip

Hub Server

<img width="1918" height="899" alt="image" src="https://github.com/user-attachments/assets/bf32d49b-279d-4f1e-8c1a-7893f011fee5" />

Flip Server

<img width="1913" height="931" alt="image" src="https://github.com/user-attachments/assets/a98e6a72-0a7c-48b4-94d3-ae4f02a5338f" />

Skillup Server

<img width="1891" height="953" alt="image" src="https://github.com/user-attachments/assets/80882c1e-05e2-4d1a-9f46-26fd45ebe4eb" />

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

## VPC Network Peering

### Hub network project to Flip Network project
1. In project picker, select Hub network project. Click on navigational Menu. Click on VPC Network. Click on VPC network peering. 

<img width="1786" height="838" alt="image" src="https://github.com/user-attachments/assets/25c7b286-b963-4307-a8af-13f768232729" />

2. Click on "Create Connection"

<img width="1752" height="815" alt="image" src="https://github.com/user-attachments/assets/97eae2fc-1fa3-4841-b6cd-facc2e35434a" />

3. Fill the details. Peering connection name. VPC-network, peered vpc network, project id, vpc network name. Click on required check boxes.

<img width="1414" height="913" alt="image" src="https://github.com/user-attachments/assets/994794cb-4a67-40db-a5f7-53d42197f05a" />

4. Click on create.

<img width="1898" height="897" alt="image" src="https://github.com/user-attachments/assets/98dbcf0a-0dd6-41d8-8ae6-c7e5921cc493" />

Peering Status is inactive because the peering is still jot done from flip to hub.

### Flip network Project to Hub network Project peering

1. In project picker, select Flip network project. Click on navigational Menu. Click on VPC Network. Click on VPC network peering. 

<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/9160dfd1-4791-49d3-bba0-9cde85e8415f" />

2. Click on "Create Connection"

<img width="1403" height="813" alt="image" src="https://github.com/user-attachments/assets/50c0d1db-8e5a-4962-9203-907859bb24eb" />

3. Fill the details. Peering connection name. VPC-network, peered vpc network, project id, vpc network name. Click on required check boxes.

<img width="1714" height="911" alt="image" src="https://github.com/user-attachments/assets/7b9b8aed-57fa-4420-bc34-5b3b4b31785f" />

4. Click on Create.

<img width="1919" height="885" alt="image" src="https://github.com/user-attachments/assets/161182f4-6425-4405-a7a8-1a3281f3897e" />

Now refresh the page and we can see the peering status be become active.

<img width="1906" height="927" alt="image" src="https://github.com/user-attachments/assets/e6b7f1f7-2745-4773-97bc-9f326adede56" />

<img width="1905" height="834" alt="image" src="https://github.com/user-attachments/assets/3026dcb8-4020-4b89-a865-3af6d0a62f03" />

