# ESP32 Sensor Network — gateway/node telemetry 📡

[![Hardware](https://img.shields.io/badge/Hardware-ESP32-blue.svg)](https://www.espressif.com/en/products/socs/esp32)
[![Firmware](https://img.shields.io/badge/Firmware-ESP--IDF%20v6.1-green.svg)](https://www.espressif.com/en/products/sdks/esp-idf)
[![Version](https://img.shields.io/badge/Version-0.1.0-brightgreen.svg)](https://github.com/jhowsbDiem/ESP32-Sensor-Network)

ESP32 Sensor Network is a telemetry system written in C on ESP-IDF: ESP32
sensor nodes take readings, and an ESP32 gateway collects them and forwards
them to a database. The repository holds the whole system — the gateway
firmware, the node firmware, and the path from the gateway to the database.

---

## 🛠️ Hardware Specifications

* **Microcontroller:** ESP32 — on the gateway and on every node.

---

## 🤝 Contributing

Workflow, commit and comment conventions are in
[`CONTRIBUTING.md`](CONTRIBUTING.md).

---

## 📊 Project Status

### ⏳ In Progress
* **System architecture:** choosing the gateway–node link, the sensors, and the message format.

### 🗺️ Planned Next Steps
* **Node firmware:** each node reads its sensors and sends the readings to the gateway.
* **Gateway firmware:** the gateway receives the readings from every node.
* **Database upload:** the gateway forwards the readings it receives to a database.
* **Code quality:** automatic builds on GitHub Actions for every pull request, automated tests running on the host, and formatting with `clang-format`.

---

## ✒️ Authors and License

* **Developer:** Jonathan dos Santos Bezerra.
* **License:** MIT — see [LICENSE](LICENSE).
