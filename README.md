# Hackathon
Norway Hackathon Lab Details for NSX related exercises

NSX Segments

    hol-db
        Connected Gateway hol-gw
        Transport Zone TZ-HOL-Overlay | Overlay
        Subnets 172.16.15.1/24

    hol-app
        Connected Gateway hol-gw
        Transport Zone TZ-HOL-Overlay | Overlay
        Subnets 172.16.16.1/24

    hol-web
        Connected Gateway hol-gw
        Transport Zone TZ-HOL-Overlay | Overlay
        Subnets 172.16.17.1/24

Aria Automation Network Profiles

    DB NSX Network
        Account / Region Private Cloud / RegionA01
        Name DB NSX Network
        Capabilities net:nsx workload:db
        Networks hol-db
        Domain corp.vmbeans.com
        IPv4 CIDR 172.16.15.0/24
        IPv4 default gateway 172.16.15.1
        DNS servers 192.168.110.10
        DNS search domains corp.vmbeans.com
        IP Ranges 
        Source Internal
        Name 172.16.15.1/24
        Network hol-db
        Start IP address 172.16.15.11
        End IP address 172.16.15.50
        Network Policies
        Isolation policy On-demand network
        Transport Zone nsx-overlay-transportzone
        External network hol-dev
        Tier-0 logical router hol-gw
        Edge cluster hol-edge-cluster
        Source internal
        CIDR 172.16.20.0/24
        Subnet size /28
        IP range assignment Static and DHCP
        The network inside of the Network Profile needs DNS domain, DNS server and DNS search path specified

    App NSX Network
        Account / Region Private Cloud / RegionA01
        Name App NSX Network
        Capabilities net:nsx workload:app
        Networks hol-app
        Domain corp.vmbeans.com
         IPv4 CIDR 172.16.16.0/24
        IPv4 default gateway 172.16.16.1
        DNS servers 192.168.110.10
        DNS search domains corp.vmbeans.com
        IP Ranges 
        Source Internal
        Name 172.16.16.1/24
        Network hol-app
        Start IP address 172.16.16.11
        End IP address 172.16.16.50
        Network Policies
        Isolation policy On-demand network
        Transport Zone nsx-overlay-transportzone
        External network hol-dev
        Tier-0 logical router hol-gw
        Edge cluster hol-edge-cluster
        Source internal
        CIDR 172.16.20.0/24
        Subnet size /28
        IP range assignment Static and DHCP
        The network inside of the Network Profile needs DNS domain, DNS server and DNS search path specified

    Web NSX Network
        Account / Region Private Cloud / RegionA01
        Name Web NSX Network
        Capabilities net:nsx workload:web
        Networks hol-web
        Domain corp.vmbeans.com
        IPv4 CIDR 172.16.17.0/24
        IPv4 default gateway 172.16.17.1
        DNS servers 192.168.110.10
        DNS search domains corp.vmbeans.com
        IP Ranges 
        Source Internal
        Name 172.16.17.1/24
        Network hol-web
        Start IP address 172.16.17.11
        End IP address 172.16.17.50
        Network Policies
        Isolation policy On-demand network
        Transport Zone nsx-overlay-transportzone
        External network hol-dev
        Tier-0 logical router hol-gw
        Edge cluster hol-edge-cluster
        Source internal
        CIDR 172.16.20.0/24
        Subnet size /28
        IP range assignment Static and DHCP
        The network inside of the Network Profile needs DNS domain, DNS server and DNS search path specified

Aria Automation Tags

    workload:app
    workload:db
    workload:web

NSX T1 Gateway

    Name hol-3-tier-t1
    T0 Gateway hol-gw
    Edge Cluster hol-edge-cluster
    Route Advertisement All options selected

NSX Load Balancer

    hol-3-tier
    Small



![image](https://github.com/kskilling/Hackathon/assets/48841085/fa421c0c-3bec-4752-b1f7-24a2eee9fbcf)
