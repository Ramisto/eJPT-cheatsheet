# Options

-f : The -f option causes the requested scan (including host discovery scans) to use tiny fragmented IP packets. The idea is to split up the TCP header over several packets to make it harder for packet filters, intrusion detection systems, and other annoyances to detect what you are doing.

-D : Causes a decoy scan to be performed, which makes it appear to the remote host that the host(s) you specify as decoys are scanning the target network too. 

-g : Simply provide a port number and Nmap will send packets from that port where possible.

--host-timeout : Specify --host-timeout with the maximum amount of time you are willing to wait.

--scan-delay : This option causes Nmap to wait at least the given amount of time between each probe it sends to a given host.

# Firewall detect

ACK packets for detect filtered or unfiltered ports :
`nmap -sA -p80,445,3389 192.31.214.3`

# IDS Evasion

Fragment packets : 
`nmap -f -p- 192.31.214.3`

Decoy scan with other IPs : 
`nmap -D <decoy-ip-1, decoy-ip-2> -p- 192.31.214.3`

Source port scan : 
`nmap -g <source-port> -p- 192.31.214.3`

 Sneaky mode :
 `nmap -T1 192.31.214.3`
  
  Paranoid mode : 
  `nmap -T0 192.31.214.3`
	

# Optimizing nmap

Specify 30m to ensure that Nmap doesn't waste more than half an hour on a single host :
`nmap --host-timeout 30m 192.31.214.3`

 A --scan-delay of 1s will keep Nmap at that slow rate : 
`nmap --scan-delay 1s 192.31.214.3`
 

  