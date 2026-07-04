# VajraX v2.0.0

**Professional network engineering and cybersecurity toolkit — 68 tools, offline-first, Android.**

Built for network engineers, security professionals, and CCNA/CCNP/CCIE candidates who need production-grade calculators, config generators, and diagnostic tools without depending on internet connectivity or cloud services.

---

## What's New in v2.0

VajraX v2.0 adds **37 new tools** across 5 professional engines, upgrades **31 tools carried over from v1.0**, and introduces a signed release pipeline with reproducible builds.

### Engine 1 — Fabric Architect (9 tools)
Design and validate modern data center and WAN fabrics.
- VXLAN MTU Calculator
- TCP Window Scaling Modeler
- AWS/Azure CIDR Carver
- Route-Target & RD Planner
- EVPN-VXLAN Fabric Designer
- Spine-Leaf Underlay Designer
- BGP Path Analyzer Pro
- SD-WAN Policy Calculator
- WireGuard Config Generator

### Engine 2 — Config Intelligence (6 tools)
Analyze, generate, translate, and version-control device configurations.
- Config Analyzer
- Config Template Engine
- Multi-Vendor Translator Pro
- Config Vault
- Regex Filter Engine
- Config Diff Pro

### Engine 3 — Security Ops Center (9 tools)
Threat modeling, compliance, and cryptographic analysis.
- Zero Trust Architecture Planner Pro
- Firewall Policy Analyzer
- CVE Explorer Pro
- Log Parser & Analyzer
- IP Reputation & Threat Intel
- Certificate Chain Analyzer Pro
- Compliance Auditor Pro
- WPA3/WPA2 PMK Calculator
- DNSSEC Chain Validator

### Engine 4 — Live Network Ops (7 tools)
Real-time diagnostics and remote device access.
- SSH Terminal
- SNMP Browser Pro
- WiFi Analyzer Pro
- Network Scanner Pro
- Speed Test
- Wake-on-LAN Pro
- Advanced Ping & Traceroute

### Engine 5 — Protocol Deep Dive (6 tools)
Protocol references, encoding utilities, and packet analysis.
- Protocol Lab Pro
- RFC Browser (39 curated deep-dive entries)
- Multi-Vendor Command Reference Pro
- Encoder Toolkit
- Bitsmith Sandbox
- Hex Packet Decoder

### Carried Over from v1.0 — Upgraded (31 tools)

**Full 6-layer output added (20 tools):**
VLSM Planner, Subnet Hub, Subnet Troubleshooter, Network ID Architect, Route Summarizer, IPv6 Suite, IP Converter, Reverse VLSM, MTU/MSS Planner, Bandwidth Calculator, ACL Generator, IPv6 PD Planner, Universal Translator, Protocol Lab, DNS Lookup, Hash Generator, IP Camera Planner, CCTV Storage Calculator, Compliance Checker, Zero Trust Validator

**Export and cross-linking upgrades (11 tools):**
CIDR Cheat Sheet, Binary Heart, Cable Wiring Guide, MAC OUI Lookup, Port Reference, Field Options, Protocol Cheat Sheet, PoE Budget Calculator, Fiber Power Budget, VLAN Architecture Designer, Redundancy Planner

**Superseded by Pro versions (5 tools, redirect to their replacement):**
Tactical Manual → Multi-Vendor Command Reference Pro · Network Scanner → Network Scanner Pro · Ping & Traceroute → Advanced Ping & Traceroute · SSL Inspector → Certificate Chain Analyzer Pro · Config Diff → Config Diff Pro

---

## Tool Count

**68 functional tools** total (37 new + 31 carried over from v1.0's 31-tool baseline). This excludes 5 redirect stubs that point to a Pro replacement already counted above.

---

## Requirements

| | |
|---|---|
| Minimum Android version | 8.0 (API 26) |
| Target SDK | 35 (Android 15) |
| APK size | ~4.52 MB  |
| Signing | RSA-4096, APK Signature Scheme v2 |
| Internet required | No — fully offline. 8 tools connect to local network/devices when used: SSH Terminal, SNMP Browser Pro, WiFi Analyzer Pro, Network Scanner Pro, Speed Test, Wake-on-LAN Pro, Advanced Ping & Traceroute (Live Network Ops), and DNS Lookup (Command Center) |

---

## Installation

1. Download `VajraX-v2.0.0.apk` from the [Releases page](../../releases).
2. Enable "Install unknown apps" for your browser or file manager in Android Settings.
3. Open the downloaded APK and install.
4. Verify signature (optional but recommended): Expected: RSA 4096-bit, CN=VajraX, O=VajraX, C=IN, APK Signature Scheme v2.

Also available: [VajraX v1.0.0](https://github.com/VajraXcore/VajraX_Release) — the original 31-tool release, still supported for users who prefer the earlier feature set.

---

## Known Limitations

Disclosed here rather than discovered by users:

- **Route Summarizer** returns a `/32` summary for single-route input due to a short-circuit in the longest-common-prefix calculation. Not yet fixed.
- **VLSM Deaggregator** always clamps output to `/30` regardless of a smaller theoretical maximum prefix — a dead code path exists for `/31`/`/32` allocation that isn't currently reachable. Not yet fixed.
- **K8s CNI Policy Generator**, scoped in early planning, is not implemented in this release.
- **SD-WAN Full Overlay Designer** (full multi-site overlay design) is deferred to the planned Windows release. v2.0 ships the narrower-scope **SD-WAN Policy Calculator** instead.
- **RFC Browser** provides 39 curated deep-dive entries with abstracts and key points — not a full RFC archive. A separate, simpler 519-entry number+title reference table is available under Armory → Field Options.

---

## Changelog

### v2.0.0
- Added 5 new engines: Fabric Architect, Config Intelligence, Security Ops Center, Live Network Ops, Protocol Deep Dive (37 new tools)
- Upgraded 20 v1.0 tools with full 6-layer output (result, explanation, config example, related tools, warnings, export)
- Upgraded 11 v1.0 tools with export and cross-linking improvements
- Consolidated 5 legacy tools into their Pro replacements (with redirect for continuity)
- Introduced Config Vault, SSH Terminal, and SNMP Browser Pro for live device interaction
- Signed release pipeline with reproducible builds and public signature verification

### v1.0.0
See [VajraX_Release](https://github.com/VajraXcore/VajraX_Release) for the original changelog.

---

## Privacy

VajraX collects zero telemetry and zero analytics. All tools run fully offline except the 8 tools listed above (Live Network Ops' 7 tools, plus DNS Lookup), which only ever talk to devices on your local network or the host you point them at — nothing is sent to VajraX or any third party.

See the full [Privacy Policy](https://vajrax.in#privacy) for details.

## Contact

- **Website:** [vajrax.in](https://vajrax.in)
- **Email:** [pbr65.tech@gmail.com](mailto:pbr65.tech@gmail.com)

---

## License

Proprietary. VajraX is provided free of charge for personal and professional use, with no paywalls or in-app purchases. See repository for full terms.

© 2026 VajraXcore. All rights reserved.
