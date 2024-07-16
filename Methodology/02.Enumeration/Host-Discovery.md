<h1>ICMP</h1>

```bash
ping <target>
```

```bash
fping -a -g <target> 2>/dev/null
```

<h1>ARP</h1>

```bash
netdiscover -i eth0 -r <target>
```

<h1>Nmap (ping scan)</h1>

```bash
nmap -sn <target>
```

```bash
nmap -sn <target> --send-ip
```

```bash
nmap -sn -iL targets.txt
```