```
  ██  ██   ████   ██      ██████   ████       ██       ████   █████    █████
  ██ ██   ██  ██  ██        ██    ██  ██      ██      ██  ██  ██  ██  ██
  ████    ██  ██  ██        ██    ██  ██      ██      ██████  █████    ████
  ▓▓ ▓▓   ▓▓  ▓▓  ▓▓        ▓▓    ▓▓  ▓▓      ▓▓      ▓▓  ▓▓  ▓▓  ▓▓      ▓▓
  ▒▒  ▒▒   ▒▒▒▒   ▒▒▒▒▒▒    ▒▒     ▒▒▒▒       ▒▒▒▒▒▒  ▒▒  ▒▒  ▒▒▒▒▒   ▒▒▒▒▒

        LIFE SUPPORT FOR THE ODYSSEY ENGINE  ·  PROTECTION: NONE
```

**Open-source tools for _Star Wars: Knights of the Old Republic_ I & II.** We reverse-engineer, patch and extend the Odyssey engine.

[Website](https://koltolabs.bocloud.workers.dev) · [Roadmap](https://koltolabs.bocloud.workers.dev/roadmap/) · [FAQ](https://koltolabs.bocloud.workers.dev/faq/) · [Contribute](https://github.com/kolto-labs/.github/blob/main/CONTRIBUTING.md)

## Releases

| Project                                                         | What it does                                                                           | Status                                                                                                                                                                                                                 | License          |
| --------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| [**kq**](https://github.com/kolto-labs/kq)                       | Query a KotOR install like it was plain text, the way `rg` and `jq` query code and JSON. | ![released](https://img.shields.io/badge/status-released-7dff9a?style=flat-square&labelColor=0b1016) ![version](https://img.shields.io/github/v/release/kolto-labs/kq?style=flat-square&labelColor=0b1016&color=19e3c1) | MIT              |
| [**kotor-formats**](https://github.com/kolto-labs/kotor-formats) | Shared Rust readers and writers for GFF, 2DA, TLK, SSF, ERF/RIM and NCS, with byte-exact round trips. | ![released](https://img.shields.io/badge/status-released-7dff9a?style=flat-square&labelColor=0b1016) ![early](https://img.shields.io/badge/API-early-ffb000?style=flat-square&labelColor=0b1016)                       | MIT              |

[mod-builds](https://github.com/kolto-labs/mod-builds) is our public fork of the KOTOR Community Portal's mod-build repository.

## In the tank

| Project        | What it is                                                                                                                            | Status                                                                                                             |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Hyperstim**  | A script extender for KotOR and TSL. | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Adrenal**    | Scripting for KotOR and TSL mods. | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Kolto Tank** | A test bench for mods. | ![in development](https://img.shields.io/badge/status-in%20development-ffb000?style=flat-square&labelColor=0b1016) |
| **Hrakert**    | A long-term project. | ![planned](https://img.shields.io/badge/status-planned-7f93a0?style=flat-square&labelColor=0b1016)                 |
| **Ahto**       | The Kolto Labs docs hub. | ![planned](https://img.shields.io/badge/status-planned-7f93a0?style=flat-square&labelColor=0b1016)                 |

## Quick start

```sh
# kq is NOT the crate called "kq" on crates.io; install from our repo
cargo install --git https://github.com/kolto-labs/kq --locked

kq -i ~/kotor which appearance.2da
```

Installers for macOS, Linux and Windows are attached to every [kq release](https://github.com/kolto-labs/kq/releases).

## How we work

- Each released project has one repository, and bugs and feature requests go in its public issues.
- Our released projects are MIT-licensed.
- We build on TSLPatcher, KotOR Tool, DeNCS, xoreos and more. See [credits](https://koltolabs.bocloud.workers.dev/credits/).
- [Contributing](https://github.com/kolto-labs/.github/blob/main/CONTRIBUTING.md) · [Code of Conduct](https://koltolabs.bocloud.workers.dev/#code-of-conduct) · [Reverse-engineering policy](https://koltolabs.bocloud.workers.dev/#re-policy) · [Security](https://github.com/kolto-labs/.github/blob/main/SECURITY.md)

**We are looking for** reverse engineers, Rust developers, NWScript modders, test authors and technical writers.

---

<sub>Kolto Labs is an independent, non-commercial community project. It is not affiliated with, endorsed by, or sponsored by Lucasfilm Ltd., Disney, BioWare, Electronic Arts, Obsidian Entertainment, Aspyr Media or Saber Interactive. Star Wars, Knights of the Old Republic and related marks are trademarks of their respective owners. Our repositories contain no game assets or copyrighted game code. You need a legally obtained copy of the games to use our tools. We do not condone piracy.</sub>
