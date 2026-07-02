# Network Security Baseline

Project 1 of a six-project GRC portfolio series demonstrating hands-on
security engineering aligned to NIST Cybersecurity Framework 2.0.

## Objective

Establish a segmented network architecture with documented asset inventory,
risk-tiered classification, and least-privilege access controls suitable
as a baseline for downstream security operations projects (SIEM deployment,
vulnerability management, compliance gap assessment).

## Architecture

![Network Architecture](diagrams/project1-network-architecture-v1.0.png)

Three-tier VLAN segmentation on OPNsense firewall:

- **VLAN 10 (Management)** — Administrative access, analyst workstation
- **VLAN 20 (Monitoring)** — SIEM and log aggregation, restricted egress
- **VLAN 30 (Lab-Vulnerable)** — Attack targets, isolated from management plane

## NIST CSF 2.0 Controls Implemented

| Function | Subcategory | Implementation |
|---|---|---|
| Identify | ID.AM-01 | Hardware inventory maintained via Nmap asset scanner |
| Identify | ID.AM-02 | Software/services inventory maintained via Nmap version detection |
| Identify | ID.AM-03 | Network communication and data flows mapped (see diagram) |
| Protect | PR.AA-05 | Access permissions managed via inter-VLAN firewall rules with least privilege |
| Protect | PR.IR-01 | Network segmented based on risk tier |

## Artifacts

- [Network Architecture Diagram](diagrams/project1-network-architecture-v1.0.png)
- Data Classification Policy — *coming*
- Business Risk Context Document — *coming*
- Reflection Notes — *coming*

## Related Repositories

- [nmap-asset-scanner](https://github.com/Alasall0/nmap-asset-scanner) — Python-based asset discovery tool
- [pfsense-log-parser](https://github.com/Alasall0/pfsense-log-parser) — Firewall log parsing utility

## Author

Anthony LaSalle | Transitioning USMC S-6 to GRC Engineer
