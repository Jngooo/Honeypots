## Honeypot Types

- **Honey System**: Emulates operating systems and services, providing production-like honeypots that closely resemble real environments.

- **Honey Service**: Simulates software or protocol functions, such as HTTP, database, email, authentication, and more.

- **Honey Tokens**: Replicates data and fictitious IT resources, including files, API keys, dummy credentials, and bait accounts, with the intention of attracting malicious login attempts.

## Placement of Honeypots

- **External Placement**: Positioned in front of the firewall, external honeypots serve as perpetual collectors of threat intelligence. They effectively differentiate automated probes from human intrusion attempts, visualize malicious activity trends, and act as an early warning system. However, they may consume resources due to false positive alerts.

- **Internal Placement**: Located behind the firewall within the internal network, internal honeypots play a crucial role in identifying internal attackers, detecting lateral movement, optimizing resource usage, and facilitating port mirroring. Challenges include controlling compromised data within local traffic and the risk of direct attacks on production systems.

- **DMZ Placement**:  Positioned within the Demilitarized Zone (DMZ), between two firewalls, DMZ honeypots serve as an advanced warning mechanism by proactively detecting and intercepting malicious activity prior to breaching the production environment. Nevertheless, establishing and maintaining a DMZ-based honeypot necessitates meticulous configuration and ongoing management to ensure optimal effectiveness while mitigating potential vulnerabilities.
