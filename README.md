# 🦉 OPhpIni

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPhpIni** — PHP Runtime Configuration Hardening Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPhpIni is an offline, read-only auditor for PHP runtime configuration. It parses php.ini, conf.d directories, PHP-FPM pools, .user.ini and .htaccess files and resolves effective directive values across the PHP load order. Findings are scored and mapped to CWE and OWASP references.

---

## ✨ Features

- Offline parser for php.ini and conf.d/*.ini with effective-value resolution across the load order
- Auto-discovery of PHP installation directories under a configurable root
- 80+ rules covering error exposure, RFI, uploads, session cookies, OPcache, FFI and more
- PHP-FPM auditor for listen exposure, socket modes, worker users and pm limits
- CWE/OWASP mapping with severity profiles for production and development
- Effective-value printing, remediation overlays, hardened templates and multiple export formats

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPhpIni --scan --root /
./OPhpIni --ini /etc/php/8.3/fpm/php.ini --fpm /etc/php/8.3/fpm/php-fpm.conf
./OPhpIni --ini php.ini --format json -o report.json
./OPhpIni --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
