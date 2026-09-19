<p align="center">
  <img src="https://raw.githubusercontent.com/PatienceEnoch/PatienceEnoch/main/assets/profile-header.svg" alt="Patience Enoch — Cloud and Network Engineering" width="100%">
</p>

# Ashley "Patience" Hopkins

**Cloud & Network Engineering student · Linux · AWS · Python · Security-aware networking**

I like systems I can take apart, understand, break safely, and make more observable.

I'm completing the AWS track of the B.S. Cloud and Network Engineering program at Western Governors University. Most of my learning happens in labs: build the system, create a controlled failure, collect the evidence, and work backward until I can explain exactly what changed.

Networking is the center of it, with Linux, cloud infrastructure, automation, and security layered around it.

## // CURRENT BUILDS

### [Network Flight Recorder](https://github.com/PatienceEnoch/network-flight-recorder)

**A black box for your network.**

A local-first network observability and troubleshooting tool that records known-good state, watches for meaningful changes, correlates symptoms into likely causes, preserves incident evidence, and supports guarded recovery.

**What I care about in this build**

- Evidence before action
- Diagnosis that still works when the external network does not
- Privacy-aware evidence handling before cloud upload
- Approval-gated, allowlisted remediation with verification and rollback
- Reproducible Docker failure injection
- Automated Python and Terraform checks in GitHub Actions

`Python` · `Linux` · `Docker` · `Terraform` · `AWS` · `S3` · `CloudWatch` · `GitHub Actions` · `pytest` · `Ruff`

[Read the project →](https://github.com/PatienceEnoch/network-flight-recorder)

---

### [Shipment Tracker](https://github.com/PatienceEnoch/shipment-tracker)

**A small operational problem turned into an automated workflow.**

Built for a real parts-sales workflow: a sales-order email starts a 72-hour clock, a tracking email attaches the FedEx number, and a second clock measures whether FedEx actually acquires the package. Once FedEx has possession, the order is complete.

The current version includes Gmail intake, automated alerting, deduplication, a browser dashboard, SQLite persistence, FastAPI endpoints, and GitHub Actions. The next integration point is FedEx's tracking API.

`Python` · `FastAPI` · `SQLAlchemy` · `SQLite` · `Gmail/IMAP` · `SMTP` · `GitHub Actions` · `pytest`

[Read the project →](https://github.com/PatienceEnoch/shipment-tracker)

## // PROJECTS IN THE FIELD

### [Ubuntu Virtual Network Lab](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab)

Two Ubuntu systems used to work through routing, NAT, DNS, SSH, Apache, nftables, and packet inspection with `tcpdump`. This is where a lot of the networking theory became visible instead of abstract.

### [Tor Middle Relay Deployment](https://github.com/PatienceEnoch/TOR_Relay)

A documented Tor middle-relay deployment centered on Linux service administration, TCP/IP, port configuration, logging, and traffic validation.

### [IDOR Security Learning Project](https://github.com/PatienceEnoch/IDOR--Insecure_Direct_Object_Reference_Learning-Project)

An authorized lab for studying insecure direct object references and broken access control through HTTP request behavior, exploitation evidence, impact, and prevention.

### [Cloud & Network Engineering Portfolio](https://github.com/PatienceEnoch/Hopkins_portfolio)

My broader technical notebook: labs, certifications, coursework, architecture notes, and project work as I build toward cloud and network engineering roles.

## // TOOLKIT

| Area | Working with |
| --- | --- |
| **Networking** | TCP/IP, IPv4, subnetting, DNS, DHCP, NAT, VLANs, routing, switching, firewalls, VPN troubleshooting, packet analysis |
| **Linux & systems** | Ubuntu, systemd, Bash, SSH, NGINX, permissions, services, logging, virtualization, system troubleshooting |
| **Cloud & infrastructure** | AWS, S3, CloudWatch, IAM, Terraform, Docker, infrastructure as code |
| **Development & automation** | Python, FastAPI, SQLAlchemy, pytest, Ruff, Git, GitHub Actions, JSON, CLI tooling |
| **Security** | Network visibility, access control, dependency auditing, evidence protection, secure-by-default design |

## // CERTIFICATIONS

- CompTIA Network+
- CompTIA A+
- LPI Linux Essentials
- ITIL 4 Foundation
- CompTIA IT Fundamentals

## // ENGINEERING NOTES

Right now I'm deepening the parts that connect directly to network engineering work: Cisco/CCNA concepts, Linux troubleshooting, AWS networking, network observability, Python automation, and defensive security.

The goal isn't to collect disconnected skills. I want to be able to follow a problem across the stack—from interface and route state to cloud infrastructure—and explain what the evidence shows.

## // WHERE I'M HEADED

I'm working toward network and cloud engineering roles where troubleshooting matters: network operations, cloud support, infrastructure support, systems administration, and security-aware networking.

I'm based in North Alabama and especially interested in the Huntsville area.

[LinkedIn](https://www.linkedin.com/in/ashley-hopkins-432244329/) · [Technical Portfolio](https://github.com/PatienceEnoch/Hopkins_portfolio)

---

> **Light in one hand. Linux in the other.**
