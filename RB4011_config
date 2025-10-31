# 2025-10-31 10:02:33 by RouterOS 7.20.2
# software id = 8PC5-3AVD
#
# model = RB4011iGS+
# serial number = 968A09DB9E44
/interface bridge
add admin-mac=BE:D6:E1:3E:04:AB auto-mac=no name=Guest-Network \
    port-cost-mode=short
add name=IoT port-cost-mode=short
add admin-mac=B8:69:F4:99:4D:CB auto-mac=no name=Private-Lan port-cost-mode=\
    short
/interface ethernet
set [ find default-name=ether1 ] comment=4G name="ether1(LTE)"
set [ find default-name=ether2 ] comment=Modem name="ether2(VDSL)"
set [ find default-name=ether3 ] disabled=yes
set [ find default-name=ether4 ] disabled=yes
set [ find default-name=ether5 ] comment="Guest terminal"
set [ find default-name=ether7 ] disabled=yes
set [ find default-name=ether8 ] disabled=yes
set [ find default-name=ether10 ] poe-priority=0
set [ find default-name=sfp-sfpplus1 ] disabled=yes
/interface wireguard
add comment=back-to-home-vpn listen-port=39885 mtu=1420 name=back-to-home-vpn
add listen-port=51820 mtu=1420 name=surfshark
/caps-man configuration
add channel.band=2ghz-b/g/n .control-channel-width=20mhz .reselect-interval=\
    12m .tx-power=17 country=greece datapath.arp=enabled .bridge=\
    Guest-Network .local-forwarding=no disconnect-timeout=3s distance=indoors \
    installation=indoor mode=ap name=Guest ssid=Free-WiFi
add channel.band=2ghz-b/g/n .control-channel-width=20mhz .skip-dfs-channels=\
    yes .tx-power=17 country=greece datapath.arp=enabled .bridge=Private-Lan \
    .client-to-client-forwarding=yes .local-forwarding=yes \
    disconnect-timeout=3s distance=indoors installation=indoor name=\
    Private-Lan security.authentication-types=wpa2-psk .encryption=aes-ccm \
    ssid=Syndicate
add channel.band=2ghz-b/g/n .control-channel-width=20mhz .reselect-interval=\
    12m .tx-power=17 country=greece datapath.arp=enabled .bridge=IoT \
    .client-to-client-forwarding=yes .local-forwarding=no disconnect-timeout=\
    3s distance=indoors installation=indoor mode=ap name=IoT \
    security.authentication-types=wpa2-psk .encryption=aes-ccm ssid=IoT
/caps-man interface
add configuration=Private-Lan disabled=no l2mtu=1600 mac-address=\
    74:4D:28:D5:5C:6F master-interface=none name=Attic-1 radio-mac=\
    74:4D:28:D5:5C:6F radio-name=744D28D55C6F
add configuration=Guest disabled=no l2mtu=1600 mac-address=76:4D:28:D5:5C:6F \
    master-interface=Attic-1 name=Attic-1-1 radio-mac=00:00:00:00:00:00 \
    radio-name=764D28D55C6F
add configuration=IoT disabled=no l2mtu=1600 mac-address=76:4D:28:D5:5C:70 \
    master-interface=Attic-1 name=Attic-1-2 radio-mac=00:00:00:00:00:00 \
    radio-name=764D28D55C70
add configuration=Private-Lan disabled=no l2mtu=1600 mac-address=\
    B8:69:F4:AA:CE:1E master-interface=none name=Balcony-1 radio-mac=\
    B8:69:F4:AA:CE:1E radio-name=B869F4AACE1E
add configuration=Guest disabled=no l2mtu=1600 mac-address=BA:69:F4:AA:CE:1E \
    master-interface=Balcony-1 name=Balcony-1-1 radio-mac=00:00:00:00:00:00 \
    radio-name=BA69F4AACE1E
add configuration=IoT disabled=no l2mtu=1600 mac-address=BA:69:F4:AA:CE:1F \
    master-interface=Balcony-1 name=Balcony-1-2 radio-mac=00:00:00:00:00:00 \
    radio-name=BA69F4AACE1F
add configuration=Private-Lan disabled=no l2mtu=1600 mac-address=\
    74:4D:28:19:27:34 master-interface=none name=LivingRoom-1 radio-mac=\
    74:4D:28:19:27:34 radio-name=744D28192734
add configuration=Guest disabled=no l2mtu=1600 mac-address=76:4D:28:19:27:34 \
    master-interface=LivingRoom-1 name=LivingRoom-1-1 radio-mac=\
    00:00:00:00:00:00 radio-name=764D28192734
add configuration=IoT disabled=no l2mtu=1600 mac-address=76:4D:28:19:27:35 \
    master-interface=LivingRoom-1 name=LivingRoom-1-2 radio-mac=\
    00:00:00:00:00:00 radio-name=764D28192735
add configuration=Private-Lan disabled=no l2mtu=1600 mac-address=\
    74:4D:28:8B:F6:E2 master-interface=none name=Office-1 radio-mac=\
    74:4D:28:8B:F6:E2 radio-name=744D288BF6E2
add configuration=Guest disabled=no l2mtu=1600 mac-address=76:4D:28:8B:F6:E2 \
    master-interface=Office-1 name=Office-1-1 radio-mac=00:00:00:00:00:00 \
    radio-name=764D288BF6E2
add configuration=IoT disabled=no l2mtu=1600 mac-address=76:4D:28:8B:F6:E3 \
    master-interface=Office-1 name=Office-1-2 radio-mac=00:00:00:00:00:00 \
    radio-name=764D288BF6E3
add configuration=Private-Lan disabled=no l2mtu=1600 mac-address=\
    74:4D:28:8B:DE:25 master-interface=none name=Rack-1 radio-mac=\
    74:4D:28:8B:DE:25 radio-name=744D288BDE25
add configuration=Guest disabled=no l2mtu=1600 mac-address=76:4D:28:8B:DE:25 \
    master-interface=Rack-1 name=Rack-1-1 radio-mac=00:00:00:00:00:00 \
    radio-name=764D288BDE25
add configuration=IoT disabled=no l2mtu=1600 mac-address=76:4D:28:8B:DE:26 \
    master-interface=Rack-1 name=Rack-1-2 radio-mac=00:00:00:00:00:00 \
    radio-name=764D288BDE26
/caps-man security
add authentication-types=wpa2-psk encryption=aes-ccm name=security1
/caps-man configuration
add channel.band=5ghz-a/n/ac .control-channel-width=20mhz .reselect-interval=\
    12m .skip-dfs-channels=yes .tx-power=17 country=greece datapath.arp=\
    enabled .bridge=Private-Lan .client-to-client-forwarding=yes \
    .local-forwarding=yes disconnect-timeout=3s hw-retries=0 installation=\
    indoor mode=ap name=Dwelled-Revolver security=security1 ssid=\
    Dwelled-Revolver
/caps-man interface
add configuration=Dwelled-Revolver disabled=no l2mtu=1600 mac-address=\
    74:4D:28:D5:5C:70 master-interface=none name=Attic-2 radio-mac=\
    74:4D:28:D5:5C:70 radio-name=744D28D55C70
add configuration=Dwelled-Revolver disabled=no l2mtu=1600 mac-address=\
    74:4D:28:19:27:35 master-interface=none name=LivingRoom-2 radio-mac=\
    74:4D:28:19:27:35 radio-name=744D28192735
add configuration=Dwelled-Revolver disabled=no l2mtu=1600 mac-address=\
    74:4D:28:8B:F6:E3 master-interface=none name=Office-2 radio-mac=\
    74:4D:28:8B:F6:E3 radio-name=744D288BF6E3
add configuration=Dwelled-Revolver disabled=no l2mtu=1600 mac-address=\
    74:4D:28:8B:DE:26 master-interface=none name=Rack-2 radio-mac=\
    74:4D:28:8B:DE:26 radio-name=744D288BDE26
/interface list
add name=WAN
add name=ZeroTier
add name=LAN
/interface lte apn
set [ find default=yes ] ip-type=ipv4 use-network-apn=no
/interface wireless security-profiles
set [ find default=yes ] supplicant-identity=MikroTik
/ip hotspot user profile
set [ find default=yes ] shared-users=10
/ip pool
add name=Private-Lan ranges=192.168.88.100-192.168.88.126
add name=Guest-Network ranges=192.168.2.2-192.168.2.126
add name=IoT ranges=192.168.2.130-192.168.2.254
/ip dhcp-server
add add-arp=yes address-pool=Private-Lan always-broadcast=yes \
    insert-queue-before=bottom interface=Private-Lan lease-time=1d name=\
    Private-Lan use-reconfigure=yes
add address-pool=Guest-Network interface=Guest-Network lease-time=4h name=\
    Guest-Netwok
add address-pool=IoT interface=IoT lease-time=4h name=IoT
/ip smb users
set [ find default=yes ] disabled=yes
/port
set 0 name=serial0
set 1 name=serial1
/ppp profile
set *0 change-tcp-mss=default use-encryption=yes use-ipv6=default use-upnp=no
/queue simple
add max-limit=2M/5M name=Guest queue=pcq-upload-default/pcq-download-default \
    target=Guest-Network total-queue=default
/routing bgp template
set default disabled=no output.network=bgp-networks
/routing ospf instance
add disabled=no name=default-v2
add disabled=no name=default-v3 version=3
/routing ospf area
add disabled=yes instance=default-v2 name=backbone-v2
add disabled=yes instance=default-v3 name=backbone-v3
/routing rip instance
add name=rip-instance-4 route-gc-timeout=120 route-timeout=180 routing-table=\
    main update-interval=30
/routing table
add fib name=VPN
/zerotier
set zt1 disabled=no disabled=no
/zerotier interface
add allow-default=yes allow-global=yes allow-managed=yes disabled=no \
    instance=zt1 name=zt-cafenio network=d5e5fb653729bb5b
/caps-man access-list
add action=accept allow-signal-out-of-range=10s disabled=no interface=all \
    signal-range=-66..20 ssid-regexp=""
add action=reject allow-signal-out-of-range=10s disabled=no interface=all \
    signal-range=-120..-66 ssid-regexp=""
/caps-man manager
set ca-certificate=CAPsMAN-CA-B869F4994DC3 certificate=CAPsMAN-B869F4994DC3 \
    enabled=yes require-peer-certificate=yes upgrade-policy=\
    require-same-version
/caps-man provisioning
add action=create-enabled hw-supported-modes=gn master-configuration=\
    Private-Lan name-format=identity slave-configurations=Guest,IoT
add action=create-enabled hw-supported-modes=ac master-configuration=\
    Dwelled-Revolver name-format=identity
/certificate settings
set builtin-trust-anchors=not-trusted
/dude
set enabled=yes
/interface bridge port
add bridge=Private-Lan ingress-filtering=no interface=ether9 \
    internal-path-cost=10 path-cost=10
add bridge=Private-Lan ingress-filtering=no interface=ether10 \
    internal-path-cost=10 path-cost=10
add bridge=Guest-Network interface=ether5 internal-path-cost=10 path-cost=10
add bridge=IoT interface=ether6 internal-path-cost=10 path-cost=10
/interface bridge settings
set use-ip-firewall=yes use-ip-firewall-for-vlan=yes
/ip firewall connection tracking
set udp-timeout=10s
/ip neighbor discovery-settings
set discover-interface-list=LAN
/ip settings
set max-neighbor-entries=8192
/ipv6 settings
set max-neighbor-entries=8192 soft-max-neighbor-entries=8191
/interface detect-internet
set detect-interface-list=all
/interface l2tp-server server
set allow-fast-path=yes caller-id-type=number default-profile=default \
    keepalive-timeout=disabled max-sessions=4 use-ipsec=yes
/interface list member
add interface="ether1(LTE)" list=WAN
add interface="ether2(VDSL)" list=WAN
add interface=Private-Lan list=LAN
add interface=Guest-Network list=LAN
add interface=IoT list=LAN
add interface=zt-cafenio list=LAN
add interface=surfshark list=LAN
/interface pptp-server server
# PPTP connections are considered unsafe, it is suggested to use a more modern VPN protocol instead
set authentication=pap,chap,mschap1,mschap2 default-profile=default \
    keepalive-timeout=disabled mrru=1500
/interface sstp-server server
set authentication=mschap1,mschap2 pfs=yes port=433
/interface wireguard peers
add allowed-address=0.0.0.0/0 endpoint-address=gr-ath.prod.surfshark.com \
    endpoint-port=51820 interface=surfshark name=Greece persistent-keepalive=\
    25s public-key="bXnjQGLhuauvBMg51YIAhwX40YqNL2ImyEub5DpHaBk="
add allowed-address=0.0.0.0/0 disabled=yes endpoint-address=\
    bg-sof.prod.surfshark.com endpoint-port=51820 interface=surfshark name=\
    Bulgaria persistent-keepalive=25s public-key=\
    "LQFiCiZcPEoYasKRLbCfXp2fYYsj8wiMr/L9u6hYqSo="
add allowed-address=0.0.0.0/0 disabled=yes endpoint-address=\
    us-dal.prod.surfshark.com endpoint-port=51820 interface=surfshark name=\
    Dallas persistent-keepalive=25s public-key=\
    "0iwHQpV+rsOg38ogv4g4XMLJa51YqWY/yKWR9UEUMDk="
/ip address
add address=192.168.88.1/25 interface=Private-Lan network=192.168.88.0
add address=192.168.2.1/25 interface=Guest-Network network=192.168.2.0
add address=192.168.2.129/25 interface=IoT network=192.168.2.128
add address=10.14.0.2/16 interface=surfshark network=10.14.0.0
/ip cloud
set back-to-home-vpn=enabled ddns-enabled=yes ddns-update-interval=10m
/ip cloud back-to-home-user
add allow-lan=yes comment="Syndicate | RB4011iGS+" file-access=full name=\
    "Redmi Note 11 NFC" private-key=\
    "6Nvzk6+8y/BS9hX54XAczInAHJX4VO49P8StI1PHMWU=" public-key=\
    "fBvjNmGGQEqAV3+6QE8rdZ+1oaJPaqrCV4VVhrbjBgQ="
/ip dhcp-client
add check-gateway=ping default-route-distance=2 interface="ether1(LTE)" \
    use-peer-dns=no
add check-gateway=ping interface="ether2(VDSL)" use-peer-dns=no use-peer-ntp=\
    no
/ip dhcp-server config
set interim-update=1m
/ip dhcp-server lease
add address=192.168.88.16 always-broadcast=yes comment=Titanas mac-address=\
    74:56:3C:CF:B3:D3 server=Private-Lan
add address=192.168.88.4 mac-address=B8:69:F4:AA:CE:1C server=Private-Lan
add address=192.168.88.2 mac-address=74:4D:28:8B:F6:DD server=Private-Lan
add address=192.168.88.3 mac-address=74:4D:28:D5:5C:6D server=Private-Lan
add address=192.168.88.6 mac-address=74:4D:28:8B:DE:20 server=Private-Lan
add address=192.168.88.5 mac-address=74:4D:28:19:27:32 server=Private-Lan
add address=192.168.88.17 mac-address=14:AB:C5:69:64:96 server=Private-Lan
add address=192.168.88.20 always-broadcast=yes lease-time=1w mac-address=\
    A4:BB:6D:79:C4:F8 server=Private-Lan
add address=192.168.88.19 always-broadcast=yes comment=TVT-DVR mac-address=\
    00:18:AE:A4:C2:50 server=Private-Lan
add address=192.168.88.15 always-broadcast=yes comment=Gigabyte-Brix \
    lease-time=1w mac-address=1C:1B:0D:B6:C7:D1 server=Private-Lan
add address=192.168.88.31 always-broadcast=yes mac-address=F4:F2:6D:93:79:9F \
    server=Private-Lan
add address=192.168.88.18 mac-address=D8:3A:DD:51:53:3E server=Private-Lan
add address=192.168.88.14 comment="Titanas Wi-Fi" mac-address=\
    BC:C7:46:99:DA:94 server=Private-Lan
add address=192.168.88.22 lease-time=1w mac-address=06:DB:2D:9C:F0:49 server=\
    Private-Lan
add address=192.168.88.27 lease-time=1w mac-address=F6:36:07:21:78:4C server=\
    Private-Lan
add address=192.168.88.23 lease-time=1w mac-address=3E:23:D7:B4:96:22 server=\
    Private-Lan
add address=192.168.88.24 lease-time=1w mac-address=76:86:5E:E5:6B:63 server=\
    Private-Lan
add address=192.168.88.26 lease-time=1w mac-address=BC:24:11:24:97:CD server=\
    Private-Lan
add address=192.168.88.13 mac-address=D8:3A:DD:33:4F:4C server=Private-Lan
add address=192.168.88.50 lease-time=1w mac-address=F4:06:69:E2:C4:3A server=\
    Private-Lan
/ip dhcp-server network
add address=192.168.2.0/25 dns-server=1.1.1.1 gateway=192.168.2.1
add address=192.168.2.128/25 dns-server=1.1.1.1 gateway=192.168.2.129
add address=192.168.88.0/25 dns-server=192.168.88.1 gateway=192.168.88.1
/ip dns
set allow-remote-requests=yes servers=162.252.172.57,149.154.159.92
/ip firewall address-list
add address=192.168.88.0/25 comment=\
    "Main private LAN range for local devices and internal communication." \
    list=Private-Lan
add address=192.168.2.2-192.168.2.126 comment=\
    "Guest network range. Isolated from main LAN for security." list=Guest
add address=192.168.2.130-192.168.2.254 comment=\
    "IoT network range for smart devices, kept separate for safety." list=IoT
add address=0.0.0.0/8 comment=\
    "Invalid source IP range (RFC6890). Never routable." list=no_forward_ipv4
add address=169.254.0.0/16 comment=\
    "Link-local addresses (self-assigned IPs), not routable." list=\
    no_forward_ipv4
add address=224.0.0.0/4 comment=\
    "Multicast address range, not for unicast routing." list=no_forward_ipv4
add address=255.255.255.255 comment=\
    "Broadcast address, should not be forwarded." list=no_forward_ipv4
add address=127.0.0.0/8 comment="Loopback addresses. Only valid locally." \
    list=bad_ipv4
add address=192.0.0.0/24 comment="Reserved IP range (RFC6890)." list=bad_ipv4
add address=192.0.2.0/24 comment=\
    "Documentation range. Example addresses, not real networks." list=\
    bad_ipv4
add address=198.51.100.0/24 comment="Documentation range." list=bad_ipv4
add address=203.0.113.0/24 comment="Documentation range." list=bad_ipv4
add address=240.0.0.0/4 comment="Reserved for future use." list=bad_ipv4
add address=0.0.0.0/8 comment="Non-global, invalid for routing." list=\
    not_global_ipv4
add address=10.0.0.0/8 comment="Private network range (RFC1918)." list=\
    not_global_ipv4
add address=100.64.0.0/10 comment="Shared address space for ISPs (RFC6598)." \
    list=not_global_ipv4
add address=169.254.0.0/16 comment="Link-local addresses (RFC3927)." list=\
    not_global_ipv4
add address=172.16.0.0/12 comment="Private network range (RFC1918)." list=\
    not_global_ipv4
add address=192.0.0.0/29 comment="Reserved protocol addresses." list=\
    not_global_ipv4
add address=192.168.0.0/16 comment="Private network range (RFC1918)." list=\
    not_global_ipv4
add address=198.18.0.0/15 comment="Benchmarking range (RFC2544)." list=\
    not_global_ipv4
add address=255.255.255.255 comment="Broadcast address." list=not_global_ipv4
add address=224.0.0.0/4 comment="Multicast sources invalid as senders." list=\
    bad_src_ipv4
add address=255.255.255.255 comment="Broadcast sources invalid." list=\
    bad_src_ipv4
add address=0.0.0.0/8 comment="Invalid destination." list=bad_dst_ipv4
add address=224.0.0.0/4 comment="Multicast destination invalid." list=\
    bad_dst_ipv4
add address=192.168.10.0/24 comment=\
    "Remote Intale Network reachable via VPN or site-to-site connection." \
    list="Intale Network"
/ip firewall filter
add action=accept chain=forward in-interface-list=ZeroTier
add action=accept chain=input in-interface-list=ZeroTier
add action=accept chain=input comment="accept established,related" \
    connection-state=established,related
add action=accept chain=forward comment="accept established,related" \
    connection-state=established,related
add action=accept chain=input comment="allow ICMP" in-interface-list=WAN \
    protocol=icmp
add action=fasttrack-connection chain=forward comment=\
    "fast-track for established,related" connection-state=established,related \
    hw-offload=yes
add action=accept chain=forward dst-address-list="Intale Network" \
    src-address-list=Private-Lan
add action=drop chain=input connection-state=invalid
add action=drop chain=forward connection-state=invalid
add action=drop chain=forward comment=\
    "drop access to clients behind NAT from WAN" connection-nat-state=!dstnat \
    connection-state=new in-interface-list=WAN
add action=accept chain=input comment="defconf: accept ICMP after RAW" \
    protocol=icmp
add action=accept chain=input comment=\
    "defconf: accept established,related,untracked" connection-state=\
    established,related,untracked
add action=accept chain=forward comment=\
    "defconf: accept all that matches IPSec policy" ipsec-policy=in,ipsec
add action=fasttrack-connection chain=forward comment="defconf: fasttrack" \
    connection-state=established,related hw-offload=yes
add action=drop chain=forward comment="defconf: drop invalid" \
    connection-state=invalid
add action=drop chain=input comment="defconf: drop all not coming from LAN" \
    in-interface-list=!LAN
add action=drop chain=forward comment=\
    "defconf:  drop all from WAN not DSTNATed" connection-nat-state=!dstnat \
    connection-state=new in-interface-list=WAN
add action=drop chain=forward comment="defconf: drop bad forward IPs" \
    src-address-list=no_forward_ipv4
add action=drop chain=forward comment="defconf: drop bad forward IPs" \
    dst-address-list=no_forward_ipv4
add action=drop chain=forward out-interface-list=LAN src-address-list=Guest
add action=drop chain=forward out-interface-list=LAN src-address-list=IoT
add action=drop chain=forward out-interface-list=LAN src-address-list=\
    VMs-Block
add action=accept chain=forward
add action=drop chain=forward comment="Block outside UDP DNS" dst-port=53 \
    out-interface=!surfshark out-interface-list=all protocol=udp src-address=\
    192.168.88.0/25
add action=drop chain=forward comment="Block outside TCP DNS" dst-port=53 \
    out-interface=!surfshark protocol=tcp src-address=192.168.88.0/25
add action=drop chain=forward comment="Force all LAN through VPN" \
    routing-mark=!VPN src-address=192.168.88.0/25
add action=drop chain=input comment="block everything else" \
    in-interface-list=WAN
/ip firewall mangle
add action=accept chain=prerouting comment="LAN-to-LAN stays local" \
    dst-address-list=Private-Lan src-address-list=Private-Lan
add action=accept chain=prerouting comment="ZeroTier stays local" \
    dst-address=192.168.88.128/25 src-address=192.168.88.0/25
add action=accept chain=prerouting comment="ZeroTier stays local" \
    dst-address=192.168.10.0/24 src-address=192.168.88.0/25
add action=accept chain=prerouting comment="ZeroTier stays local" \
    dst-address=192.168.51.0/24 src-address=192.168.88.0/25
add action=change-mss chain=forward comment="Clamp MSS for Surfshark" \
    new-mss=1360 out-interface=surfshark passthrough=no protocol=tcp \
    tcp-flags=syn
add action=mark-routing chain=prerouting comment="Force LAN DNS via VPN UDP" \
    dst-port=53 new-routing-mark=VPN protocol=udp src-address=192.168.88.0/25
add action=mark-routing chain=prerouting comment="Force LAN DNS via VPN TCP" \
    dst-port=53 new-routing-mark=VPN protocol=tcp src-address=192.168.88.0/25
add action=mark-routing chain=output comment=\
    "Mark router\E2\80\99s own DNS queries" dst-port=53 new-routing-mark=VPN \
    protocol=tcp
add action=mark-routing chain=output comment=\
    "Mark router\E2\80\99s own DNS queries" dst-port=53 new-routing-mark=VPN \
    protocol=udp
add action=mark-routing chain=prerouting comment=\
    "Send Private LAN through Surfshark" new-routing-mark=VPN src-address=\
    192.168.88.0/25
/ip firewall nat
add action=masquerade chain=srcnat comment="masquerade LAN networks" \
    ipsec-policy=out,none out-interface-list=WAN
add action=accept chain=srcnat comment=\
    "defconf: accept all that matches IPSec policy" ipsec-policy=out,ipsec
add action=redirect chain=dstnat comment=\
    "Redirect LAN DNS through router VPN" dst-port=53 protocol=udp \
    src-address=192.168.88.0/25 to-ports=53
add action=redirect chain=dstnat comment=\
    "Redirect LAN DNS through router VPN" dst-port=53 protocol=tcp \
    src-address=192.168.88.0/25 to-ports=53
add action=masquerade chain=srcnat comment="NAT via Surfshark" out-interface=\
    surfshark
/ip firewall raw
add action=accept chain=prerouting comment=\
    "defconf: enable for transparent firewall"
add action=accept chain=prerouting comment="defconf: accept DHCP discover" \
    dst-address=255.255.255.255 dst-port=67 in-interface-list=LAN protocol=\
    udp src-address=0.0.0.0 src-port=68
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    src-address-list=bad_ipv4
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    dst-address-list=bad_ipv4
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    src-address-list=bad_src_ipv4
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    dst-address-list=bad_dst_ipv4
add action=drop chain=prerouting comment="defconf: drop non global from WAN" \
    in-interface-list=WAN src-address-list=not_global_ipv4
add action=drop chain=prerouting comment=\
    "defconf: drop forward to local lan from WAN" dst-address-list=\
    Private-Lan in-interface-list=WAN
add action=drop chain=prerouting comment=\
    "defconf: drop forward to local lan from WAN" dst-address-list=Guest \
    in-interface-list=WAN
add action=drop chain=prerouting comment=\
    "defconf: drop forward to local lan from WAN" dst-address-list=iot \
    in-interface-list=WAN
add action=drop chain=prerouting comment=\
    "defconf: drop local if not from default IP range" in-interface-list=LAN \
    src-address-list=!Private-Lan
add action=drop chain=prerouting comment=\
    "defconf: drop local if not from default IP range" in-interface-list=LAN \
    src-address-list=!Guest
add action=drop chain=prerouting comment=\
    "defconf: drop local if not from default IP range" in-interface-list=LAN \
    src-address-list=!iot
add action=drop chain=prerouting comment="defconf: drop bad UDP" port=0 \
    protocol=udp
add action=jump chain=prerouting comment="defconf: jump to ICMP chain" \
    jump-target=icmp4 protocol=icmp
add action=jump chain=prerouting comment="defconf: jump to TCP chain" \
    jump-target=bad_tcp protocol=tcp
add action=accept chain=prerouting comment=\
    "defconf: accept everything else from LAN" in-interface-list=LAN
add action=accept chain=prerouting comment=\
    "defconf: accept everything else from WAN" in-interface-list=WAN
add action=drop chain=prerouting comment="defconf: drop the rest"
add action=drop chain=bad_tcp comment="defconf: TCP flag filter" protocol=tcp \
    tcp-flags=!fin,!syn,!rst,!ack
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=fin,syn
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=fin,rst
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=fin,!ack
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=fin,urg
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=syn,rst
add action=drop chain=bad_tcp comment=defconf protocol=tcp tcp-flags=rst,urg
add action=drop chain=bad_tcp comment="defconf: TCP port 0 drop" port=0 \
    protocol=tcp
add action=accept chain=icmp4 comment="defconf: echo reply" icmp-options=0:0 \
    limit=5,10:packet protocol=icmp
add action=accept chain=icmp4 comment="defconf: net unreachable" \
    icmp-options=3:0 protocol=icmp
add action=accept chain=icmp4 comment="defconf: host unreachable" \
    icmp-options=3:1 protocol=icmp
add action=accept chain=icmp4 comment="defconf: protocol unreachable" \
    icmp-options=3:2 protocol=icmp
add action=accept chain=icmp4 comment="defconf: port unreachable" \
    icmp-options=3:3 protocol=icmp
add action=accept chain=icmp4 comment="defconf: fragmentation needed" \
    icmp-options=3:4 protocol=icmp
add action=accept chain=icmp4 comment="defconf: echo" icmp-options=8:0 limit=\
    5,10:packet protocol=icmp
add action=accept chain=icmp4 comment="defconf: time exceeded " icmp-options=\
    11:0-255 protocol=icmp
add action=drop chain=icmp4 comment="defconf: drop other icmp" protocol=icmp
/ip firewall service-port
set rtsp disabled=no
/ip hotspot profile
set [ find default=yes ] login-by=http-chap,http-pap,trial,mac-cookie
/ip hotspot service-port
set ftp disabled=yes
/ip ipsec policy
set 0 proposal=*6
/ip ipsec profile
set [ find default=yes ] dh-group=modp2048 dpd-interval=2m \
    dpd-maximum-failures=5 enc-algorithm=aes-256 hash-algorithm=sha256
/ip kid-control
add fri=0s-1d mon=0s-1d name=system-dummy sat=0s-1d sun=0s-1d thu=0s-1d tue=\
    0s-1d tur-fri=0s-1d tur-mon=0s-1d tur-sat=0s-1d tur-sun=0s-1d tur-thu=\
    0s-1d tur-tue=0s-1d tur-wed=0s-1d wed=0s-1d
/ip route
add dst-address=0.0.0.0/0 gateway=surfshark routing-table=VPN
add disabled=no dst-address=162.252.172.57/32 gateway=surfshark \
    routing-table=VPN suppress-hw-offload=no
add disabled=no distance=1 dst-address=149.154.159.92/32 gateway=surfshark \
    routing-table=VPN scope=30 suppress-hw-offload=no target-scope=10
/ip service
set ftp disabled=yes
set ssh address=192.168.88.0/25,192.168.88.128/25,192.168.51.0/24
set telnet disabled=yes
set www address=192.168.88.0/25,192.168.88.128/25,192.168.51.0/24 disabled=\
    yes
set www-ssl certificate=CAP-744D288BDE20
set winbox address=192.168.88.0/25,192.168.88.128/25,192.168.51.0/24
set api disabled=yes
set api-ssl disabled=yes
/ip smb shares
set [ find default=yes ] directory=/pub
/ip ssh
set strong-crypto=yes
/ip upnp
set enabled=yes show-dummy-rule=no
/ipv6 firewall address-list
add address=fe80::/16 list=allowed
add address=ff02::/16 comment=multicast list=allowed
add address=fe80::/10 comment="defconf: RFC6890 Linked-Scoped Unicast" list=\
    no_forward_ipv6
add address=ff00::/8 comment="defconf: multicast" list=no_forward_ipv6
add address=::1/128 comment="defconf: RFC6890 lo" list=bad_ipv6
add address=::ffff:0.0.0.0/96 comment="defconf: RFC6890 IPv4 mapped" list=\
    bad_ipv6
add address=2001::/23 comment="defconf: RFC6890" list=bad_ipv6
add address=2001:db8::/32 comment="defconf: RFC6890 documentation" list=\
    bad_ipv6
add address=2001:10::/28 comment="defconf: RFC6890 orchid" list=bad_ipv6
add address=::/96 comment="defconf: ipv4 compat" list=bad_ipv6
add address=100::/64 comment="defconf: RFC6890 Discard-only" list=\
    not_global_ipv6
add address=2001::/32 comment="defconf: RFC6890 TEREDO" list=not_global_ipv6
add address=2001:2::/48 comment="defconf: RFC6890 Benchmark" list=\
    not_global_ipv6
add address=fc00::/7 comment="defconf: RFC6890 Unique-Local" list=\
    not_global_ipv6
add address=::/128 comment="defconf: unspecified" list=bad_dst_ipv6
add address=::/128 comment="defconf: unspecified" list=bad_src_ipv6
add address=ff00::/8 comment="defconf: multicast" list=bad_src_ipv6
/ipv6 firewall filter
add action=accept chain=input comment="allow established and related" \
    connection-state=established,related
add action=accept chain=input comment="accept ICMPv6" protocol=icmpv6
add action=accept chain=input comment="defconf: accept UDP traceroute" port=\
    33434-33534 protocol=udp
add action=accept chain=input comment=\
    "accept DHCPv6-Client prefix delegation." dst-port=546 protocol=udp \
    src-address=fe80::/16
add action=accept chain=input comment=\
    "accept DHCPv6-Client prefix delegation." dst-port=546 protocol=udp \
    src-address=fe80::/16
add action=accept chain=input comment="allow allowed addresses" \
    src-address-list=allowed
add action=drop chain=input
add action=accept chain=input comment="defconf: accept ICMPv6 after RAW" \
    protocol=icmpv6
add action=accept chain=input comment=\
    "defconf: accept established,related,untracked" connection-state=\
    established,related,untracked
add action=accept chain=input comment="defconf: accept UDP traceroute" port=\
    33434-33534 protocol=udp
add action=accept chain=input comment=\
    "defconf: accept DHCPv6-Client prefix delegation." dst-port=546 protocol=\
    udp src-address=fe80::/16
add action=accept chain=input comment="defconf: accept IKE" dst-port=500,4500 \
    protocol=udp
add action=accept chain=input comment="defconf: accept IPSec AH" protocol=\
    ipsec-ah
add action=accept chain=input comment="defconf: accept IPSec ESP" protocol=\
    ipsec-esp
add action=drop chain=input comment="defconf: drop all not coming from LAN" \
    in-interface-list=!LAN
add action=accept chain=forward comment=\
    "defconf: accept established,related,untracked" connection-state=\
    established,related,untracked
add action=drop chain=forward comment="defconf: drop invalid" \
    connection-state=invalid
add action=drop chain=forward comment="defconf: drop bad forward IPs" \
    src-address-list=no_forward_ipv6
add action=drop chain=forward comment="defconf: drop bad forward IPs" \
    dst-address-list=no_forward_ipv6
add action=drop chain=forward comment="defconf: rfc4890 drop hop-limit=1" \
    hop-limit=equal:1 protocol=icmpv6
add action=accept chain=forward comment="defconf: accept ICMPv6 after RAW" \
    protocol=icmpv6
add action=accept chain=forward comment="defconf: accept HIP" protocol=139
add action=accept chain=forward comment="defconf: accept IKE" dst-port=\
    500,4500 protocol=udp
add action=accept chain=forward comment="defconf: accept AH" protocol=\
    ipsec-ah
add action=accept chain=forward comment="defconf: accept ESP" protocol=\
    ipsec-esp
add action=accept chain=forward comment=\
    "defconf: accept all that matches IPSec policy" ipsec-policy=in,ipsec
/ipv6 firewall raw
add action=accept chain=prerouting comment=\
    "defconf: enable for transparent firewall" disabled=yes
add action=accept chain=prerouting comment="defconf: RFC4291, section 2.7.1" \
    dst-address=ff02::1:ff00:0/104 icmp-options=135 protocol=icmpv6 \
    src-address=::/128
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    src-address-list=bad_ipv6
add action=drop chain=prerouting comment="defconf: drop bogon IP's" \
    dst-address-list=bad_ipv6
add action=drop chain=prerouting comment=\
    "defconf: drop packets with bad SRC ipv6" src-address-list=bad_src_ipv6
add action=drop chain=prerouting comment=\
    "defconf: drop packets with bad dst ipv6" dst-address-list=bad_dst_ipv6
add action=drop chain=prerouting comment="defconf: drop non global from WAN" \
    in-interface-list=WAN src-address-list=not_global_ipv6
add action=jump chain=prerouting comment="defconf: jump to ICMPv6 chain" \
    jump-target=icmp6 protocol=icmpv6
add action=accept chain=prerouting comment=\
    "defconf: accept local multicast scope" dst-address=ff02::/16
add action=drop chain=prerouting comment=\
    "defconf: drop other multicast destinations" dst-address=ff00::/8
add action=accept chain=prerouting comment=\
    "defconf: accept everything else from WAN" in-interface-list=WAN
add action=accept chain=prerouting comment=\
    "defconf: accept everything else from LAN" in-interface-list=LAN
add action=drop chain=prerouting comment="defconf: drop the rest"
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 drop ll if hop-limit!=255" dst-address=fe80::/10 \
    hop-limit=not-equal:255 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: dst unreachable" \
    icmp-options=1:0-255 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: packet too big" icmp-options=\
    2:0-255 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: limit exceeded" icmp-options=\
    3:0-1 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: bad header" icmp-options=\
    4:0-2 protocol=icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: Mobile home agent address discovery" icmp-options=144:0-255 \
    protocol=icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: Mobile home agent address discovery" icmp-options=145:0-255 \
    protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: Mobile prefix solic" \
    icmp-options=146:0-255 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: Mobile prefix advert" \
    icmp-options=147:0-255 protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: echo request limit 5,10" \
    icmp-options=128:0-255 limit=5,10:packet protocol=icmpv6
add action=accept chain=icmp6 comment="defconf: echo reply limit 5,10" \
    icmp-options=129:0-255 limit=5,10:packet protocol=icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 router solic limit 5,10 only LAN" hop-limit=equal:255 \
    icmp-options=133:0-255 in-interface-list=LAN limit=5,10:packet protocol=\
    icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 router advert limit 5,10 only LAN" hop-limit=equal:255 \
    icmp-options=134:0-255 in-interface-list=LAN limit=5,10:packet protocol=\
    icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 neighbor solic limit 5,10 only LAN" hop-limit=equal:255 \
    icmp-options=135:0-255 in-interface-list=LAN limit=5,10:packet protocol=\
    icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 neighbor advert limit 5,10 only LAN" hop-limit=\
    equal:255 icmp-options=136:0-255 in-interface-list=LAN limit=5,10:packet \
    protocol=icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 inverse ND solic limit 5,10 only LAN" hop-limit=\
    equal:255 icmp-options=141:0-255 in-interface-list=LAN limit=5,10:packet \
    protocol=icmpv6
add action=accept chain=icmp6 comment=\
    "defconf: rfc4890 inverse ND advert limit 5,10 only LAN" hop-limit=\
    equal:255 icmp-options=142:0-255 in-interface-list=LAN limit=5,10:packet \
    protocol=icmpv6
add action=drop chain=icmp6 comment="defconf: drop other icmp" protocol=\
    icmpv6
/ipv6 nd
set [ find default=yes ] advertise-dns=no disabled=yes
/routing bfd configuration
add disabled=no
/routing rule
add action=lookup routing-mark=VPN table=VPN
/snmp
set enabled=yes trap-version=2
/system clock
set time-zone-name=Europe/Athens
/system identity
set name=Syndicate
/system note
set show-at-login=no
/system resource irq rps
set sfp-sfpplus1 disabled=no
/system routerboard settings
set auto-upgrade=yes
/system scheduler
add interval=1w name=reboot on-event="/system reboot" policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
    start-time=startup
add interval=30s name=wan-failover on-event=wan-failover-policy policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
    start-time=startup
/system script
add dont-require-permissions=no name=wan-failover-policy owner=funmicra \
    policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
    source="# Persistent WAN Failover Script\
    \n:local primaryWAN \"ether2(VDSL)\";\
    \n:local backupWAN \"ether1(LTE)\";\
    \n:local checkIP \"8.8.8.8\";\
    \n:local failThreshold 3;\
    \n\
    \n# Get persistent fail count (default 0 if not set)\
    \n:global failCount\
    \n:if ([:typeof \$failCount] = nil) do={:global failCount 0}\
    \n\
    \n# Ping the target from primary WAN\
    \n:if ([/ping address=\$checkIP interface=\$primaryWAN count=3] = 0) do={\
    \n    # Failed ping\
    \n    :set failCount (\$failCount + 1);\
    \n    :log warning (\"WAN check failed \" . \$failCount . \" times\");\
    \n\
    \n    # Only switch if threshold reached\
    \n    :if (\$failCount >= \$failThreshold) do={\
    \n        /ip route set [find dst-address=0.0.0.0/0 gateway=192.168.122.1]\
    \_distance=1;\
    \n        /ip route set [find dst-address=0.0.0.0/0 gateway=192.168.8.1] d\
    istance=2;\
    \n        :log warning \"Failover: LTE is now primary route\";\
    \n    }\
    \n} else={\
    \n    # Primary WAN reachable, reset fail count\
    \n    :set failCount 0;\
    \n\
    \n    # Ensure primary WAN is preferred\
    \n    /ip route set [find dst-address=0.0.0.0/0 gateway=192.168.8.1] dista\
    nce=1;\
    \n    /ip route set [find dst-address=0.0.0.0/0 gateway=192.168.122.1] dis\
    tance=2;\
    \n    :log info \"Primary WAN (VDSL) is up. Routes restored.\";\
    \n}\
    \n"
add dont-require-permissions=no name=surfshark_VPN owner=funmicra policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source="#\
    \_=== Step 0: Remove old VPN settings (optional, avoids conflicts) ===\
    \n/interface wireguard remove [find name=surfshark]\
    \n/ip route remove [find gateway=surfshark]\
    \n/ip firewall nat remove [find out-interface=surfshark]\
    \n/ip firewall mangle remove [find new-routing-mark=VPN]\
    \n/routing table remove [find name=VPN]\
    \n\
    \n# === Step 1: Create WireGuard interface ===\
    \n/interface wireguard add name=surfshark listen-port=51820 private-key=\"\
    +GovRqiYq92jCrMPOaT55JTWZSupSh30DouxjX98eF8=\" mtu=1420\
    \n\
    \n# === Step 2: Assign VPN IP ===\
    \n/ip address add address=10.14.0.2/16 interface=surfshark\
    \n\
    \n# === Step 3: Add Surfshark peer ===\
    \n/interface wireguard peers add interface=surfshark public-key=\"bXnjQGLh\
    uauvBMg51YIAhwX40YqNL2ImyEub5DpHaBk=\" endpoint-address=bg-sof.prod.surfsh\
    ark.com endpoint-port=51820 allowed-address=0.0.0.0/0 persistent-keepalive\
    =25\
    \n\
    \n# === Step 4: Set DNS for LAN devices ===\
    \n/ip dns set servers=162.252.172.57,149.154.159.92 allow-remote-requests=\
    yes\
    \n\
    \n# === Step 5: Enable NAT for VPN traffic ===\
    \n/ip firewall nat add chain=srcnat out-interface=surfshark action=masquer\
    ade comment=\"NAT via Surfshark\"\
    \n\
    \n# === Step 6: Create a dedicated routing table for VPN ===\
    \n/routing table add name=VPN fib\
    \n\
    \n# === Step 7: Add default route in VPN table ===\
    \n/ip route add dst-address=0.0.0.0/0 gateway=surfshark routing-table=VPN\
    \n\
    \n# === Step 8: Mark LAN traffic to use VPN ===\
    \n/ip firewall mangle add chain=prerouting src-address=192.168.88.0/25 act\
    ion=mark-routing new-routing-mark=VPN comment=\"Send Private LAN through S\
    urfshark\"\
    \n\
    \n# === Step 9: Optional: verify handshake ===\
    \n/interface wireguard peers print\
    \n"
/tool e-mail
set from=<RB4011> port=587 server=smtp.gmail.com tls=yes user=\
    el.funmicra@gmail.com
/tool mac-server
set allowed-interface-list=LAN
/tool mac-server mac-winbox
set allowed-interface-list=LAN
/tool romon
set enabled=yes
/zerotier controller member
add authorized=yes ip-address=172.27.27.12 network=*2 zt-address=425a9d11d0
