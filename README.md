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

Offline PHP runtime configuration (php.ini / PHP-FPM) hardening auditor

---

## ✨ Features

- Offline, read-only parser for php.ini and conf.d/*.ini (sections, quoting, constants, booleans, size suffixes)
- Effective-value resolution across the PHP load order (php.ini → conf.d sorted → FPM pool → .user.ini/.htaccess)
- Auto-discovery of /etc/php/<ver>/{fpm,cli,apache2,cgi}, /etc/php.ini, /etc/php.d, /usr/local/etc/php, php-fpm.d
- 80+ rules: error exposure, RFI, disable_functions gap scoring, open_basedir, uploads, session cookie flags, sid entropy, cgi.fix_pathinfo, enable_dl, prepend files, DoS limits, assertions, OPcache, phar, FFI, Xdebug, deprecated/removed directives per PHP version
- PHP-FPM auditor: TCP listen exposure, socket modes, root workers, limit_extensions, pm limits, status / ping paths, clear_env, secrets in env[], admin overrides
- .user.ini / .htaccess override auditor with INI changeable-mode awareness (SYSTEM / PERDIR / ALL)
- CWE + OWASP mapping, severity, remediation per rule
- Weighted 0–100 score and A+…F grade
- Hardened php.ini / pool template generator
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- CI mode: --min-severity, --fail-on (exit 2)
- Self-test --demo (weak vs hardened, exit 3 on miss)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPhpIni
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
