
# 🚀 Cometa Documentation

**Cometa** is the AI-native testing framework that empowers developers to write, manage, and scale end-to-end tests with LLMs. Designed for modern workflows and GitHub integration, Cometa enables you to test like never before—autonomously, intelligently, and fast.

---

## ✨ Features

- ✅ **AI-Powered Test Automation**  
  Write tests in plain language—Cometa interprets and executes them with precision.

- 🌐 **GitHub Integration**  
  Runs seamlessly within your GitHub Actions for PR checks and CI/CD workflows.

- ⚙️ **Multi-Browser & Device Support**  
  Run your tests across different browsers and device profiles with ease.

- 🔁 **Self-Correcting Test Engine**  
  Uses LLMs to automatically fix failing test steps and retry smartly.

- 📊 **Visual Reports**  
  Get rich, visual test reports directly in your pull request or pipeline.

---

## 🧠 How It Works

```bash
# 1. Install Cometa
npm install -g cometa

# 2. Initialize your first test
cometa init

# 3. Run tests
cometa test
```

---

## 🔧 Example Test

```yaml
name: Login Test
steps:
  - open: https://example.com
  - type: "my username" into "#username"
  - type: "my password" into "#password"
  - click: "Login"
  - expect: "Welcome back" to be visible
```

---

## 🧪 GitHub Integration

Cometa plays nice with GitHub Actions. Simply add the following to your workflow:

```yaml
- name: Run Cometa Tests
  uses: cometa-rocks/cometa-action@v1
  with:
    config: path/to/cometa.yml
```

---

## 📚 Documentation

All docs are in this repository! Head to the [`docs/`](./docs) folder for full guides, examples, and API reference.

---

## 📢 Join the Community

- 💬 [Discord]( https://discord.gg/PUxt5bsRej)  
- 📣 [Follow us on Twitter](https://twitter.com/cometa_rocks)  
- 🌍 [cometa.rocks](https://cometa.rocks)

---

## 🛠️ Contributing

We welcome contributions! Check out [`CONTRIBUTING.md`](./CONTRIBUTING.md) to get started.

---

## 📄 License

Cometa.Rocks is licensed under AGPLv3 - see details in `LICENSE`(https://github.com/cometa-rocks/cometa_documentation/blob/main/LICENSE)
