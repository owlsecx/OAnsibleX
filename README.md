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

Offline Ansible playbook, role, inventory & ansible.cfg security linter

---

## ✨ Features

- Stdlib-only YAML-lite parser — multi-document, lists of maps, block scalars (| > with chomping), flow collections, anchors/aliases/merge, !vault tags
- ansible.cfg auditor — host_key_checking, log_path, vault_password_file, world-readable tmpfiles, callback leaks, pipelining/requiretty, ssh_args ...
- INI + YAML inventory auditor — plaintext ansible_password / become / ssh pass (masked), StrictHostKeyChecking=no, root SSH user, WinRM
- Playbook / role / task linter — curl|bash, shell injection, validate_certs, http URLs, GPG bypass, world-writable modes, plaintext user passwords, missing no_log, SELinux/firewall disabling, ...
- group_vars / host_vars secret detection vs $ANSIBLE_VAULT; headers, private keys, cloud keys
- Galaxy requirements — version pins, git commits, untrusted collection sources
- CWE + MITRE ATT&CK mapping, remediation, score/grade
- Inline suppression # oansiblex:ignore=ID
- Export TXT / MD / JSON / CSV / SARIF 2.1.0
- Self-test --demo (weak vs hardened projects)
- Full CLI mode (--path, --fail-on, --explain ...) Read-only: never modifies scanned files.

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OAnsibleX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
