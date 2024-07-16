<h1>Nmap</h1>

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

<h1>Metasploit</h1>

```bash
msf6 > use auxiliary/scanner/http/http_version
```

```bash
msf6 > use auxiliary/scanner/http/brute_dirs
```

```bash
msf6 > use auxiliary/scanner/http/robots_txt
```

<h1>HTTP fingerprint</h1>

```bash
http <target>
```

<h1>Directory listing</h1>

```bash
dirb <target>
```

<h1>Directories hidden from search engines</h1>

```bash
https://example.org/robots.txt  
https://example.org/sitemap.xml  
https://example.org/sitemaps.xml
```

<h1>Web technologies being used</h1>

Firefox add-ons :

- [BuiltWith](https://addons.mozilla.org/en-US/firefox/addon/builtwith/)
- [Wappalyzer](https://addons.mozilla.org/en-US/firefox/addon/wappalyzer/)

<h1>Web scanner</h1>

```bash
whatweb example.org
```

```bash
nikto example.org
```

```bash
nuclei example.org
```

<h1>CLI Browser</h1>

```bash
lynx http://<target>
```