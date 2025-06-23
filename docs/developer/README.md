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

## 🔍 Developer Documentation

This section contains all the information needed for developers to integrate with and extend Cometa.

### Core Developer Guides:

1. **API Integration**
   - [REST API](REST-API.md) - Complete API reference for automation and integration
   - [Contributing Guidelines](CONTRIBUTING.md) - How to contribute to the Cometa project

2. **Development Setup**
   - [Local Development Environment](CONTRIBUTING.md) - Setting up Cometa for development
   - [Code Standards](CONTRIBUTING.md) - Coding guidelines and best practices

3. **Architecture & Extensions**
   - [System Architecture](CONTRIBUTING.md) - Understanding Cometa's architecture
   - [Plugin Development](CONTRIBUTING.md) - Creating custom plugins and extensions
   - [API Client Libraries](REST-API.md) - Available client libraries and SDKs

4. **Testing & Quality Assurance**
   - [Testing Framework](CONTRIBUTING.md) - Running tests and quality checks
   - [Performance Testing](REST-API.md) - API performance and load testing
   - [Security Testing](REST-API.md) - Security considerations and testing

5. **Deployment & Operations**
   - [Deployment Guide](../admin/deployment.md) - Production deployment instructions
   - [Configuration Management](CONTRIBUTING.md) - Environment configuration
   - [Monitoring & Logging](REST-API.md) - System monitoring and debugging

6. **Community & Support**
   - [GitHub Issues](https://github.com/cometa-rocks/cometa/issues) - Report bugs and request features
   - [Discord Community](https://discord.gg/PUxt5bsRej) - Developer discussions and support
   - [Code of Conduct](CONTRIBUTING.md) - Community guidelines

---

## 🚀 Quick Start for Developers

1. **Fork and Clone**
   ```bash
   git clone https://github.com/your-username/cometa.git
   cd cometa
   ```

2. **Setup Development Environment**
   ```bash
   # Install dependencies
   pip install -r requirements.txt
   
   # Setup database
   python manage.py migrate
   
   # Run development server
   python manage.py runserver
   ```

3. **Access Development UI**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:8000`
   - Admin Panel: `http://localhost:8000/admin`

> [!NOTE]
> - Check [CONTRIBUTING.md](CONTRIBUTING.md) for detailed setup instructions
> - Ensure you have Docker and Docker Compose installed for full functionality
> - Join our [Discord](https://discord.gg/PUxt5bsRej) for developer support

---

## 🧑‍💻 Contributing

We welcome contributions from the developer community! Here's how to get started:

### Getting Started
1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes** following our [coding standards](CONTRIBUTING.md)
4. **Test your changes** thoroughly
5. **Submit a pull request** with a clear description

### Development Workflow
```bash
# Fork and clone
git clone https://github.com/your-username/cometa.git
cd cometa

# Create feature branch
git checkout -b feature/your-feature-name

# Make changes and test
python manage.py test

# Commit with conventional commits
git commit -m "feat: add new API endpoint for user management"

# Push and create PR
git push origin feature/your-feature-name
```

### What We're Looking For
- **Bug fixes** and performance improvements
- **New features** and enhancements
- **Documentation** improvements
- **Test coverage** additions
- **API extensions** and integrations

See our [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## 🔧 Development Tools

### Required Tools
- **Python 3.8+** - Backend development
- **Node.js 16+** - Frontend development
- **Docker & Docker Compose** - Containerization
- **Git** - Version control

### Recommended Tools
- **VS Code** - IDE with Python and JavaScript extensions
- **Postman** - API testing
- **DBeaver** - Database management
- **Chrome DevTools** - Frontend debugging

### Development Commands
```bash
# Run tests
python manage.py test

# Check code style
flake8 .
black .

# Run linting
pylint cometa/

# Build Docker image
docker build -t cometa:dev .
```

---

## 🧑‍🤝‍🧑 Sponsors

- **Mercedes-Benz AG**
- **Daimler Trucks AG**

---

## 🆘 Need Help?

We're here to support developers:

- [Discord Community](https://discord.gg/PUxt5bsRej) - Developer discussions and support
- [GitHub Issues](https://github.com/cometa-rocks/cometa/issues) - Report bugs and request features
- [GitHub Discussions](https://github.com/cometa-rocks/cometa/discussions) - Ask questions and share ideas
- Email: [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)
