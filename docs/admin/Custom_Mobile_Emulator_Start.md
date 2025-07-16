# Android Emulator Docker: `start.sh` Script Guide

This repository includes a flexible `start.sh` script to create and run Android Virtual Devices (AVDs) using Docker, with full control over device specs, emulator system image, display size, and rendering options.

---

## 🚀 Usage

```bash
./start.sh [--emulator_name=NAME] [--device=DEVICE_ID] [--api_level=LEVEL] [--target=TARGET] \
           [--arch=ARCH] [--screen_size=WxH] [--theme=THEME] [--gpu=GPU_MODE]
```

You can also use environment variables instead of CLI arguments. CLI arguments override environment variables.

---

## 📌 Options

| Option           | Description                                                                 | Default             | Example                            |
|------------------|-----------------------------------------------------------------------------|---------------------|------------------------------------|
| `--emulator_name`| AVD name to create or reuse                                                 | `nexus-test2`       | `--emulator_name=my_emulator`     |
| `--device`       | Device ID from `avdmanager list devices`                                    | `Nexus 6`           | `--device=pixel_4`                 |
| `--api_level`    | Android API level                                                           | `34`                | `--api_level=30`                   |
| `--target`       | System image tag                                                            | `google_apis`       | `--target=google_apis_playstore`  |
| `--arch`         | CPU architecture                                                            | `x86_64`            | `--arch=x86_64`                    |
| `--screen_size`  | Screen resolution (width x height)                                          | `1080x1920`         | `--screen_size=1440x2960`         |
| `--theme`        | Android UI theme                                                            | `light`             | `--theme=Holo`                     |
| `--gpu`          | GPU rendering mode (`host`, `swiftshader`, `swiftshader_indirect`, `off`)  | `swiftshader_indirect` | `--gpu=off`                     |

---

## 🌿 Environment Variable Support

You can also set any of the options as environment variables:

```bash
export DEVICE=pixel_4
export API_LEVEL=34
export GPU=off
./start.sh
```

Environment variables are used **only if** CLI options are not provided.

---

## 🧪 Examples

### Run default emulator (no flags)
```bash
./start.sh
```

### Run Pixel 4 on API 34 with GPU acceleration
```bash
./start.sh --emulator_name=pixel4emu --device=pixel_4 --api_level=34 --gpu=host
```

### Headless Docker usage
```bash
./start.sh --gpu=swiftshader_indirect
```

---

## 📋 Notes

- Run `avdmanager list devices` inside the container to get valid `--device` IDs.
- All system images are installed during Docker build. AVDs are created at runtime.
- `swiftshader_indirect` is ideal for headless containers (e.g., CI/CD or Docker).

---

## 📦 Docker Entry Point

In your `Dockerfile`, use:

```dockerfile
COPY start.sh /app/start.sh
RUN chmod +x /app/start.sh
CMD ["/app/start.sh"]
```

---

## 🛠 Troubleshooting

- If you get a `No device found matching` error, double-check the value for `--device` against `avdmanager list devices`.
- Use `--gpu=off` if you’re having GPU compatibility issues in Docker.

---

## 📞 Support

Feel free to open an issue or submit a pull request with improvements!

