<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>
<div align="center">
  <h1>Cometa - Complete Meta Test Platform</h1>
  <h4>Codeless & Code-Based Testing Across Systems. Cloud & On-Prem Ready.</h4>

  [![Docker Pulls](https://img.shields.io/docker/pulls/cometa/django?style=flat-square)](https://hub.docker.com/r/cometa/django)
  [![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg?style=flat-square)](https://www.gnu.org/licenses/agpl-3.0.html)
  [![GitHub Stars](https://img.shields.io/github/stars/cometa-rocks/cometa?style=social)](https://github.com/cometa-rocks/cometa/stargazers)
  [![Join](https://img.shields.io/discord/810822044367061042?label=Join%20our%20Community&logo=discord)](https://discord.gg/PUxt5bsRej)
  [![YouTube Demo](https://img.shields.io/badge/Watch-Demo-red?logo=youtube&style=flat-square)](https://youtu.be/s86rnmbLDpc)
  [![Twitter Follow](https://img.shields.io/twitter/follow/cometa_rocks?style=social)](https://twitter.com/cometa_rocks)
  [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)
  [![GitHub Issues](https://img.shields.io/github/issues/cometa-rocks/cometa?style=flat-square)](https://github.com/cometa-rocks/cometa/issues)
  [![GitHub PRs](https://img.shields.io/github/issues-pr/cometa-rocks/cometa?style=flat-square)](https://github.com/cometa-rocks/cometa/pulls)
  [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/cometa-rocks/cometa_documentation)

  <br/>
  <em>Created for DevOps, QA Engineers, SDETs, Developers & Business Teams</em>
</div>

---

## Admin Documentation

This section contains all the information needed for system administrators to deploy, configure, and maintain Cometa.

### Core Administrative Guides:

1. **System Administration**
   - [Deployment Guide](deployment.md) - Complete installation and setup guide
   - [User Management](#user-management) - Managing users, roles, and permissions
   - [System Configuration](#system-configuration) - Backend resources and configuration
   - [Backup & Recovery](#backup--recovery) - Data backup and restore procedures
   - [Security & Authentication](#security--authentication) - SSO setup and security best practices

2. **Maintenance & Monitoring**
   - [Browser Management](#browser-management) - Installing and managing browser versions
   - [System Resources](#hardware-requirements) - Hardware requirements and optimization
   - [Troubleshooting](#troubleshooting) - Common issues and solutions

---

## Quick Deployment

1. **Local Installation**
   ```bash
   git clone https://github.com/cometa-rocks/cometa.git
   cd cometa
   ./cometa.sh
   ```
   Access the UI at `https://localhost:443`

   - Default ports: 443 (HTTPS) and 80 (HTTP)
   - Customize ports in `docker-compose.yml` if needed
   - Installation typically completes in 8 minutes. If you face any issues, [contact us](#support)
   - In corporate environments, review Internet access and SSO provider setup requirements.

*See the [Deployment Guide](deployment.md) for manual installation steps and corporate environment requirements.*

---

## User Management

Cometa supports multiple user roles with granular permissions:

- **SUPERUSER/ADMIN**: Full system access, can manage all departments and users
- **DEVOPS**: Technical role with advanced capabilities
- **ANALYSIS**: Analysis and reporting focused role
- **Department Admin**: Department-specific administration rights

**Role Capabilities:**
- Access to edit departments
- User management within departments
- Feature creation and modification
- Test execution permissions
- Reporting and analysis access

**Department-Wise Administration:**
- Create department-specific admin roles
- Assign users to multiple departments
- Manage permissions at department level
- Share resources between departments

**Default Superuser:**
- Default superuser is created at runtime as `admin:admin`
- Create additional superusers via Django admin interface
- Access Django admin at `http://localhost:8000/admin`

**User Account Operations:**
- **GET** `/backend/api/accounts/` – Retrieve all accounts (requires permissions)
- **PATCH** `/backend/api/accounts/<user_id>/` – Modify account information
- **DELETE** `/backend/api/accounts/<user_id>/` – Delete user account
- **GET** `/backend/api/account_roles/` – Retrieve account roles

---

## System Configuration

**Backend Resources:**
- **Selenoid Grid**: `http://localhost:4444/wd/hub`
- **Selenoid Dashboard**: `http://localhost:4444/dashboard/`
- **Django Admin**: `http://localhost:8000/admin`

**Directory Layout:**
```
./behave                # Behave related files
./crontabs              # Crontab files for Django & Behave
./selenoid              # Selenoid related files
./front                 # Apache and Angular files
./src                   # Django related files
./src/backend           # Backend code for URLs
./src/cometa_pj         # Django configuration
./ws-server             # WebSocket server related files
```

**System Requirements:**
- **Minimum**: 16GB RAM, 8 CPUs, 28GB disk space
- **Recommended**: Higher specs for production
- **ulimit**: Set to 8192 for corporate environments using proxy
- **Server Time**: Must be synchronized with NTP (max 10-minute deviation)
- **Operating System**: Linux recommended (native environment)

---

## Security & Authentication

Cometa supports multiple SSO providers:

**Google OAuth Setup:**
1. Go to [Google Developer Console](https://console.cloud.google.com/)
2. Create an OAuth application
3. Add your domain to allowed hosts
4. Retrieve `client_id` and `secret_id`
5. Paste credentials in `./front/apache-conf/metadata/accounts.google.com.client`
6. Set `redirect_uri` to `https://<domain>/callback`

**GitLab OAuth Setup:**
1. Go to [git.amvara.de](https://git.amvara.de/)
2. Create a new account
3. Settings > Application > Add new application
4. Add your domain to allowed hosts
5. Retrieve `client_id` and `secret_id`
6. Paste credentials in `./front/apache-conf/metadata/accounts/git.amvara.de.client`
7. Set `redirect_uri` to `https://<domain>/callback`

**Corporate Environment Configuration:**

- Configure Docker to use corporate proxy:
  ```json
  {
    "proxies": {
      "default": {
        "httpProxy": "http://<host>:<port>",
        "httpsProxy": "http://<host>:<port>",
        "noProxy": "localhost,127.0.0.1,172.0.0.1/8,cometa_socket,cometa_zalenium,cometa_front,cometa_behave,cometa_django,cometa_postgres,behave"
      }
    }
  }
  ```
- Required domain whitelist:
  | **Domain** | **Reason** |
  |------------|------------|
  | git.amvara.de | GitLab-runner updates |
  | d.amvara.de | Discord notifications |
  | github.com, raw.githubusercontent.com | GitHub dependencies |
  | hub.docker.com | Docker images |
  | registry.npmjs.org | Node.js packages |
  | pypi.org | Python libraries |
  | deb.debian.org | Debian packages |

---

## Backup & Recovery

**Creating Backups:**
- Execute backup script from root folder:
  ```bash
  ./backup.sh
  ```
- Backup includes database, features metadata, screenshots, and is timestamped.

**Restoring Backups:**
1. Unzip `db_data.zip` and copy contents to folder `db_data`
2. Unzip `features.zip` and `screenshots.zip` directly inside behave folder
3. Restart containers: `docker-compose restart`

---

## Browser Management

**Installing Browser Versions:**
- Install latest browser versions (optional):
  ```bash
  ./backend/selenoid/deploy_selenoid.sh -n 3
  ```
- This configures and pulls the three newest Docker images with virtual browsers.

**Browser Configuration:**
- Selenoid images are the browsers available in Cometa
- Parse new browser images: `https://localhost/backend/parseBrowsers/`
- Support for BrowserStack, HeadSpin, or SauceLabs browsers (advanced setup)

---

## Troubleshooting

**Common Issues:**
- Installation typically takes 8-10 minutes
- If stuck for more than 5 minutes, contact support
- Check logs: `docker-compose logs -f --tail=10`

**Debug Mode:**
- Enable frontend debug mode:
  ```bash
  docker exec -it cometa_front bash
  root@cometa_front:/code# ./start.sh serve
  ```
- Access debug mode at `https://localhost/debug/`

**Import Actions:**
- On first start, manually parse actions:
  - Visit `https://localhost/backend/parseActions/`
  - Import option also available in Admin Section

---

## Support

We're here to support you:

- [Discord Community](https://discord.gg/PUxt5bsRej) – Join for instant access and support
- [YouTube Channel](https://www.youtube.com/channel/UCSne7hU1GRbg4cV0qWvD2Uw) – Video tutorials and demos
- [GitHub Issues](https://github.com/cometa-rocks/cometa/issues) – Report bugs and request features
- Email: [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

---

## 🧑‍🤝‍🧑 Sponsors

- Mercedes-Benz AG
- Daimler Trucks AG