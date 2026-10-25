# 🦉 OAnsibleX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
