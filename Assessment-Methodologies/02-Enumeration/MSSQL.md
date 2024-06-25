# Nmap

`nmap --script=ms-sql-info -p 1433 <target>`

`nmap --script=ms-sql-ntlm-info --script-args=mssql.instance-port=1433 -p 1433 <target>`