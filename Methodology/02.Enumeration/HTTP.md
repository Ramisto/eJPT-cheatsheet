# Nmap

```bash
nmap -sV --script=http-enum -p80 <target>
```

```bash
nmap -sV --script=http-headers -p80 <target>
```

```bash
nmap -sV --script=banner -p80 <target>
```

```bash
nmap -sV --script=http-headers --script-args http-methods.url-path=/webdav/ -p80 <target>
```

```bash
nmap -sV --script=http-webdav-scan --script-args http-methods.url-path=/webdav/ -p80 <target>
```

# Metasploit

```bash
msf6 > use auxiliary/scanner/http/http_version
```

```bash
msf6 > use auxiliary/scanner/http/brute_dirs
```

```bash
msf6 > use auxiliary/scanner/http/robots_txt
```

# HTTP fingerprint

```bash
http <target>
```

# Directory listing

```bash
dirb <target>
```

# Directories hidden from search engines

```http
https://example.org/robots.txt  
https://example.org/sitemap.xml  
https://example.org/sitemaps.xml
```

# Web technologies being used

Firefox add-ons :

- [BuiltWith](https://addons.mozilla.org/en-US/firefox/addon/builtwith/)
- [Wappalyzer](https://addons.mozilla.org/en-US/firefox/addon/wappalyzer/)

# Web scanner

```bash
whatweb example.org
```

```bash
nikto example.org
```

```bash
nuclei example.org
```

# CLI Browser

```bash
lynx http://<target>
```