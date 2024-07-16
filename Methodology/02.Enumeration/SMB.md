<h1>Nmap</h1>

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

<h1>SMBmap</h1>

`smbmap -u administrator -p smbserver_771 -H <target>`

`smbmap -u administrator -p smbserver_771 -d . -H <target>`

`smbmap -u administrator -p smbserver_771 -L -H <target>`

`smbmap -u administrator -p smbserver_771 -r 'C$' -H <target>`

`smbmap -u administrator -p smbserver_771 -x 'ipconfig' -H <target>`

`smbmap -u administrator -p smbserver_771 --upload '/root/backdoor' 'C$\backdoor' -H <target>`

`smbmap -u administrator -p smbserver_771 --download 'C$\flag.txt' -H <target>`

<h1>Metasploit</h1>

`msf6 > use auxiliary/scanner/smb/smb_version`

`msf6 > use auxiliary/scanner/smb/smb2`

`msf6 > use auxiliary/scanner/smb/smb_enumshares`

`msf6 > use auxiliary/scanner/smb/pipe_auditor`

<h1>NMBlookup</h1>

`nmblookup -A <target>`

<h1>SMBclient</h1>

`smbclient -L -N <target>`

<h1>RPCclient</h1>

`rpcclient -U "" -N <target>`

`$> srvinfo`

`$> enumdomusers`

`$> enumdomgroups`

`$> lookupnames admin`

<h1>Enum4linux</h1>

`enum4linux -o <target>`

`enum4linux -U <target>`

`enum4linux -S <target>`

`enum4linux -G <target>`

`enum4linux -i <target>`

`enum4linux -r <target>`