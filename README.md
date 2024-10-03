# Cybersecurity Tools and Techniques Documentation

## Purpose
This repository documents various cybersecurity tools and techniques aligned with the [MITRE ATT&CK](https://attack.mitre.org/) framework, a globally accessible knowledge base of adversarial tactics and techniques based on real-world observations.

The repository is organized based on the phases of a cyberattack as defined by MITRE ATT&CK. Each phase, known as a "tactic," is a strategic goal that adversaries aim to achieve during their attack campaigns. The repository starts with **Reconnaissance** and expands to include other phases.

### Current Structure

- **Reconnaissance**
  - [General](./Reconnaissance/General.md)
  - [AMASS](./Reconnaissance/AMASS.md)
  - [Sn1per](./Reconnaissance/Sn1per.md)
  - [theHarvester](./Reconnaissance/theHarvester.md)
   - [Recon-ng](./Reconnaissance/Recon-ng.md)
   - [Gobuster](./Reconnaissance/Gobuster.md)


As the repository grows, additional tactics and tools will be documented.

## MITRE ATT&CK Tactics

Below is a list of the primary **tactics** from the MITRE ATT&CK framework, each representing a specific goal or phase in an adversary's attack. Click on the tactic names to view detailed information from MITRE ATT&CK.

1. **Reconnaissance**: Gathering information necessary to plan future operations.
   - [MITRE ATT&CK - Reconnaissance](https://attack.mitre.org/tactics/TA0043/)

2. **Resource Development**: Establishing the infrastructure and resources required to launch attacks.
   - [MITRE ATT&CK - Resource Development](https://attack.mitre.org/tactics/TA0042/)

3. **Initial Access**: Gaining an initial foothold within a network.
   - [MITRE ATT&CK - Initial Access](https://attack.mitre.org/tactics/TA0001/)

4. **Execution**: Running malicious code on the target system.
   - [MITRE ATT&CK - Execution](https://attack.mitre.org/tactics/TA0002/)

5. **Persistence**: Maintaining a foothold in the system, even after reboots or credential changes.
   - [MITRE ATT&CK - Persistence](https://attack.mitre.org/tactics/TA0003/)

6. **Privilege Escalation**: Gaining elevated permissions on a system.
   - [MITRE ATT&CK - Privilege Escalation](https://attack.mitre.org/tactics/TA0004/)

7. **Defense Evasion**: Avoiding detection or bypassing security controls.
   - [MITRE ATT&CK - Defense Evasion](https://attack.mitre.org/tactics/TA0005/)

8. **Credential Access**: Stealing credentials like usernames and passwords.
   - [MITRE ATT&CK - Credential Access](https://attack.mitre.org/tactics/TA0006/)

9. **Discovery**: Understanding the environment, such as network architecture, software, and users.
   - [MITRE ATT&CK - Discovery](https://attack.mitre.org/tactics/TA0007/)

10. **Lateral Movement**: Moving within the network to other systems.
    - [MITRE ATT&CK - Lateral Movement](https://attack.mitre.org/tactics/TA0008/)

11. **Collection**: Gathering data of interest to the adversary.
    - [MITRE ATT&CK - Collection](https://attack.mitre.org/tactics/TA0009/)

12. **Command and Control**: Establishing communication with compromised systems to control them.
    - [MITRE ATT&CK - Command and Control](https://attack.mitre.org/tactics/TA0011/)

13. **Exfiltration**: Stealing data from the network.
    - [MITRE ATT&CK - Exfiltration](https://attack.mitre.org/tactics/TA0010/)

14. **Impact**: Manipulating, interrupting, or destroying systems and data.
    - [MITRE ATT&CK - Impact](https://attack.mitre.org/tactics/TA0040/)

For more information about each tactic and how adversaries use these phases in real-world attacks, visit the [MITRE ATT&CK website](https://attack.mitre.org/).

## Contributing
Contributions are welcome! If you have additional tools or techniques that align with the MITRE ATT&CK framework, feel free to open a pull request or raise an issue for discussion.

---

This repository is a work in progress, and new tools will be added as they are documented.

### License
This project is licensed under the [MIT License](./LICENSE).
