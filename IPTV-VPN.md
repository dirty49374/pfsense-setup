## IPTV through Site to Site VPN

> - Establish a `wireguard` site-to-site VPN tunnel.
> - For each `wireguard` peer, configure `Allowed IPs` to `0.0.0.0/0`.
> - Remember to enable `Allow IP options` for tunnel interfaces.
> - Activate `IGMP proxy` at both sites.
> - Designate one side of tunnel as upstream and the other side as downstream.

