## theHarvester

Github repo: https://github.com/laramies/theHarvester

theHarvester in Kali Linux: https://www.kali.org/tools/theharvester/

#### **Installation**

https://github.com/laramies/theHarvester/wiki/Installation

```bash
git clone https://github.com/laramies/theHarvester
cd theHarvester
sudo apt-get update
sudo apt-get install python3-pip
pip3 install -r requirements-txt
```

#### Covered Techniques (MITRE ATT&CK)
- T1250: Determine Domain and IP Address Space
- T1255: Discover Target Logon/Email Address Format
- T1251: Discover Target Domain/IP Registration Information
- T1254: Conduct Active Scanning
- T1273: Mine Social Media

### 1. Basic Domain Search 

```bash 
theHarvester -d <domain> -b all
```

- Purpose: Conducts a basic search on the specified domain using all available data sources.
- Use Case: Ideal for gathering information on a target domain (e.g., subdomains, email addresses, IPs) from various public sources in one go.

### 2. Search Specific Data Sources 

```bash
theHarvester -d <domain> -b <data_source>
```

- Purpose: Searches the specified domain using only the chosen data source (e.g., Google, Bing, LinkedIn).
- Use Case: Useful when you want to focus on a specific data source (e.g., google, bing, linkedin, crtsh).

### 3.  Limit Number of Results from Data Source

```bash
theHarvester -d <domain> -b <data_source> --limit <number>
```

- Purpose: Limits the number of results collected from the specified data source. This is not limited to emails; it will limit all collected data, including subdomains, IP addresses, and email addresses.
- Use Case: Useful when you want to gather a smaller, more manageable set of results.

### 4. Specify Output File Type

```bash
theHarvester -d <domain> -b all -f <output_file> -o <file_type>
```

- Purpose: Saves the results to an output file, with an option to specify the file format (e.g., XML, JSON, HTML).
- Use Case: Ideal when you need to save results for later analysis or sharing with others.

### 5. Passive DNS Search 

```bash 
theHarvester -d <domain> -b crtsh
```

- Purpose: Performs a search for DNS records using Certificate Transparency logs.
- Use Case: Helpful for discovering subdomains and DNS records that are publicly available through certificate transparency logs.

### 6. Search with a Proxy 

```bash 
theHarvester -d <domain> -b all --proxy <proxy_ip:port>
````

- Purpose: Routes the search through a proxy, which can be useful for anonymizing the search or avoiding IP rate limits.
- Use Case: Helps prevent detection by hiding your real IP during information gathering.

### 7. Passive Mode 

```bash
theHarvester -d <domain> -b all --limit <number> -p
```

- Purpose: Runs a passive search only, avoiding interactions that could alert the target.
- Use Case: Useful when you want to remain stealthy and not actively interact with the target's infrastructure.

### 8. Active Mode (DNS Brute Force & Screenshots)

```bash 
theHarvester -d <domain> -b all --dns-brute --take-screenshots
````

- Purpose: Performs a DNS brute force attack and takes screenshots of discovered subdomains.
- Use Case: This is helpful during red team assessments when detailed reconnaissance and visual confirmation of discovered services are required.

#### **Notes**
1. Use a VPN when using theHarvester to avoid having your IP blocked.

