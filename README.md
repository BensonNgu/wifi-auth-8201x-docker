# WiFi Authentication via 802.1X with Docker

This project demonstrates how to simulate WPA2-Enterprise (802.1X) Wi-Fi authentication using Docker, FreeRADIUS, and EAP-based credentials (username & password).

## 💡 Features
- Dockerized FreeRADIUS server
- Simple test user database
- CLI test using `radtest`
- Optional integration with hostapd (for real Wi-Fi simulation)
- Modular config files for quick customization

## 🧰 Tech Stack
- Docker
- FreeRADIUS
- 802.1X / EAP / RADIUS
- Bash / radtest (for testing)

## 🚀 Getting Started

### Prerequisites
- Docker + Docker Compose
- Linux or macOS (recommended for CLI tools)

### Quick Start

```bash
git clone https://github.com/your-username/wifi-auth-8021x-docker.git
cd /wifi-auth-8021x-docker/src
docker-compose up -d
```

### Test Authentication

```bash
docker exec -it freeradius radtest testuser secret123 localhost 0 testing123
```

## 📁 Directory Structure

* `freeradius/`: RADIUS server config and user database
* `tests/`: Shell scripts to automate testing
* `docs/`: Setup instructions, screenshots, extra explanations

## 📝 Example Users

```text
testuser  Cleartext-Password := "secret123"
```

## 📷 Screenshots

See [`docs/screenshots/`](docs/screenshots/) for visual setup steps.

## 📚 Resources

* [FreeRADIUS Docs](https://wiki.freeradius.org/)
* [802.1X Overview](https://en.wikipedia.org/wiki/IEEE_802.1X)
* [hostapd Setup](https://w1.fi/hostapd/)
