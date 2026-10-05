# Security Policy

Kolto Labs tools read files written by strangers (mods, saves, archives) and, in some projects, run code inside a game process. We take bugs in those paths seriously.

## Reporting a vulnerability

**Don't put the details in a public issue.**

GitHub's private vulnerability reporting isn't switched on for our repositories yet, and there's no security mailbox. Until one of those exists, open an issue on the affected repository titled `Security: need a private channel` and stop there: no description, no proof of concept. A maintainer will reply in that issue with a private way to send the rest.

When you send it, include the affected version, what goes wrong, and steps to reproduce. A proof-of-concept file helps, but it has to be synthetic. Never attach game assets.

Once private reporting is on, the **Report a vulnerability** button under a repository's **Security** tab replaces the issue step, and this file will say so.

## What happens next

- We aim to acknowledge reports within **7 days**.
- We'll confirm the issue, agree on a severity with you, and keep you updated while we fix it.
- We coordinate disclosure with you. Our default is to publish an advisory once a fixed release is out, and no later than 90 days after the report unless we agree otherwise.
- We credit reporters in the advisory, by name or handle, unless you'd rather stay anonymous.

This is a volunteer project; there is no bug bounty.

## Supported versions

Security fixes go into the **latest release** of each project on the Medpac (stable) channel. Advanced Medpac (beta) and Life Support (nightly) builds get fixes as part of normal development. Older releases aren't patched; upgrade to the latest.

## In scope

- Memory-safety or logic bugs triggered by crafted files: GFF, 2DA, TLK, ERF/RIM, KEY/BIF, NCS, MDL and the other formats we parse. A panic or crash on malformed input is a bug; code execution or an out-of-bounds write is a vulnerability.
- Path traversal or unexpected file writes from archive or resource names.
- Our install scripts and release artefacts: anything that could make an installer fetch or run something other than our signed-off release.
- Runtime projects (Hyperstim, Adrenal, Kolto Tank, once released): ways for a mod or script to escape its intended capabilities, such as unexpected file-system or network access from an API that shouldn't allow it.
- Leaked secrets in our repositories or CI.

## Out of scope

- Bugs in the games themselves, unless our tools make them exploitable.
- Mods that are malicious by design. Adrenal and Hyperstim run code you choose to install; treat mods like any other software you download.
- Antivirus heuristics flagging our runtime hooks. That's expected for any in-process hook; report it as a normal issue if it's a new false positive.
- Issues in third-party dependencies with no demonstrated impact on our tools. Report those upstream, and tell us if we need to update.
