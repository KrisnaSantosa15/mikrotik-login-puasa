# SETTING Router

## Identitas & User

1. System -> Idenitity -> Router - Krisna
2. System -> Users -> + -> Name, Group, Pass, Confirm Pass
3. System -> Users -> + -> krisna, full, passwordkrisna, passwordkrisna

## Set IP from ISP

- IP -> Address -> + -> 10.10.10.14/24, Ether 1

## Set DNS, Gateway ISP

1. IP -> Routes -> + -> Gateway = 10.10.10.254
2. IP -> DNS -> Servers = 10.10.10.254, 192.168.10.1 + Allow Remote Request

## Determine VLAN=

1. Interface -> VLAN -> + -> Name, VLAN ID, Interface
2. Interface -> VLAN -> + -> Lab Admin, 10, ether 2
3. Interface -> VLAN -> + -> Lab Jaringan, 20, ether 2

## Setting Interface Hotspot

1. Interface -> enable Wlan1 (Checklist)
2. Interface -> wlan1 (dbl click) -> wireless -> mode,SSID
3. Interface -> wlan1 -> wireless -> ap bridge, Hotspot - Krisna

## Set Firewall

1. IP -> Firewall -> NAT -> + -> Chain, OutInterface -> Action
2. IP -> Firewall -> NAT -> + -> srcnat, ether 1 -> Action -> Masquerade

## Set IP Client

1. IP -> Address -> + -> Address, Interface
2. IP -> Address -> + -> 192.168.10.1/28, Lab admin
3. IP -> Address -> + -> 192.168.20.1/28, Lab Jaringan
4. IP -> Address -> + -> 192.168.30.1/24, Wlan1

## Set DHCP Server

- IP -> DHCP Server -> DHCP Setup -> Lab Jaringan

## Set Hotspot Server

- IP -> Hotspot -> Hotspot Setup -> next, lalu jika ada dns name masukan hotspot-krisna.com lalu next

## Configure Hotspot

- IP -> Hotspot -> User profiles -> Shared Users = 254

## Add Login page

- Files -> Drag Folder to Files Mikrotik

## Change Login Page

1. IP -> Hotspot -> Server-profiles -> hsprof1&default
2. Change HTML Directory to your login folder

## Settings Client - Server Method

1. koneksikan Ether 2 di switch ke komputer, buka pengaturan, change adapter setting
2. masukan IP 192.168.10.5
3. gateway: 192.168.10.1
4. DNS: 192.168.10.1 dan 8.8.8.8

- Oke

1. Lakukan ping ke setiap gateway
2. ping 192.168.10.1
3. ping 192.168.20.1
4. ping 192.168.30.1
5. ping 10.10.10.254

## Turn on Web Server (Buka aplikasi)

- Buka VSCODE npm run start80

## Turn Off Firewall

1. windows Defender -> firewall -> matikan semua firewall
2. Domain Network
3. Private Network
4. Public Network

## Set DNS Static

1. Masuk ke router memakai IP yang tadi diberi 192.168.10.1
2. IP -> DNS -> Static -> + -> name, type, Address
3. IP -> DNS -> Static -> + -> mymovie-app.com, A, 192.168.10.5

- OKE OKE

## Cek DNS Static

1. Buka wifi di komputer lain, koneksikan ke hotspot-krisna
2. guest, tamu
3. buka mymovie-app.com:3000 / mymovie-app.com:80
