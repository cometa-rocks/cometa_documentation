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

## 🚀 What is Cometa?

**Cometa** stands for **Complete Meta Test Platform** — a versatile, powerful testing solution that lets you run automated tests **across system boundaries** using either a **codeless editor** or **full-code mode**, on cloud or on-prem.

> _Meta_ comes from the Greek "μετά-" meaning "beyond" — and that's exactly what Cometa enables.
## One More Thing...

Imagine a world where testing isn't just about finding bugs. It's about creating perfect user experiences, across every system, every time. That's Cometa.

## Why Cometa?

**Because testing should be:**
- **Simple**: No-code or full-code, your choice
- **Powerful**: Test across any system, any boundary
- **Beautiful**: Results that tell a story
- **Smart**: AI-powered, future-ready
  

> [!TIP]
>
> **With Cometa, you can:**
> - Fetch data from one system and test it in another  
> - Create scalable test plans with reusable features  
> - Use BDD-style tests with Behave and Selenium  
> - View results with logs, screenshots, and videos  
> - Access results via a REST API or a beautiful Angular UI
> - Combine Browser, API, mobile and native desktop testing in a single feature
> - Use AI to generate tests in natural language

Read more in the detailed overview of [Cometa Features](docs/user/cometa_features.md)


## Quick Start

1. **Join Discord Community**
   - [Join our Discord](https://discord.gg/e3uBKHhKW5) for instant access to Co.Meta (for free of course)
   - Ask for invitation link
   - No installation required

2. **Local Installation**
   ```bash
   git clone https://github.com/cometa-rocks/cometa.git
   cd cometa
   ./cometa.sh
   ```
   Access the UI at `https://localhost:443`

> [!NOTE]
> - Default ports: 443 (HTTPS) and 80 (HTTP)
> - Customize ports in `docker-compose.yml` if needed
> - Installation typically completes in 8 minutes. If you face any issues [contact us](#-need-help)
> - In corporate environments there are some things to know regarding Internet access as well as SSO provider setup.

*Check our [Deployment guide](docs/admin/deployment.md) for manual installation steps and corporate environments requirements.*


📖 Full guide: [Your First Test](docs/user/GETTING_STARTED.md)

---

## 🔀 Choose Your Path

### Community Edition
- Open-source on GitHub
- Free forever under [AGPLv3](LICENSE)
- [Get started now](https://github.com/cometa-rocks/cometa)

### Enterprise
- Fully managed on cloud / on-prem / hybrid
- Access to advanced features and dedicated support
- Unlimited users [usage subject to hardware configuration]
- [Let's talk](mailto:tec_dev@cometa.rocks,sales@cometa.rocks)

---

## 📜 Cometa History

| Year | Milestone |
|------|-----------|
| 2014 | PoC with Daimler |
| 2016 | Version 0.1 |
| 2018 | Production rollout |
| 2019 | Second PoC |
| 2020 | Smart step enhancements |
| 2021 | Public GitHub repo |
| 2022 | Enterprise pilots |
| 2023 | Formation of global legal entity |
| 2024 | Roadmap: AI selectors, Load Testing, Chrome CDP metrics |

---

## 🔍 Explore the Docs
### Core guides for:
<details>
<summary><strong>Admins</strong></summary>

1. Deployment
   - [Deployment Guide](docs/admin/deployment.md)
</details>

<details>
<summary><strong>Developers</strong></summary>

1. API Documentation
   - [REST API](docs/developer/REST-API.md)
</details>

<details>
<summary><strong>Users</strong></summary>

1. First Steps
   - [Getting Started](docs/user/GETTING_STARTED.md)
   - [Feature Example: Your First Testcase](docs/user/feature_example_your_first_testcase.json)

2. Core Concepts
   - [Cometa Features](docs/user/cometa_features.md)
   - [Cometa Actions](docs/user/cometa_actions.md)
   - [Cometa Selectors](docs/user/cometa_selectors.md)

3. Advanced Features
   - [Mobile Feature](docs/user/mobile_feature.md)
   - [AI Feature](docs/user/ai_feature.md)
   - [Load Testing](docs/user/LOAD_TESTING.md)

4. Authentication
   - [MFA Authentication Preparation](docs/user/mfa_authentication_preparation.md)
   - [MFA Authentication Using Cometa](docs/user/mfa_authentication_using_cometa.md)

5. Support
   - [Tutorials](docs/user/TUTORIALS.md)
   - [FAQ](docs/user/FAQ.md)
   - [Additional Questions](docs/user/questions.md)
</details>

## 🧑‍💻 Want to Contribute?

We'd love your help to improve Cometa! Start with:
```bash
# Fork the repo
# Make your changes
# Submit a pull request ✨
```
See [`CONTRIBUTING.md`](CONTRIBUTING.md)

---

## 🧑‍🤝‍🧑 Sponsors

- **Mercedes-Benz AG**
- **Daimler Trucks AG**

---

## 🆘 Need Help?

We're here to support you:

📫 Email: [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)  
💬 Discord: [Join us](https://discord.gg/e3uBKHhKW5)

---

## 🎨 Design

### Fonts
- **Primary:** Comfortaa
- **Secondary:** Montserrat

### Colors
- Orange: `#f4b829`
- Black: `#191919`

### Logos
See [Logos Section](img/logos) for all supported formats.

---
