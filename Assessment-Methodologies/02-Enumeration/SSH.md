# Nmap

`nmap --script ssh2-enum-algos -p 22 192.244.143.3`

`nmap --script ssh-hostkey --script-args ssh_hotkey=full -p 22 192.244.143.3`

`nmap --script ssh2-auth-methods --script-args="ssh.user=student" -p 22 192.244.143.3`

# Netcat 

`nc 192.244.143.3 22`

