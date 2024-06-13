# ICMP

`ping 192.168.1.1`

`fping -a -g 192.168.1.0/24 2>/dev/null`


# ARP

`netdiscover -i eth0 -r 192.168.1.0/24`

# Nmap (ping scan)

`nmap -sn 192.168.1.0/24`

`nmap -sn 192.168.1.0/24 --send-ip`

`nmap -sn -iL targets.txt`