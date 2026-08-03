# Contributing to Lodestone

Short and to the point.

## Which repo do I file against?

| You are looking at | File it here |
|---|---|
| The Lodestone app — installing, connecting, the server list, updates | [HumanGenome/Lodestone](https://github.com/HumanGenome/Lodestone/issues) |
| A running server — startup, world saving, ports, server query | [HumanGenome/LodestoneServer](https://github.com/HumanGenome/LodestoneServer/issues) |
| Not sure | Here. It gets moved. |

## Reporting bugs

Open an issue using the **Bug report** template. Include:

- Lodestone version (the release tag, e.g. `v0.1.0`) and which download you used
- Your Delverium build (Steam build ID if you know it)
- Steps to reproduce
- The app log, and the server log if you host the server
- Whether anyone else can reproduce it on a clean server

If your issue is about managed hosting you bought — the control panel, billing, or support — contact your host directly. Lodestone's GitHub issues are for the open-source app, server, and mods themselves.

## Feature requests

Open an issue using the **Feature request** template. Describe what you are trying to do, not how you think it should be built.

## Security issues

Do not open a public issue. See [SECURITY.md](.github/SECURITY.md).

## Pull requests

This project does not accept code pull requests while it is pre-release. Once the first stable tag ships:

- Branch from `main`, named `feat/<short-slug>` or `fix/<short-slug>`
- One logical change per commit, short subject lines
- Match the existing code style
- Justify any new dependency in the pull request description
- Run the test suite before opening the pull request

Documentation and typo fixes are welcome at any time.

## Code of conduct

Be civil. Be technical. Do not post game-piracy or anti-cheat-evasion material in issues or pull requests.
