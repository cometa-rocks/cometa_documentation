# 📄 FOSS Disclosure – Docker, Redis 7.2.0, PostgreSQL 12.1, noVNC

This document lists all Free and Open-Source Software (FOSS) components used across Docker Engine, Redis 7.2.0, PostgreSQL 12.1, and noVNC.

---

# ✅ 1. Docker Engine (CE)

| Field | Value |
|------|--------|
| **FOSS Component Name** | Docker Engine (Community Edition) |
| **Version** | Varies with installation |
| **License** | Apache-2.0 |
| **Copyright** | © Docker, Inc. |
| **Source Code** | https://github.com/moby/moby |
| **Supply Source** | https://www.docker.com/ |
| **Reference Date** | – |

---

# ✅ 2. Redis Docker Image – redis:7.2.0

## Redis (Main Component)

| Field | Value |
|------|--------|
| **FOSS Component Name** | Redis |
| **Version** | 7.2.0 |
| **License** | BSD-3-Clause |
| **Copyright** | © Redis Ltd. |
| **Source Code** | https://github.com/redis/redis |
| **Supply Source** | https://hub.docker.com/_/redis |
| **Reference Date** | – |

## Debian Base System (Included in redis:7.2.0)

| Field | Value |
|------|--------|
| **FOSS Component Name** | Debian Base System |
| **Version** | Debian 12.x (Bookworm) |
| **License** | GPL-2.0, GPL-3.0, MIT, BSD, LGPL (varies per package) |
| **Copyright** | © Debian Project |
| **Source Code** | https://salsa.debian.org |
| **Supply Source** | Included via Docker Image |
| **Reference Date** | – |

## GNU Utilities

### GNU coreutils

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU coreutils |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/coreutils |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

### GNU bash

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU bash |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/bash |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

---

# ✅ 3. PostgreSQL Docker Image – postgres:12.1

## PostgreSQL (Main Component)

| Field | Value |
|------|--------|
| **FOSS Component Name** | PostgreSQL |
| **Version** | 12.1 |
| **License** | PostgreSQL License (similar to MIT) |
| **Copyright** | © PostgreSQL Global Development Group |
| **Source Code** | https://github.com/postgres/postgres |
| **Supply Source** | https://hub.docker.com/_/postgres |
| **Reference Date** | – |

## Debian Base System (Included in postgres:12.1)

| Field | Value |
|------|--------|
| **FOSS Component Name** | Debian Base System |
| **Version** | Debian 10.x (Buster) |
| **License** | GPL, LGPL, MIT, BSD (varies per package) |
| **Copyright** | © Debian Project |
| **Source Code** | https://salsa.debian.org |
| **Supply Source** | Included via Docker Image |
| **Reference Date** | – |

## GNU Utilities

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU coreutils, bash, shadow-utils |
| **Version** | Included via Debian |
| **License** | GPL-3.0 (bash, coreutils), GPL-2.0 (shadow-utils) |
| **Source Code** | https://www.gnu.org/software/coreutils<br>https://www.gnu.org/software/bash<br>https://github.com/shadow-maint/shadow |
| **Supply Source** | Included via Debian |
| **Reference Date** | – |

---

# ✅ 4. noVNC

| Field | Value |
|------|--------|
| **FOSS Component Name** | noVNC |
| **Version** | Latest available at integration time |
| **License** | MPL-2.0 |
| **Copyright** | © noVNC Contributors |
| **Source Code** | https://github.com/novnc/noVNC |
| **Supply Source** | https://github.com/novnc/noVNC/releases |
| **Reference Date** | – |

---

