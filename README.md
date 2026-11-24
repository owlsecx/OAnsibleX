# 🦉 OAnsibleX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OAnsibleX** — Ansible Security Linter (Offline)

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OAnsibleX is an offline, read-only security linter for Ansible projects, covering ansible.cfg, inventories, playbooks, roles, group/host vars and Galaxy requirements. It ships its own stdlib-only YAML-lite parser and never executes or modifies the files it scans, making it safe to run in CI. Findings are mapped to CWE and MITRE ATT&CK with remediation and an overall score/grade.

---

## ✨ Features

- Stdlib-only YAML-lite parser (multi-doc, anchors/aliases, block scalars, !vault)
- Audits ansible.cfg, INI/YAML inventories, playbooks, roles and group/host vars
- Detects curl|bash, shell injection, disabled TLS verification and plaintext secrets
- Galaxy requirements review for unpinned versions and untrusted sources
- CWE + MITRE ATT&CK mapping, scoring/grade and inline suppression
- Exports TXT / Markdown / JSON / CSV / SARIF 2.1.0 with CI fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAnsibleX --path ./playbooks/
./OAnsibleX -p site.yml --format sarif -o report.sarif --fail-on high
./OAnsibleX --demo
./OAnsibleX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OAnsibleX --help   # watch every network call
firejail --net=none ./OAnsibleX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
