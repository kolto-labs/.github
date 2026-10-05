```
  ██  ██   ████   ██      ██████   ████       ██       ████   █████    █████
  ██ ██   ██  ██  ██        ██    ██  ██      ██      ██  ██  ██  ██  ██
  ████    ██  ██  ██        ██    ██  ██      ██      ██████  █████    ████
  ▓▓ ▓▓   ▓▓  ▓▓  ▓▓        ▓▓    ▓▓  ▓▓      ▓▓      ▓▓  ▓▓  ▓▓  ▓▓      ▓▓
  ▒▒  ▒▒   ▒▒▒▒   ▒▒▒▒▒▒    ▒▒     ▒▒▒▒       ▒▒▒▒▒▒  ▒▒  ▒▒  ▒▒▒▒▒   ▒▒▒▒▒

        LIFE SUPPORT FOR THE ODYSSEY ENGINE  ·  PROTECTION: NONE
```

**Open-source tools for _Star Wars: Knights of the Old Republic_ I & II.** We reverse-engineer, patch and extend the Odyssey engine, and we publish everything we learn.

[Website](https://koltolabs.bocloud.workers.dev) · [Roadmap](https://koltolabs.bocloud.workers.dev/roadmap/) · [FAQ](https://koltolabs.bocloud.workers.dev/faq/) · [Contribute](https://github.com/kolto-labs/.github/blob/main/CONTRIBUTING.md) · Discord: invite coming soon

## Releases

| Project                                                         | What it does                                                                           | Status                                                                                                                                                                                                                 | License          |
| --------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| [**kq**](https://github.com/kolto-labs/kq)                       | Query a KotOR install like it was plain text. `rg` + `jq` for game data.               | ![released](https://img.shields.io/badge/status-released-7dff9a?style=flat-square&labelColor=0b1016) ![version](https://img.shields.io/github/v/release/kolto-labs/kq?style=flat-square&labelColor=0b1016&color=19e3c1) | MIT              |
| [**kotor-formats**](https://github.com/kolto-labs/kotor-formats) | Shared Rust readers/writers: GFF, 2DA, TLK, SSF, ERF/RIM, NCS. Byte-exact round trips. | ![released](https://img.shields.io/badge/status-released-7dff9a?style=flat-square&labelColor=0b1016) ![early](https://img.shields.io/badge/API-early-ffb000?style=flat-square&labelColor=0b1016)                       | MIT              |
| [**mod-builds**](https://github.com/kolto-labs/mod-builds)       | Release tooling for the KOTOR Community Portal mod builds.                             | ![released](https://img.shields.io/badge/status-released-7dff9a?style=flat-square&labelColor=0b1016)                                                                                                                   | upstream         |

## In the tank

| Project        | What it will do                                                                                                                       | Status                                                                                                             |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Hyperstim**  | Script extender. On the order of **10,000** new engine events and script commands for NWScript, hooked into the original executables. | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Adrenal**    | Lua scripting injected into the games. Subscribe to Hyperstim events, call engine commands, hot-reload.                               | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Kolto Tank** | Test harness. Boots the real game under instrumentation and asserts on engine state, so mods can be tested in CI.                     | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Hrakert**    | Matching decompilation of `swkotor.exe` and `swkotor2.exe`. No public one exists yet, as far as we know.                              | ![planned](https://img.shields.io/badge/status-planned-7f93a0?style=flat-square&labelColor=0b1016)                 |
| **Ahto**       | Docs hub: formats, engine behaviour, command references.                                                                              | ![planned](https://img.shields.io/badge/status-planned-7f93a0?style=flat-square&labelColor=0b1016)                 |

No release dates. Statuses mean what they say.

## Quick start

```sh
# kq is NOT the crate called "kq" on crates.io; install from our repo
cargo install --git https://github.com/kolto-labs/kq --locked

kq -i ~/kotor which appearance.2da
```

Installers for macOS, Linux and Windows are attached to every [kq release](https://github.com/kolto-labs/kq/releases).

## How we work

- One canonical repo per project. Decisions in public issues and RFCs.
- MIT where we can, GPL where a project chooses copyleft. Released code stays open.
- Every project credits its prior art: TSLPatcher, KotOR Tool, DeNCS, xoreos and the rest. See [credits](https://koltolabs.bocloud.workers.dev/credits/).
- [Contributing](https://github.com/kolto-labs/.github/blob/main/CONTRIBUTING.md) · [Code of Conduct](https://koltolabs.bocloud.workers.dev/#code-of-conduct) · [Reverse-engineering policy](https://koltolabs.bocloud.workers.dev/#re-policy) · [Security](https://github.com/kolto-labs/.github/blob/main/SECURITY.md)

**We are looking for** reverse engineers, Rust developers, NWScript and Lua modders, test authors and technical writers. No invitation needed.

---

<sub>Kolto Labs is an independent, non-commercial community project. It is not affiliated with, endorsed by, or sponsored by Lucasfilm Ltd., Disney, BioWare, Electronic Arts, Obsidian Entertainment, Aspyr Media or Saber Interactive. Star Wars, Knights of the Old Republic and related marks are trademarks of their respective owners. Our repositories contain no game assets or copyrighted game code. You need a legally obtained copy of the games to use our tools. We do not condone piracy.</sub>
