## AMASS

The user's guide can be found here:  
https://github.com/owasp-amass/amass/blob/master/doc/user_guide.md

An example configuration file can be found here:  
https://github.com/owasp-amass/amass/blob/master/examples/config.yaml

The Amass tutorial can be found here:  
https://github.com/owasp-amass/amass/blob/master/doc/tutorial.md

#### **Installation**
```bash 
sudo apt-get update
sudo apt-get install amass
```

#### Covered Techniques (MITRE ATT&CK)
- T1596: Search Open Technical Databases
	-	T1596.001: DNS/Passive DNS
	-	T1596.002: WHOIS
	-	T1596.003: Digital Certificates
### 1\. Basic Subdomain Enumeration

```bash
amass enum -d <domain.com>
```

- Purpose: Performs basic enumeration to discover subdomains for the specified domain (&lt;domain.com&gt;).
- Use Case: Typically used to discover subdomains during reconnaissance or asset discovery.

### 2\. Active Subdomain Enumeration

```bash
amass enum -d <domain.com> -active

```

- Purpose: Actively enumerates and sends DNS resolution requests to verify the existence of discovered subdomains.
- Use Case: Used when you need to actively verify subdomains rather than relying solely on passive data.

### 3\. Save Results in JSON Format

```bash
amass enum -d <domain.com> -json <output.json>

```

- Purpose: Saves the enumeration results to a JSON file for further analysis.
- Use Case: Ideal for structured data storage, automation, or reporting.

### 4\. Brute Force Subdomains 

```bash
amass enum -d <domain.com> -brute

```

- Purpose: Brute-forces potential subdomains by combining different words and phrases.
- Use Case: Used when passive or active enumeration yields insufficient results.

### 5. Output to Text File

```bash
amass enum -d <domain.com> -o <output.text>
```

- Purpose: Saves the discovered subdomains to a text file.
- Use Case: Simple storage of results for documentation or sharing.

### 6. Use a Custom Wordlist for Brute-Forcing 

```bash 
amass enum -d <domain.com> -brute -w <wordlist.txt>
````

- Purpose: Uses a custom wordlist to brute-force subdomains.
- Use Case: For more targeted brute-forcing using domain-specific wordlists.

### 7. Perform ASN Enumeration

```bash 
amass intel -asn <ASN>
````

- Purpose: Discovers domains and subdomains associated with a specific Autonomous System Number (ASN).
- Use Case: Used when you want to discover domains owned by a specific organization through its ASN.

### 8. Search Historical WHOIS Records

```bash 
amass intel -whois -d <domain.com>
````

- Purpose: Gathers information from historical WHOIS records.
- Use Case: Helpful for tracking changes in domain ownership.

### 9. Passive Subdomain Enumeration 

```bash
amass enum -passive -d <domain.com>
````

- Purpose: Performs passive DNS enumeration without making requests to the target.
- Use Case: Ideal for stealthy reconnaissance.

### 10. Save Results to a Specific Directory 

```bash 
amass enum -d <domain.com> -dir <output_directory>
````

- Purpose: Stores results and related data in a specified directory.
- Use Case: Useful for keeping results organized across multiple runs.

### 11. Limit Active Scan to Specific Ports

```bash
amass enum -d <domain.com> -active -p <80,443>
````

- Purpose: Limits the active scan to the specified ports (e.g., 80 and 443).
- Use Case: Used when you need to restrict port scanning to specific services.

### 12. Visualising results

https://linuxcommandlibrary.com/man/amass-viz

```bash
amass viz -graphistry -dir [path/to/database_directory]
```

- Purpose: Generates a Graphistry JSON file based on the Amass - database data. Graphistry is a platform for large-scale graph visualizations, and this command exports the results in a format that can be uploaded and visualized on Graphistry’s platform.

- Use Case: This is useful when you want to create a detailed and interactive visual graph of the discovered subdomains, IP addresses, and relationships between DNS records, allowing for more in-depth analysis.

#### **Notes**
1. **Autonomous System Number (ASN)** is a unique identifier of certain IP prefixes. To find an ASN of an organization you can query https://bgp.he.net/.
2. **WHOIS** is a protocol that queries databases storing information about domain ownership and registration details. An API that can be used https://www.whoisxmlapi.com/. 
