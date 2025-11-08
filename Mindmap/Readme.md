# Recon & OSINT for Red Teamers

Offensive security begins with intelligence.
This repository is a focused, practice-oriented reference for Reconnaissance and OSINT workflows used by Red Teams, penetration testers, and security researchers to discover, profile, and prioritize attack surface in authorized engagements.

---

## Table of Contents

* [Purpose](#purpose)
* [Scope](#scope)
* [Core Recon Categories](#core-recon-categories)
* [Passive OSINT](#passive-osint)
* [Active Recon](#active-recon)
* [Typical Workflows](#typical-workflows)
* [Deliverables / Output Artifacts](#deliverables--output-artifacts)
* [Ethics, Authorization & Legal](#ethics-authorization--legal)
* [Contributing](#contributing)
* [License](#license)

---

## Purpose

Provide structured, repeatable Recon and OSINT workflows and reference material specifically tailored to Red Team operations and pre-engagement intelligence collection. This README acts as a single-page overview for newcomers and experienced operators alike.

---

## Scope

* External attack surface discovery (internet-facing assets)
* Identity & people-target OSINT (public profiles, email harvesting)
* Public code & data leakage (repositories, paste sites)
* Infrastructure and cloud footprinting
* Safe and authorized reconnaissance techniques only

*Not included: exploit implementation, active exploitation guides, or instructions intended to be used without explicit authorization.*

---

## Core Recon Categories

1. **Passive Recon** — Collect information without direct interaction (OSINT sources, public datasets, CT logs).
2. **Active Recon** — Controlled interactions (DNS queries, scans) performed with care and authorization.
3. **Infrastructure Recon** — Hosts, ports, services, DNS, ASN mapping, cloud assets.
4. **Application Recon** — Web applications, APIs, endpoints, parameters and logic.
5. **Identity Recon** — Employee enumeration, email patterns, breached credentials.
6. **Supply Chain / Third-Party** — Vendors, partners, subdomains and SaaS integrations.

---

## Passive OSINT

Focus: discover and collect publicly available data without touching target infrastructure.

Common sources:

* Certificate Transparency (crt.sh, Censys)
* Public DNS / zonewalk outputs and historical DNS
* Public code repositories (GitHub, GitLab, Bitbucket)
* Paste sites, forums, blogs, social media
* Job boards and recruiting sites (org structure hints)
* Leak / breach databases

Outputs:

* Subdomain lists, domain aliases, service providers, email formats, public S3/Blob buckets, secrets in repos.

---

## Active Recon

Focus: authorized probing to validate assets, enumerate services, and capture responses.

Activities:

* DNS resolution, AXFR (if allowed), and bruteforce
* Port scanning and service/version fingerprinting
* Web crawling and directory/parameter enumeration
* API surface mapping and fuzzing (read-only where possible)
* Banner grabbing and TLS/HTTP header analysis

Risk control:

* Use proper scoping & authorization
* Rate-limit and use respectful scan profiles
* Coordinate with blue team where required

---

## Typical Workflows

1. **Kickoff & Scope Confirmation**

   * Confirm in-scope domains, IP ranges, cloud tenants, and excluded targets.
2. **Passive Collection**

   * Harvest CT logs, public repos, OSINT, social media, paste sites, WHOIS.
3. **Asset Aggregation**

   * Deduplicate and normalize assets (domains, hosts, IPs).
4. **Active Enumeration (low impact)**

   * Validate assets with DNS/resolution and light HTTP checks.
5. **Deep Enumeration (controlled)**

   * Port/service scans, app enumeration, API discovery within limits.
6. **Analysis & Prioritization**

   * Map assets to business functions, identify high-risk exposures.
7. **Reporting**

   * Produce inventory, attack-surface map, recommended mitigations.

---

## Deliverables / Output Artifacts

* **Asset Inventory CSV / JSON**
* **Attack Surface Map Visuals**
* **Prioritized Findings List**
* **Executive Summary**
* **TTP Notes & Methodology Log**

---

## Ethics, Authorization & Legal

This content is intended **only** for lawful, authorized security testing and research.

Unauthorized scanning or probing of systems you do not own or have written authorization to test is illegal.

Before any active recon:

* Obtain written authorization (scope & dates).
* Coordinate with legal/compliance and the target’s security contacts.
* Respect data protection and privacy regulations.

---

## Contributing

Contributions are welcome — tools, workflow improvements, sanitized case studies.

---

## License

MIT License

---
