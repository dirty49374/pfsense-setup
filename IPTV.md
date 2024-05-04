## Step 1. Configure IGMP Proxy

### Navigate to Services > IGMP Proxy

> - Check `Enable IGMP`
> - Click on `Save`

### Add upstream interface

> - Click on the `Add` button
> - For `Interface`, choose the relevant interface (e.g., WAN)
> - For `Type`, choose Upstream Interface
> - For `Networks`, input the IPTV source addresses or 0.0.0.0/0 (For SK Broadband - 192.168.140.0/24, 192.168.121.0/24, 192.168.126.0/24, check Status>System Logs>Routing or use Wireshark)
> - Click on `Save`


### Add downstream interface


> - Click on the `Add` button
> - For `Interface`, choose the relevant interface (e.g., `VLAN_IPTV`)
> - For `Type`, choose Downstream Interface
For Networks, input the network of the selected interface (e.g., 10.0.1.0/24)
> - Click on `Save`



## Step 2. Configure Allow IP Options Rules 

While IGMP packets are managed by the IGMP proxy daemon process, multicast video packets are routed by the OS kernel. To enable the kernel to route multicast packets, we need to enable "Allow IP Options" for these interfaces.

For a basic setup, for each upstream and downstream interface:

> - Add Rule: IPV4, UDP, Any->224.0.0.0/4, Any Port, Advanced>Allow IP Options, `Save`




