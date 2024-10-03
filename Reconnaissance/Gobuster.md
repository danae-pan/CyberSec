## Gobuster

Github repo: https://github.com/OJ/gobuster

Gobuster in Kali Linux: https://www.kali.org/tools/gobuster/

Guides: https://hackertarget.com/gobuster-tutorial/

Wordlist: https://github.com/danielmiessler/SecLists
```bash
sudo apt -y install seclists
```

#### **Installation**

```bash 
sudo apt-get install gobuster
```

#### Covered Techniques (MITRE ATT&CK)
-  T1595: Active Scanning
	- T1595.001: Scanning IP Blocks
	- T1595.003: Wordlist Scanning

### 1. Basic Directory Brute-Force

```bash 
gobuster dir -u <url> -w <wordlist>
```

Purpose: Performs a directory brute-force attack on the specified URL using the provided wordlist.
Use Case: This is useful for discovering hidden directories and files on web servers.

### 2. Subdomain Brute-Force

```bash
gobuster dns -d <domain> -w <wordlist>
```

- Purpose: Performs a subdomain brute-force attack on a domain.
- Use Case: Identifies subdomains of a target domain using a wordlist.

### 3. VHOST Brute-Force

```bash 
gobuster vhost -u <url> -w <wordlist>
```

- Purpose: Performs virtual host brute-force attacks on the given URL.
- Use Case: This helps identify virtual hosts on the target domain.

### 4. Directory Brute-Force with Custom Status Code

```bash
gobuster dir -u <url> -w <wordlist> -s <status_code>
```

- Purpose: Filters the results to show only specific HTTP status codes during directory brute-force attacks.
- Use Case: Useful when you're interested in certain status codes (e.g., 200 for successful requests or 403 for forbidden directories).

### 5. Brute-Force with a Proxy

```bash 
gobuster dir -u <url> -w <wordlist> -p <proxy_url>
```

- Purpose: Sends requests through a proxy while brute-forcing directories or subdomains.
- Use Case: Useful for anonymizing traffic or routing requests through a specific proxy.

### 6. Save Results to a File

```bash 
gobuster dir -u <url> -w <wordlist> -o <output_file>
```

- Purpose: Saves the output of the Gobuster scan to a file.
- Use Case: This is useful for saving the results for later analysis or reporting.

### 7. Recursive Directory Brute-Force

```bash 
gobuster dir -u <url> -w <wordlist> -r
```

- Purpose: Recursively brute-forces directories found during the initial scan.
- Use Case: This is useful for finding deeper hidden files and directories within discovered directories.

### 8. Ignore SSL Certificate Validation 

```bash 
gobuster dir -u <url> -w <wordlist> -k
```

- Purpose: Skips SSL certificate validation when accessing HTTPS websites.
- Use Case: Useful when the target site has an invalid or self-signed SSL certificate.

### 9. Use Basic Authentication 

```bash 
gobuster dir -u <url> -w <wordlist> -U <username> -P <password>
```

- Purpose: Sends basic HTTP authentication credentials while brute-forcing.
- Use Case: Useful for targeting protected directories or services that require basic authentication.