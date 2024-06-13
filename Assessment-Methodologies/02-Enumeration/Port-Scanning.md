# Options

Paranoid mode : T0
Sneaky mode : T1
Fragile mode : T2
Agressive mode : T4
Insane mode : T5

-Pn : skip host discovery
-F : fast scan

-O : OS detection
-sV : Services versions
-sC : Default NSE scripts
-A : Combining parameters -O -sV -sC and --traceroute

-sT : TCP packets
-sU : UDP packets
-sS : SYN packets
-sA : ACK packets

-PS : SYN/ACK host discovery

-p- : all ports

# Combine options

1) First, find open ports quickly : 
`nmap -Pn -sS -p- -T4 192.31.214.3`
`nmap -Pn -sU -p- -T4 192.31.214.3`

2) Get more information on running services and operating system : 
`nmap -Pn -sS -A -p445 -T4 192.31.214.3`

3) And increased aggressiveness of service version detection :
`nmap -Pn -sS -sA --version-intensity 8 -p445 -T4 192.31.214.3`

# Nmap scripting engine (NSE)

List all scripts : 
`ls -al /sur/share/nmap/scripts/`
`ls -al /sur/share/nmap/scripts/ | grep -e "mongodb"`

Display help to specific script : 
`nmap --script-help=mongodb-databases`

Execute scripts : 
`nmap -sS -sV -sC -p- -T4 192.31.214.3`
`nmap -sS -sV --script mongo-databases -p6421 -T4 192.31.214.3`

# Nmap Ouput Formats

Normal format : 
`nmap -oN output.txt`

XML format : 
`nmap-oX output.xml`

GREP format : 
`nmap -oG output.txt`

# Import nmap XML file in Metasploit Framework

`service postgresql start`
`msfconsole`
`msf6 > workspace -a pentest-1`
`msf6 > workspace`
`msf6 > db_status`
`msf6 > db_import output.xml`
`msf6 > hosts`
`msf6 > services`

# Use Nmap in Metasploit Framework

`msf6 > db_nmap -Pn -sS -A 10.4.19.132`
`msf6 > hosts`
`msf6 > services`
