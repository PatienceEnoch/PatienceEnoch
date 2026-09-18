<p align="center">
  <img src="https://raw.githubusercontent.com/PatienceEnoch/PatienceEnoch/main/ChatGPT%20Image%20Dec%206%2C%202025%2C%2005_29_15%20PM.png" alt="Patience Hopkins - Cloud and Network Engineering" width="100%">
</p>

# Ashley "Patience" Hopkins

**Cloud & Network Engineering student · Linux · AWS · Python · Security-aware networking**

I'm completing the AWS track of the B.S. Cloud and Network Engineering program at Western Governors University.

Most of my learning happens in labs: build the system, break it on purpose, collect the evidence, and work backward until I can explain exactly what failed. Networking is the center of it, with Linux, cloud infrastructure, automation, and security layered around it.

What interests me most is understanding what changed when a system stops behaving normally, and using the evidence to work backward to the cause.

## Current build: [Network Flight Recorder](https://github.com/PatienceEnoch/network-flight-recorder)

**A black box for your network.**

Network Flight Recorder records a known-good Linux network state, watches for meaningful changes, correlates symptoms into likely causes, and preserves evidence through recovery.

A few decisions that shape the project:

- **Local-first diagnosis.** Core troubleshooting still works when the external network does not.
- **Evidence before action.** Findings are tied to observable state instead of opaque alerts.
- **Privacy before upload.** Sensitive network values can be pseudonymized before evidence is stored in AWS.
- **Guarded recovery.** Remediation is approval-gated, allowlisted, verified after execution, and can roll back in the isolated lab when verification fails.
- **Reproducible failure testing.** Docker creates real routing failures without touching the host network.
- **Automated checks.** GitHub Actions validates Python, dependencies, and Terraform.

`Python` · `Linux` · `Docker` · `Terraform` · `AWS` · `S3` · `CloudWatch` · `GitHub Actions` · `pytest` · `Ruff`

[Read the project →](https://github.com/PatienceEnoch/network-flight-recorder)

## Other hands-on work

### [Ubuntu Virtual Network Lab](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab)

Two Ubuntu systems used to work through routing, NAT, DNS, SSH, Apache, nftables, and packet inspection with `tcpdump`. This is where a lot of the networking theory became visible instead of abstract.

### [Tor Middle Relay Deployment](https://github.com/PatienceEnoch/TOR_Relay)

A documented Tor middle-relay deployment centered on Linux service administration, TCP/IP, port configuration, logging, and traffic validation.

### [IDOR Security Learning Project](https://github.com/PatienceEnoch/IDOR--Insecure_Direct_Object_Reference_Learning-Project)

An authorized lab for studying insecure direct object references and broken access control through HTTP request behavior, exploitation evidence, impact, and prevention.

### [Cloud & Network Engineering Portfolio](https://github.com/PatienceEnoch/Hopkins_portfolio)

My broader technical notebook: labs, certifications, coursework, architecture notes, and project work as I build toward cloud and network engineering roles.

## Toolkit

| Area | Working with |
| --- | --- |
| **Networking** | TCP/IP, IPv4, subnetting, DNS, DHCP, NAT, VLANs, routing, switching, firewalls, VPN troubleshooting, packet analysis |
| **Linux & systems** | Ubuntu, systemd, Bash, SSH, NGINX, permissions, services, logging, virtualization, system troubleshooting |
| **Cloud & infrastructure** | AWS, S3, CloudWatch, IAM, Terraform, Docker, infrastructure as code |
| **Development & automation** | Python, pytest, Ruff, Git, GitHub Actions, JSON, CLI tooling |
| **Security** | Network visibility, access control, dependency auditing, evidence protection, secure-by-default design |

## Certifications

- CompTIA Network+
- CompTIA A+
- LPI Linux Essentials
- ITIL 4 Foundation
- CompTIA IT Fundamentals

## What I'm working on now

I'm deepening the parts that connect directly to network engineering work: Cisco/CCNA concepts, Linux troubleshooting, AWS networking, network observability, Python automation, and defensive security.

The goal is not to collect disconnected skills. I want to be able to follow a problem across the stack—from interface and route state to cloud infrastructure—and explain what the evidence shows.

## Where I'm headed

I'm looking toward network and cloud engineering roles where troubleshooting matters: network operations, cloud support, infrastructure support, systems administration, and security-aware networking.

I'm based in North Alabama and especially interested in the Huntsville area.

[LinkedIn](https://www.linkedin.com/in/ashley-hopkins-432244329/) · [Technical Portfolio](https://github.com/PatienceEnoch/Hopkins_portfolio)

---

> **"Light in one hand. Linux in the other."**
