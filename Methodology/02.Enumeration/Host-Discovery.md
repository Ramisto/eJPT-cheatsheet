# ICMP

```bash
ping <target>
```

```bash
fping -a -g <target> 2>/dev/null
```

# ARP

```bash
netdiscover -i eth0 -r <target>
```

# Nmap (ping scan)

```bash
nmap -sn <target>
```

```bash
nmap -sn <target> --send-ip
```

```bash
nmap -sn -iL targets.txt
```