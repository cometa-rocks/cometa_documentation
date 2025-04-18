<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>
<div align="center">
  <h1>Cometa - Complete Meta Test Automation</h1>
  <h4>Codeless & Code-Based Testing Across Systems. Cloud & On-Prem Ready.</h4>

  [![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg?style=flat-square)](https://www.gnu.org/licenses/agpl-3.0.html)
  [![GitHub Stars](https://img.shields.io/github/stars/cometa-rocks/cometa?style=social)](https://github.com/cometa-rocks/cometa/stargazers)
  [![Join our Community on Discord](https://img.shields.io/discord/810822044367061042?label=Join%20our%20Community&logo=discord)](https://discord.gg/PUxt5bsRej)
  [![YouTube Demo](https://img.shields.io/badge/Watch-Demo-red?logo=youtube&style=flat-square)](https://www.youtube.com/watch?v=VIDEO_ID)



  <br/>
  <em>Created for DevOps, QA Engineers, SDETs, Developers & Business Teams</em>
</div>

---

## 🚀 What is Cometa?

**Cometa** stands for **Complete Meta Test Platform** — a versatile, powerful testing solution that lets you run automated tests **across system boundaries** using either a **codeless editor** or **full-code mode**, on cloud or on-prem.

> _Meta_ comes from the Greek “μετά-” meaning "beyond" — and that’s exactly what Cometa enables.

**With Cometa, you can:**
- Fetch data from one system and test it in another.
- Create scalable test plans with reusable features.
- Use BDD-style tests with [Behave](https://github.com/behave/behave) + Selenium.
- View results with logs, screenshots, videos.
- Consume results via a REST API or a beautiful Angular UI.

---

## ⚡ Key Features

- ✅ No-code + full-code test creation
- 🔁 Cross-system test flows
- 🧠 Over 70 prebuilt test steps
- 📸 Screenshots & video capture
- 🌍 Cloud & on-prem deployments
- 🔐 OIDC Security (Google, GitLab OAuth, more)
- 📦 REST API for integration & CI/CD
- 🧪 BDD syntax with Behave + Selenium WebDriver
- 📊 Visual result dashboards

---

## ✨ Quick Start

Get started with Cometa Community Edition:

```bash
# 1. Clone the repo
git clone https://github.com/cometa-rocks/cometa.git

# 2. Follow setup instructions
cd cometa
# (install dependencies, start services, etc.)

# 3. Launch the UI
http://localhost:4200

# 4. Import your first test
Use the UI > Import JSON and try [feature_example_your_first_testcase.json](examples/feature_example_your_first_testcase.json)
```

📖 Full guide: [Your First Test](#your-first-test)

---

## 🧭 Table of Contents

<details>
<summary>📦 Versions</summary>

- [Cometa Versions](main?tab=readme-ov-file#-cometa-versions)
- [Cometa History](#cometa-history)

</details>

<details>
<summary>🚀 Getting Started</summary>

- [Overview: 5W1H](#cometa-overview---5w1h)
- [What is a Testplan / Feature](#what-is-a-testplan-versus-feature)
- [Your First Test](#your-first-test)
- [All About Cometa Steps](#all-about-cometa-steps)
- [All About Selectors](#all-about-selectors)
- [Data Driven Testing (DDT)](#data-driven-testing-ddt)
- [Execute JavaScript](#execute-your-own-javascript)
- [Compare Values Across Systems](#compare-the-values-of-two-selectors-over-system-boundaries)
- [Create Sub-Features](#create-a-sub-features)
- [Upload & Download Files](#upload-and-download-files)
- [Step Timeouts](#step-timeouts)
</details>

<details>
<summary>🔌 Integrations</summary>

- [Integration with Webhooks](#integration-with-webhooks)
- [Integration with GitHub/GitLab](#integration-with-gitlab--github)
- [REST API](#rest-api)
</details>

<details>
<summary>🔐 Operations & Maintenance</summary>

- [Security](#security)
- [Housekeeping](#housekeeping)
</details>

<details>
<summary>💬 Community & Help</summary>

- [Sponsors](#sponsors)
- [Want to Help?](#want-to-help-with-cometa-development)
- [Need Help?](#you-are-stuck-and-need-some-help)
- [Design, Fonts & Logos](#design)
</details>

---

## 🔀 Cometa Versions

### 🧪 Community Edition (CE)
- Open-source on GitHub ([repo](https://github.com/cometa-rocks/cometa))
- Lags behind premium features
- Free under [AGPLv3](#license)

### ☁️ Cloud Enterprise Edition (CEE)
- Fully hosted, 4-tier plans: Standard, Silver, Gold, Enterprise
- Details upon request

### 🏢 On-Prem Enterprise Edition (EE)
- All Cloud features + more
- Includes onboarding, unlimited users, advanced browser support, priority support

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

Here are some direct links to core guides:

- 🧱 [Cometa Features](docs/cometa_features.md)
- 🧩 [Step Library](docs/cometa_actions.md)
- 🧠 [Selectors Guide](docs/css-xpath.md)
- 🔧 [REST API](docs/REST-API.md)
- ❓ [FAQ](FAQ.md)
- ❓ [Questions](questions.md)

---

## 🧑‍💻 Want to Contribute?

We’d love your help to improve Cometa! Start with:
```bash
# Fork the repo
# Make your changes
# Submit a pull request ✨
```
See [`CONTRIBUTING.md`](CONTRIBUTING.md) (coming soon).

---

## 🧑‍🤝‍🧑 Sponsors

- **Mercedes-Benz AG**
- **Daimler Trucks AG**

---

## 🆘 Need Help?

We’re here to support you:

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
See [Logos Section](#design) for all supported formats.

---

## 📄 License

Licensed under **AGPLv3**. See [`LICENSE`](https://github.com/cometa-rocks/cometa_documentation/blob/main/LICENSE) for details.
