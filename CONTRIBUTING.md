# Contributing to Kolto Labs

Thanks for being here. Kolto Labs is built by volunteers. This file applies to every repository in the [kolto-labs](https://github.com/kolto-labs) organisation; a repository may add its own `CONTRIBUTING.md` with build details, and where the two differ, the repository's file wins.

Before anything else, read the [reverse-engineering policy](https://koltolabs.bocloud.workers.dev/#re-policy). It's short, and it's the one set of rules we can't bend.

## Ways to help

- **Report a bug.** Include the tool and version, your OS, which game (KotOR or TSL) and which build (disc, Steam, GOG, other), the exact command, and what you expected. A failing command beats a paragraph.
- **Fix a bug or add a feature.** Look for `good first issue` and `help wanted` labels.
- **Write documentation.** If you had to figure something out, the next person will too.
- **Test on your build.** Differences between game releases matter.

## Workflow

1. **Find or open an issue.** Comment that you're working on it so nobody duplicates the effort.
2. **Discuss big changes in an issue first.** Anything that changes a file format's handling, a public API, a command-line interface, a script command signature or a policy starts as an issue with the problem, the proposal and the alternatives.
3. **Fork and branch** from the default branch. Keep one logical change per pull request.
4. **Write tests.** Bug fixes come with a test that failed before the fix. Format code comes with round-trip tests (see below).
5. **Open a pull request.** Say what changed and why, link the issue, and make sure CI is green. Review happens in public, and at least one maintainer approval is required to merge.

## Commits

We use [Conventional Commits](https://www.conventionalcommits.org/) (`fix:`, `feat:`, `docs:`, `refactor:`, `test:`, `chore:`), because release automation in our repositories reads them to write changelogs and pick version numbers. Mark breaking changes with `!` or a `BREAKING CHANGE:` footer.

```
fix(gff): preserve padding after the last field struct
feat(kq)!: rename --shadow to --overshadowed
```

## Code standards

**Rust projects**

- `cargo fmt` and `cargo clippy --all-targets -- -D warnings` must pass.
- No `unsafe` without a comment explaining why it's sound.
- Parsers never panic on bad input. Malformed mod files are normal; return an error that says where and why.
- Respect each repository's minimum supported Rust version (stated in its README).

**Formats**

- **Round trips are exact.** Reading a file and writing it back unchanged must produce identical bytes. If your change can't guarantee that, discuss it in an issue first.
- **Strict by default.** Leniency is opt-in and must never change what a strict reader accepts.
- **Text is bytes.** Game strings go through the lossless Latin-1 mapping. Display-only remapping never reaches a write path.

## Tests and game data

We never commit game files. That includes BIFs, KEYs, TLKs, modules, scripts extracted from the game, textures, models and save files.

- **Unit and round-trip tests** use synthetic fixtures: small files built by the test itself or written by hand.
- **Integration tests** that need real game data read it from a local install whose path you supply (each repository documents the variable), and skip cleanly when it isn't set.
- Test output and snapshots must not embed game content either. Assert on structure, counts and hashes, not on copied strings from the game.

## Credit

If your change leans on someone else's work (a format note, an algorithm, how a tool behaves), name it in the pull request and we'll add it to the credits.

## Licensing

By contributing, you agree that your contribution is licensed under the license of the repository you contribute to (check its `LICENSE` file). Only submit work you have the right to submit.

## AI-assisted contributions

You're responsible for every line you submit, however it was written, and you must be able to explain it in review. Say in the pull request if substantial parts were machine-generated. Our reverse-engineering rules apply in full, and generated code is no exception.

## Conduct

Everyone in our spaces follows the [Code of Conduct](https://koltolabs.bocloud.workers.dev/#code-of-conduct). Be kind, assume good faith, and remember that every expert on this engine was once a confused newcomer on a forum.

## Questions

Open an issue on the repository it's about. kq and mod-builds also have Discussions switched on. Questions are welcome; there's no such thing as a stupid question about an engine with no official documentation.
