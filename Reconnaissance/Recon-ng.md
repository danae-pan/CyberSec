## Recon-ng

Github repo: https://github.com/lanmaster53/recon-ng

Guides: https://hackertarget.com/recon-ng-tutorial/

Youtube Tutorial: https://www.youtube.com/playlist?list=PLBf0hzazHTGOg9taK90uFjdcb8UgGfRKZ

Recon-ng in Kali Linux: https://www.kali.org/tools/recon-ng/

#### **Installation**
```bash
sudo apt-get update
sudo apt-get install recon-ng
```

#### Covered Techniques (MITRE ATT&CK)
- T1250: Determine Domain and IP Address Space
- T1261: Enumerate Externally Facing Software Applications, Technolohies, Languages and Dependencies.
- T1271: Identify Personnel with an Authority/Privilege

### 1. Create a New Workspace 

```bash
workspaces create <workspace_name>
```

- Purpose: Creates a new workspace to store reconnaissance data.
- Use Case: This helps organize your work by creating separate workspaces for different projects or targets.

### 2. Switch Between Workspaces

```bash
workspace select <workspace_name>
```

- Purpose: Switches between different workspaces.
- Use Case: Useful for managing multiple reconnaissance projects, each with its own workspace.

### 3. List Existing Workspaces 

```bash
workspace list
```

- Purpose: Lists all the existing workspaces.
- Use Case: Helps you view all created workspaces and switch between them when needed.

### 4. Marketplace Search 

```bash
marketplace search <module_name>
```

- Purpose: Searches for modules available in the Recon-ng marketplace.
- Use Case: Helps you search for specific modules by name or keyword, allowing you to discover functionality that you might need.

### 5. Install a Module

```bash
marketplace instal <module_path>
```

- Purpose: Installs a specific module from the marketplace.
- Use Case: Once you find the module you need, this command installs it for use.

### 6. Seed the Database with Data

```bash
db instert <table_name>
```

- Purpose: Manually inserts data into the database.
- Use Case: If you have pre-existing data (e.g., domains or IP addresses), you can insert it into Recon-ng's database.

### 7. Show Stored Data

```bash
show <table_name>
```

- Purpose: Displays the data gathered during the session, stored in different tables.
- Use Case: After running a module, this command shows data such as domains, contacts, hosts, etc.

### 8. Perform a WHOIS Lookup

```bash
load recon/domain-hosts/whois
run
```

- Purpose: Performs a WHOIS lookup on the target domain to gather domain registration information.
- Use Case: Useful for gathering domain ownership details such as the registrar, creation/expiration dates, and contact information.

### 9. Perform Subdomain Enumeration 

```bash
load recon/domain-hosts/brute_hosts
run
```

- Purpose: Brute-forces subdomains on the target domain.
- Use Case: Identifies hidden subdomains, which could expose internal systems or potentially vulnerable infrastructure.