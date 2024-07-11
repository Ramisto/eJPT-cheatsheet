# DNS

```bash
host example.org
```

```bash
whois example.org
```

[Dnsdumpster](https://dnsdumpster.com/)

[Netcraft](https://sitereport.netcraft.com/)

# Source code

Use website vacuum cleaner to read source code without interacting with the target : [HTTrack](https://www.httrack.com/page/2/fr/index.html)

```bash
sudo apt install webhttrack
```

# Google Dorks

Limit to particular domain and subdomain :  

```bash
site:example.org
```

```bash
site:*.example.org
```

Limit particular word in url :  

```bash
inurl:admin
```

```bash
inurl:auth_user_file.txt
```

```bash
inurl:passwd.txt
```

```bash
inurl:login
```

Limit particular word in title :  

```bash
intitle:index of
```

Limit particular type of file :  

```bash
filetype:xlsx
```

# Search Engines

```bash
theHarvester -d example.org -b google,linkedin
```

Look a next version of website [Wayback Machine](https://archive.org)

Look [Have i been pwned?](https://haveibeenpwned.com/)