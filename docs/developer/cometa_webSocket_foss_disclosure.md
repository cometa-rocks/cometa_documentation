# 📄 Cometa Web-Socket – FOSS Disclosure 

This document lists all Free and Open-Source Software (FOSS) components used in the **Cometa Web-Socket Server**, including NPM dependencies, Docker base image components, and system utilities included in the final container.

---

# 🟦 1. Base Image & OS Components

## 1. node:22 (Base Image)

| Field | Value |
|------|--------|
| **FOSS Component Name** | node:22 |
| **Version** | 22.x LTS |
| **License** | Node.js: MIT<br>Debian Linux: GPL, LGPL, MIT, BSD (varies per package) |
| **Copyright** | © Node.js Foundation, © Debian Project |
| **Source Code** | https://github.com/nodejs/node |
| **Supply Source** | https://hub.docker.com/_/node |
| **Reference Date** | – |

---

## 2. Debian GNU/Linux Base System

| Field | Value |
|------|--------|
| **FOSS Component Name** | Debian Base System |
| **Version** | 12.x (Bookworm) |
| **License** | GPL-2.0, GPL-3.0, LGPL, MIT, BSD (package-dependent) |
| **Copyright** | © Debian Project |
| **Source Code** | https://salsa.debian.org |
| **Supply Source** | https://www.debian.org/distrib/packages |
| **Reference Date** | – |

---

## 3. GNU Bash

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU bash |
| **Version** | Provided by Debian base |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/bash |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

---

## 4. GNU coreutils

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU coreutils |
| **Version** | Provided by Debian base |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/coreutils |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

---

## 5. shadow-utils (useradd, groupadd)

| Field | Value |
|------|--------|
| **FOSS Component Name** | shadow-utils |
| **Version** | Provided by Debian base |
| **License** | GPL-2.0 |
| **Copyright** | © shadow-utils maintainers |
| **Source Code** | https://github.com/shadow-maint/shadow |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

---

# 🟧 2. Global NPM Packages Installed via Dockerfile

## 6. PM2 (Global Installation)

| Field | Value |
|------|--------|
| **FOSS Component Name** | PM2 |
| **Version** | 5.2.2 |
| **License** | AGPL-3.0-only |
| **Copyright** | © Keymetrics |
| **Source Code** | https://github.com/Unitech/pm2 |
| **Supply Source** | https://www.npmjs.com/package/pm2 |
| **Reference Date** | – |

---

# 🟩 3. Application Dependencies (from package.json)

## 7. body-parser

| Field | Value |
|------|--------|
| **FOSS Component Name** | body-parser |
| **Version** | ^1.19.0 |
| **License** | MIT License |
| **Copyright** | © Express body-parser contributors |
| **Source Code** | https://github.com/expressjs/body-parser |
| **Supply Source** | https://www.npmjs.com/package/body-parser |
| **Reference Date** | – |

---

## 8. crypto (NPM module)

| Field | Value |
|------|--------|
| **FOSS Component Name** | crypto (NPM package) |
| **Version** | ^1.0.1 |
| **License** | ISC License |
| **Copyright** | © crypto package authors |
| **Source Code** | https://github.com/npm/security-holder |
| **Supply Source** | https://www.npmjs.com/package/crypto |
| **Reference Date** | – |

---

## 9. express

| Field | Value |
|------|--------|
| **FOSS Component Name** | Express |
| **Version** | ^4.17.1 |
| **License** | MIT License |
| **Copyright** | © Express contributors |
| **Source Code** | https://github.com/expressjs/express |
| **Supply Source** | https://www.npmjs.com/package/express |
| **Reference Date** | – |

---

## 10. morgan

| Field | Value |
|------|--------|
| **FOSS Component Name** | morgan |
| **Version** | ^1.10.0 |
| **License** | MIT License |
| **Copyright** | © Morgan contributors |
| **Source Code** | https://github.com/expressjs/morgan |
| **Supply Source** | https://www.npmjs.com/package/morgan |
| **Reference Date** | – |

---

## 11. PM2 (Local Dependency)

| Field | Value |
|------|--------|
| **FOSS Component Name** | PM2 |
| **Version** | ^5.2.2 |
| **License** | AGPL-3.0-only |
| **Source Code** | https://github.com/Unitech/pm2 |
| **Supply Source** | https://www.npmjs.com/package/pm2 |
| **Reference Date** | – |

---

## 12. socket.io

| Field | Value |
|------|--------|
| **FOSS Component Name** | socket.io |
| **Version** | ^4.1.2 |
| **License** | MIT License |
| **Copyright** | © Socket.IO contributors |
| **Source Code** | https://github.com/socketio/socket.io |
| **Supply Source** | https://www.npmjs.com/package/socket.io |
| **Reference Date** | – |

---

