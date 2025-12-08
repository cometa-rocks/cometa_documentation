# 📄 Cometa Scheduler – FOSS Disclosure 

This document identifies all Free and Open-Source Software (FOSS) components used in the **Cometa Scheduler Docker Image**, including the base OS image, system utilities, Python interpreter, and Python libraries installed via `requirements.txt`.

---

## 1. python:slim-bullseye (Base Image)

| Field | Value |
|------|--------|
| **FOSS Component Name** | python:slim-bullseye |
| **Version** | 3.12.x (latest at build time) |
| **License** | Python: PSF License<br>Debian OS components: GPL, LGPL, MIT, BSD (varies) |
| **Copyright** | © Python Software Foundation, © Debian Project |
| **Source Code** | https://github.com/docker-library/python |
| **Supply Source** | https://hub.docker.com/_/python |
| **Reference Date** | – |

---

## 2. Debian GNU/Linux Base System

| Field | Value |
|------|--------|
| **FOSS Component Name** | Debian GNU/Linux slim-bullseye |
| **Version** | 11.x (bullseye) |
| **License** | GPL-2.0, GPL-3.0, LGPL, MIT, BSD (varies per package) |
| **Copyright** | © Debian Project |
| **Source Code** | https://salsa.debian.org |
| **Supply Source** | https://www.debian.org/distrib/packages |
| **Reference Date** | – |

---

## 3. GNU coreutils

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU coreutils |
| **Version** | Provided by Debian base image |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/coreutils |
| **Supply Source** | Included via Debian base |
| **Reference Date** | – |

---

## 4. shadow-utils (useradd, groupadd)

| Field | Value |
|------|--------|
| **FOSS Component Name** | shadow-utils |
| **Version** | Provided by Debian base image |
| **License** | GPL-2.0 |
| **Copyright** | © shadow-utils contributors |
| **Source Code** | https://github.com/shadow-maint/shadow |
| **Supply Source** | Included via Debian base |
| **Reference Date** | – |

---

## 5. GNU bash

| Field | Value |
|------|--------|
| **FOSS Component Name** | GNU bash |
| **Version** | Provided by Debian base image |
| **License** | GPL-3.0 |
| **Copyright** | © Free Software Foundation |
| **Source Code** | https://www.gnu.org/software/bash |
| **Supply Source** | Included via Debian base |
| **Reference Date** | – |

---

## 6. Python Interpreter (CPython)

| Field | Value |
|------|--------|
| **FOSS Component Name** | CPython |
| **Version** | 3.12.x |
| **License** | PSF License |
| **Copyright** | © Python Software Foundation |
| **Source Code** | https://github.com/python/cpython |
| **Supply Source** | Included via python:slim image |
| **Reference Date** | – |

---

# 📦 Python Libraries Installed via requirements.txt

## APScheduler

| Field | Value |
|------|--------|
| **FOSS Component Name** | APScheduler |
| **Version** | 3.10.4 |
| **License** | MIT License |
| **Copyright** | © Alex Grönholm and contributors |
| **Source Code** | https://github.com/agronholm/apscheduler |
| **Supply Source** | https://pypi.org/project/APScheduler/ |
| **Reference Date** | – |

---

## certifi

| Field | Value |
|------|--------|
| **FOSS Component Name** | certifi |
| **Version** | 2024.2.2 |
| **License** | MPL-2.0 |
| **Copyright** | © Python Software Foundation |
| **Source Code** | https://github.com/certifi/python-certifi |
| **Supply Source** | https://pypi.org/project/certifi/ |
| **Reference Date** | – |

---

## charset-normalizer

| Field | Value |
|------|--------|
| **FOSS Component Name** | charset-normalizer |
| **Version** | 3.3.2 |
| **License** | MIT License |
| **Copyright** | © Ousret |
| **Source Code** | https://github.com/Ousret/charset_normalizer |
| **Supply Source** | https://pypi.org/project/charset-normalizer/ |
| **Reference Date** | – |

---

## idna

| Field | Value |
|------|--------|
| **FOSS Component Name** | idna |
| **Version** | 3.7 |
| **License** | BSD-3-Clause |
| **Copyright** | © Kim Davies |
| **Source Code** | https://github.com/kjd/idna |
| **Supply Source** | https://pypi.org/project/idna/ |
| **Reference Date** | – |

---

## pytz

| Field | Value |
|------|--------|
| **FOSS Component Name** | pytz |
| **Version** | 2024.1 |
| **License** | MIT License |
| **Copyright** | © Stuart Bishop |
| **Source Code** | https://github.com/stub42/pytz |
| **Supply Source** | https://pypi.org/project/pytz/ |
| **Reference Date** | – |

---

## requests

| Field | Value |
|------|--------|
| **FOSS Component Name** | Requests |
| **Version** | 2.31.0 |
| **License** | Apache-2.0 |
| **Copyright** | © Kenneth Reitz |
| **Source Code** | https://github.com/psf/requests |
| **Supply Source** | https://pypi.org/project/requests/ |
| **Reference Date** | – |

---

## six

| Field | Value |
|------|--------|
| **FOSS Component Name** | six |
| **Version** | 1.16.0 |
| **License** | MIT License |
| **Copyright** | © Benjamin Peterson |
| **Source Code** | https://github.com/benjaminp/six |
| **Supply Source** | https://pypi.org/project/six/ |
| **Reference Date** | – |

---

## tzdata

| Field | Value |
|------|--------|
| **FOSS Component Name** | tzdata |
| **Version** | 2024.1 |
| **License** | Apache-2.0 |
| **Copyright** | © IANA |
| **Source Code** | https://github.com/python/tzdata |
| **Supply Source** | https://pypi.org/project/tzdata/ |
| **Reference Date** | – |

---

## tzlocal

| Field | Value |
|------|--------|
| **FOSS Component Name** | tzlocal |
| **Version** | 5.2 |
| **License** | MIT License |
| **Copyright** | © Lothar Scholz |
| **Source Code** | https://github.com/regebro/tzlocal |
| **Supply Source** | https://pypi.org/project/tzlocal/ |
| **Reference Date** | – |

---

## urllib3

| Field | Value |
|------|--------|
| **FOSS Component Name** | urllib3 |
| **Version** | 2.2.1 |
| **License** | MIT License |
| **Copyright** | © urllib3 contributors |
| **Source Code** | https://github.com/urllib3/urllib3 |
| **Supply Source** | https://pypi.org/project/urllib3/ |
| **Reference Date** | – |

