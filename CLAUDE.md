# CLAUDE.md — instructions for AI coding agents 🤖

This file guides AI coding agents working in this repository. The project
overview is in the [README](README.md) and the contribution conventions are
in [CONTRIBUTING](CONTRIBUTING.md); nothing there is repeated here.

---

## 🔭 Overview

A telemetry system on ESP-IDF v6.1 for the ESP32: sensor nodes take readings,
and a gateway collects them and forwards them to a database. The repository
has no code yet: the project is at the architecture stage.

---

## 🧰 Technology

* **Language:** C.
* **Framework:** ESP-IDF v6.1, with its bundled FreeRTOS.
* **Target:** `esp32`.

---

## 🔨 Build and Verify

* **Build:** `idf.py build` from the firmware folder, in a terminal with the ESP-IDF v6.1 environment active. Runs without asking: it never touches the hardware.
* **Flash and read the serial port:** only on the developer's explicit request — the board sits on the developer's bench, and an unexpected flash interrupts whatever is being tested.
* **Verification:** on the bench — the developer flashes the board and watches its behavior.

---

## 🔒 Security

* **Credentials stay out of git:** Wi-Fi passwords, database credentials and tokens never go into a tracked file — the repository is public, and a secret that reaches the history stays exposed even after it is deleted.

---

## 📐 Conventions

* **Terminology:** the board that collects the readings is the *gateway*; the boards that take them are *nodes* — in code, docs and commits alike.
* **Documentation:** describes the project's current state only, never the history of changes — readers need to know what the project is, and git already records what it was.
* **Version:** changes only when the developer sets a new one; the README badge and the firmware version change together, so they never disagree.

---

## 📚 Documentation Map

* **[README.md](README.md):** overview, hardware, and project status.
* **[CONTRIBUTING.md](CONTRIBUTING.md):** setup, workflow, and commit and comment conventions.
* **[LICENSE](LICENSE):** the MIT license.
