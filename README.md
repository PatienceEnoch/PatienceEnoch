<p align="center">
  <img src="https://raw.githubusercontent.com/PatienceEnoch/PatienceEnoch/main/assets/profile-header.svg" alt="Patience Enoch — Cloud and Network Engineering" width="100%">
</p>

# Ashley "Patience" Hopkins

**Cloud & Network Engineering student · Linux · AWS · Python · Security-aware networking**

I learn best by building things and then figuring out why they work—or why they don't.

I'm working through the AWS track of WGU's B.S. Cloud and Network Engineering program. Most of what sticks for me comes from hands-on labs: setting something up, breaking it on purpose, looking at the evidence, and tracing the problem back to the source.

Networking is where I feel most at home, but I also spend a lot of time in Linux, AWS, Python, automation, and security.

## // WHERE IT STARTED

My interest in technology started in the early 2000s. My brother introduced me to Linux, and I spent a lot of time in online forums learning HTML, experimenting with computers, and trying to understand how everything worked underneath the interface.

That curiosity never really went away. Today, it has turned into a focus on networking, Linux, cloud infrastructure, and security.

## // ACTIVE SYSTEMS

### [LastKnownGood](https://github.com/PatienceEnoch/last-known-good)

I started this project because I wanted a better way to answer a simple troubleshooting question:

**What changed?**

LastKnownGood captures a known-good network state, watches for meaningful changes, and keeps enough evidence around to help explain what happened during a failure.

Some of the pieces I've built into it so far:

- local-first troubleshooting
- Docker-based failure injection
- Python tests and CLI tooling
- Terraform-managed AWS infrastructure
- S3 evidence storage
- CloudWatch metrics and logging
- guarded remediation with verification and rollback
- GitHub Actions for automated checks

`Python` · `Linux` · `Docker` · `Terraform` · `AWS` · `S3` · `CloudWatch` · `GitHub Actions` · `pytest` · `Ruff`

[Read the project →](https://github.com/PatienceEnoch/last-known-good)

---

### [Mini Internet](https://github.com/PatienceEnoch/mini-internet)

I wanted to see what happens when a route disappears, so I built three connected routers with FRRouting and Docker Compose, each in its own autonomous system.

Then I turned off the direct link between two of them. BGP found the backup path, but the return traffic took longer to catch up. Watching the ping pause made the difference between having a backup route and actually recovering a connection much clearer.

I compared the original BGP timers with shorter settings on that link. In two manual runs, lost ping replies dropped from **176 to 7**. Both runs recovered through the third router, and restoring the link brought the direct route back.

The repo includes the topology, route filters, commands to repeat the tests, and the results with their measurement limits.

`BGP` · `FRRouting` · `Docker Compose` · `Linux` · `IPv4` · `Route filtering` · `Failover testing`

[Read the project →](https://github.com/PatienceEnoch/mini-internet)

---

### [Site-to-Site IPsec VPN Lab](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab/blob/main/docs/local-site-to-site-ipsec-validation.md)

I wanted to understand what "the tunnel is up" actually proves, so I built both sides of a routed IPsec path and traced traffic all the way through it.

The Ubuntu Client at `10.10.10.10` reaches a simulated cloud workload at `10.20.0.10` through two Linux gateways and a strongSwan IKEv2/IPsec tunnel. I worked through NAT exemption, XFRM policy/state, forwarding, return routing, ARP, tcpdump, network namespaces, veth pairs, and duplicate Security Associations.

The finished lab survives reboot on both gateways and returns end-to-end traffic with 0% packet loss. The next phase is applying the same troubleshooting method to AWS Site-to-Site VPN.

`Linux` · `strongSwan` · `IKEv2` · `IPsec` · `XFRM` · `nftables` · `tcpdump` · `network namespaces` · `systemd`

[Read the validation notes →](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab/blob/main/docs/local-site-to-site-ipsec-validation.md) · [AWS extension →](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab/blob/main/docs/hybrid-cloud-vpn.md)

---

### [Shipment Tracker](https://github.com/PatienceEnoch/shipment-tracker)

This project came from a real workflow problem: knowing whether a sales order actually made it from "created" to "FedEx has the package."

The app watches for a sales-order email, starts a 72-hour timer for the shipping label, matches the tracking number when it arrives, and then starts a second timer waiting for FedEx to acquire the package.

Once FedEx has it, the order is done. The customer can track it from there.

So far it has:

- Gmail intake
- automatic overdue alerts
- alert deduplication
- a browser dashboard
- SQLite persistence
- FastAPI endpoints
- GitHub Actions
- tests around the order and status flow

The next piece is replacing the simulated FedEx event with the real FedEx tracking API.

`Python` · `FastAPI` · `SQLAlchemy` · `SQLite` · `Gmail/IMAP` · `SMTP` · `GitHub Actions` · `pytest`

[Read the project →](https://github.com/PatienceEnoch/shipment-tracker)

## // FIELD NOTES

### [Ubuntu Virtual Network Lab](https://github.com/PatienceEnoch/Ubuntu-virtual-network-lab)

Two Ubuntu systems I used to work through routing, NAT, DNS, SSH, Apache, nftables, and packet inspection with `tcpdump`.

This lab helped turn a lot of networking concepts from diagrams into things I could actually see and troubleshoot. It is now the local foundation for my Hybrid Cloud VPN Lab.

### [Tor Middle Relay Deployment](https://github.com/PatienceEnoch/TOR_Relay)

A documented Tor middle-relay deployment focused on Linux services, TCP/IP, port configuration, logging, and traffic validation.

### [IDOR Security Learning Project](https://github.com/PatienceEnoch/IDOR--Insecure-Direct-Object-Reference-Learning-Project)

An authorized lab for learning how insecure direct object references and broken access control show up in real HTTP requests.

### [Cloud Network Architecture Journal](https://github.com/PatienceEnoch/Cloud-Network-Architecture-Journal)

My technical journal for routing, distributed systems, cloud architecture, failure analysis, observability, and the engineering lessons I pull out of hands-on labs.

### [Cloud & Network Engineering Portfolio](https://github.com/PatienceEnoch/Hopkins-portfolio)

My career-facing portfolio site with project highlights, certifications, career materials, and supporting web pages.

## // INCIDENT RECORDS

A few failures that taught me more than the clean builds did:

| Incident | What I followed |
| --- | --- |
| **BGP path failure** | Removed the direct path between two routers, watched traffic fail over through a third, then compared convergence with different timer settings. |
| **IPsec tunnel without end-to-end traffic** | Treated "the tunnel is up" as only one clue and traced routing, forwarding, NAT exemption, XFRM state, ARP, and return traffic until the full path worked. |
| **Injected network failures** | Used controlled breakage in the LastKnownGood lab to capture evidence, compare network state, verify remediation, and preserve a rollback path. |

## // ROUTING TABLE

| Area | Working with |
| --- | --- |
| **Networking** | TCP/IP, IPv4, subnetting, DNS, DHCP, NAT, VLANs, routing, switching, firewalls, VPN troubleshooting, packet analysis |
| **Linux & systems** | Ubuntu, systemd, Bash, SSH, NGINX, permissions, services, logging, virtualization, system troubleshooting |
| **Cloud & infrastructure** | AWS, S3, CloudWatch, IAM, Terraform, Docker, infrastructure as code |
| **Development & automation** | Python, FastAPI, SQLAlchemy, pytest, Ruff, Git, GitHub Actions, JSON, CLI tooling |
| **Security** | Network visibility, access control, dependency auditing, evidence protection, secure-by-default design |

## // CREDENTIALS

- CompTIA Network+
- CompTIA A+
- LPI Linux Essentials
- ITIL 4 Foundation
- CompTIA IT Fundamentals

## // CURRENT ROUTE

Right now I'm spending most of my time on Cisco/CCNA concepts, Linux troubleshooting, AWS networking, Python automation, network observability, and defensive security.

I'm trying to get better at following a problem across layers instead of treating each tool as its own separate thing.

## // NEXT HOP

I'm working toward network and cloud engineering roles where troubleshooting is a big part of the job.

I'm especially interested in network operations, cloud support, infrastructure support, systems administration, and security-aware networking.

I'm based in North Alabama and especially interested in the Huntsville area.

## // UPLINK

[LinkedIn](https://www.linkedin.com/in/ashley-hopkins-432244329/) · [Architecture Journal](https://github.com/PatienceEnoch/Cloud-Network-Architecture-Journal) · [Portfolio](https://github.com/PatienceEnoch/Hopkins-portfolio)

---

<p align="center">
  <img src="https://raw.githubusercontent.com/PatienceEnoch/PatienceEnoch/main/assets/patience-waterfall-banner-github.jpg" alt="Patience beneath a waterfall" width="100%">
</p>

```console
patience@edge:~$ disconnect

Closing incident records............. [OK]
Saving field notes................... [OK]
Preserving packet captures........... [OK]
Leaving the network better understood [OK]

Connection closed.

Light in one hand.
Linux in the other.
```
