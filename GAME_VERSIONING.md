# Game Versioning Strategy

To ensure reliable, accurate, and long-term multiplayer compatibility across platforms, Multicore tracks and validates game versions using secure hashes and metadata. This strategy applies to all supported game types — console, handheld, PC, and emulator-based.

---

## 🎯 Purpose

Multicore’s multiplayer modules are designed to work with specific, known-good versions of each game. This preserves:

* Stable protocol matching
* Reproducible behavior across clients
* Compatibility across original hardware, modded systems, and emulators

---

## ✅ Version Matching System

Each supported game will be registered with:

* **Game Title**
* **Platform** (e.g. PS2, Xbox, PC)
* **Region** (e.g. USA, PAL, JPN)
* **File Type** (ISO, ROM, BIN, CHD, EXE, etc.)
* **MD5 or SHA-256 Checksum** (verifies correct version)
* **Multiplayer Status** (Supported, In Progress, Planned)
* Optional: Required patches or setup steps

This info will live in a public file: `SUPPORTED_GAMES.md` or `ISO_COMPATIBILITY.md`

---

## 🔄 Examples

| Game Title           | Platform | File Type | MD5 Checksum                     | Status         |
| -------------------- | -------- | --------- | -------------------------------- | -------------- |
| Halo: Combat Evolved | Xbox     | XISO      | 8A23DAF4D3F6A2C23B2E4F7B8940BBE2 | ✅ Supported    |
| TimeSplitters 2      | PS2      | ISO       | B3E9F5C28D770FE00DC83D1E7C018D54 | ⚠️ In Progress |
| Battlefield 2        | PC       | EXE       | 0C8A0D117BBF777A9033A5A90508B1D4 | 🧪 Testing     |

---

## 🔐 Legal and Ethical Use

* Multicore does **not** distribute ISOs, ROMs, or game files.
* Players must dump their own legally owned copies.
* Hashes are used only to confirm compatibility.

---

## 🛠️ Compatibility Flexibility

In the future, Multicore will:

* Support compatibility layers for patched versions
* Warn about mismatched hashes, but allow override if functionality is equivalent
* Use community-submitted metadata to expand support

---

## 💡 Why This Matters

Multiplayer preservation depends on consistency. Without versioning:

* Bugs multiply
* Protocols desync
* Servers crash

With this strategy, Multicore becomes the first open framework to:

* Validate and match multiplayer game versions across any platform
* Provide trust and clarity for players
* Support original hardware and emulators equally

---

*Versioning is preservation. Preservation is power.*
