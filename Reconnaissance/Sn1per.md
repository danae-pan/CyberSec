## Sn1per

Github repo: https://github.com/1N3/Sn1per

Sn1per configuration options: https://github.com/1N3/Sn1per/wiki/Sn1per-Configuration-Options

#### **Installation**
```bash
git clone https://github.com/1N3/snipper.git
cd Sn1per
sudo bash install.sh 
````

**Note**: Sn1per needs to be run as root 
```bash 
sudo -i
````

#### Covered Techniques (MITRE ATT&CK)
- T1595: Active Scanning
- T1592: Gather Victim Host Information
- T1590: Gather Victim Network Information
- T1596: Search Open Source Technical Databases
- T1593: Search Open Source Website/Domains
- T1589: Gather Victim Identity Information 

### 1\. Basic Target Scan

```bash
sniper -t <target>
```

- Purpose: Performs a basic scan on the specified target (target).
- Use Case: This is the most basic usage of Sn1per, ideal for quickly scanning a domain or IP address to gather general information.

**Note**: Use this command if you are authorised to perform active recon.

### 2. Full Target Scan with OSINT

```bash 
sniper -t <target> -o full
````
- Purpose: Performs a full scan including OSINT (Open Source Intelligence) collection.
- Use Case: This command is used to perform a thorough reconnaissance scan on the target, collecting as much information as possible from publicly available sources.

### 3\. Stealth Scan (Noisy Scan Disabled)

```bash
sniper -t <target> -m stealth 
````

- Purpose: Runs a stealthy scan, disabling noisy scans that might alert the target.
- Use Case: Useful when you need to gather information quietly without triggering alarms on the target's systems.

### 4. Nuke Scan (Comprehensive and Aggresive)

```bash 
sniper -t <target> -m nuke
````

- Purpose: Performs a highly aggressive and comprehensive scan of the target.
- Use Case: This is used when you want to go all-in and perform an exhaustive scan that tests every aspect of the target’s infrastructure.

### 5. Web Application Scan 

```bash 
sniper -t <target> -m web 
````

- Purpose: Scans for vulnerabilities and issues specific to web applications.
- Use Case: Useful when you are targeting a website or web application and want to focus on vulnerabilities such as SQL injection, XSS, etc.

### 6. Launch Mass Scan Against Multiple Targets

```bash 
sniper -f <file>
````

- Purpose: Runs Sn1per against multiple targets listed in a file.
- Use Case: Useful when you need to scan multiple domains or IP addresses at once. The file should contain a list of targets.

### 7. Passive Scan (OSINT Only)

```bash 
sniper -t <target> -m passive
```

- Purpose: Conducts an OSINT-only scan, avoiding any direct interaction with the target.
- Use Case: Ideal when you only want to gather publicly available data and avoid making any requests or connections to the target.

### 8. Generate HTML Report 

```bash 
sniper -t <target> --report
````

- Purpose: Generates an HTML report of the scan results.
- Use Case: Useful when you need to generate a presentable report for further analysis or sharing with team members.

### 9. Anonymous Scan with TOR

```bash
sniper -t <target> --tor
````

- Purpose: Runs the scan through the TOR network for anonymization.
- Use Case: Helps to mask the origin of your scan, useful for avoiding detection or blocking by the target.
