# Contributing to ESP32 Sensor Network

This guide covers what you need to work on the project: the tools, the path
of a change, and the commit and comment conventions. The project overview is
in the [README](README.md).

---

## ⚙️ Setting Up

* **Requirement:** ESP-IDF v6.1, with its environment active in the terminal.
* **Editor:** any editor with EditorConfig support picks up the project's formatting from `.editorconfig`.
* **Build**, from the firmware folder:
  ```bash
  idf.py build
  ```
* **Flash and watch the serial output:**
  ```bash
  idf.py -p <PORT> flash monitor
  ```

---

## 🔀 Workflow

1. Every change starts from an issue, opened from one of the issue templates.
2. A larger feature gets its own branch from `main`: `feature/<name>`.
3. Each of its issues gets a branch from the feature branch:
   `feature/<N>-<subject>` (or `fix/`, `docs/`).
4. One commit per issue, made after the change is verified on the bench.
5. The issue branch joins the feature branch by fast-forward; the feature
   branch joins `main` through a pull request.

```
main ─────────────────────────────●──── (pull request)
  └─ feature/<name> ──●──●──●────┘
         └─ feature/<N>-<subject> (one commit each)
```

---

## 📝 Commit Convention

[Conventional Commits](https://www.conventionalcommits.org/), in English:

```
<type>: <short imperative description, no final period>

Closes #<issue>
```

* **Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`, `build`, `ci`, `revert` — no scope in parentheses.
* **Body:** only when the reason is not obvious from the issue.

Example:

```
feat: add temperature reading to the node

Closes #3
```

---

## 💬 Comment Convention

* Comments are in English.
* No references to issues or tasks in the code: the link between a change and its issue lives in the commit.

---

## 📚 Where Each Document Lives

* **[README.md](README.md):** overview, hardware, and project status.
* **CONTRIBUTING.md:** this guide — setup, workflow, and conventions.
* **[SECURITY.md](SECURITY.md):** how to report a vulnerability privately.
* **[LICENSE](LICENSE):** the MIT license.
* **[CLAUDE.md](CLAUDE.md):** instructions for AI coding agents working in the repository.
* **[.github/](.github/):** issue and pull request templates.
