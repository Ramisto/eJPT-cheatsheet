# Nmap

First, find open ports quickly :

```bash
nmap -Pn -sS -p- -T4 <target>
```

```bash
nmap -Pn -sU -p- -T4 <target>
```

Get more information on running services and operating system :

```bash
nmap -Pn -sS -sV -O -p445 -T4 <target>
```

And increased aggressiveness of service version detection :

```bash
nmap -Pn -sS -sA --version-intensity 8 -p445 -T4 <target>
```

# Nmap scripting engine (NSE)

List all scripts :

```bash
ls -al /sur/share/nmap/scripts/
```

```bash
ls -al /sur/share/nmap/scripts/ | grep -e "mongodb"
```

Display help to specific script :

```bash
nmap --script-help=mongodb-databases
```

Execute scripts :

```bash
nmap -sS -sV -sC -p- -T4 <target>
```

```bash
nmap -sS -sV --script=mongo-databases -p 6421 -T4 <target>
```

# Nmap Ouput Formats

Normal format :

```bash
nmap -oN output.txt
```

XML format :

```bash
nmap-oX output.xml
```

GREP format :

```bash
nmap -oG output.txt
```

# Import nmap XML file in Metasploit Framework

```bash
service postgresql start
```

```bash
msfconsole
msf6 > workspace -a pentest-1
msf6 > db_import output.xml
msf6 > hosts
msf6 > services
```

# Use Nmap in Metasploit Framework

```bash
msf6 > db_nmap -Pn -sS -A <target>
msf6 > hosts
msf6 > services
```