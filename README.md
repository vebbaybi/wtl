# 🌀 WTL — Webbaby Type Loop

> Reactive storytelling and sequencing engine across languages and devices.

WTL (Webbaby Type Loop) is a universal timing and narrative engine designed by **Uchenna Anozie (webbaby)**.  
It orchestrates sequential text, events, or visual flows — from browser scrollytelling to Python scripts, CLI logs, embedded LEDs, and Flutter apps — using one shared core written in **Rust**.

---

## ✨ Core Idea

WTL is not just a loop — it’s a **temporal grammar**.  
You define a *timeline* (JSON, YAML, or code) describing events, text, or triggers.  
WTL runs that timeline deterministically across any host language, outputting structured callbacks (DOM, terminal, device, sound, anything).

### Example Concept
```json
{
  "tracks": [
    { "type": "text", "at": 0, "value": "Initializing system..." },
    { "type": "action", "at": 2, "value": "led:on" },
    { "type": "text", "at": 3, "value": "Sequence engaged." }
  ]
}
````

That same file runs in:

* a web page (via `wtl-wasm`)
* a Python console (via `wtl-py`)
* a microcontroller (via `wtl-ffi-c`)
* or a Flutter app (via `wtl-dart`)

---

## 🧩 Architecture

**Rust Core**

* `wtl-core` — engine, scheduler, and event system
* `wtl-model` — timeline and track types

**Language Bindings**

* `wtl-py` — Python (PyO3)
* `wtl-wasm` — WebAssembly (wasm-bindgen)
* `wtl-ffi-c` — universal C ABI
* `wtl-dart`, `wtl-go`, `wtl-jvm` — built on top of C ABI

**Tools**

* `wtl-cli` — CLI runner for testing and playback
* `wtl-inspector` — visual timeline debugger and editor

---

## 📦 Installation (planned)

**Rust**

```bash
cargo add wtl-core
```

**Python**

```bash
pip install wtl
```

**JavaScript**

```bash
npm install @the1807/wtl
```

**C / C++**

```c
#include "wtl.h"
```

**Flutter**

```yaml
dependencies:
  wtl:
    git: https://github.com/the1807/wtl.git
```

---

## 🧠 Development Structure

```text
core/           — Rust core logic
bindings/       — Language bindings (PyO3, WASM, FFI)
tools/          — CLI + Inspector
tests/          — Integration and fixture validation
docs/           — Specs, design, and roadmap
packaging/      — Release metadata for PyPI, NPM, Crates.io, Maven
```

Full structure is detailed in `/docs/design/architecture.md`.

---

## ⚙️ Build

```bash
# Build Rust core
cargo build

# Build Python binding
maturin develop -m bindings/wtl-py/Cargo.toml

# Build WebAssembly package
wasm-pack build bindings/wtl-wasm --target web

# Run core tests
cargo test
```

---

## 🧪 Status

| Component       | State          | Description                     |
| --------------- | -------------- | ------------------------------- |
| `wtl-core`      | 🧩 In progress | Core event engine and scheduler |
| `wtl-py`        | 🧠 Planned     | PyO3 wrapper for Python         |
| `wtl-wasm`      | 🌐 Planned     | Browser and Node.js WASM        |
| `wtl-cli`       | ⚙️ Planned     | CLI tool for timeline playback  |
| `wtl-inspector` | 🎛️ Planned    | Visual editor for timelines     |

---

## 🪶 License

This project is licensed under the **Apache License 2.0**.
You may freely use, modify, and distribute it with attribution.

See [`LICENSE`](./LICENSE) for details.

---

## 👤 Author

**Uchenna Anozie (webbaby)**
Computer Scientist • AI, Data, Embedded & Blockchain
🌐 [the1807.xyz](https://the1807.xyz)

---

## 🚀 Vision

WTL is built to become a **bridge between code and narrative**.
Wherever time and meaning meet — a scrollytelling page, a machine’s heartbeat, a command-line ritual — WTL speaks that rhythm.
Would you like me to generate the **Apache-2.0 LICENSE file** next (ready for commit)? It’s legally required to accompany the README.
```
