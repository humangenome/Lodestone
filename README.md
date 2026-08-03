<p align="center">
  <img src="docs/img/lodestone-lockup.png" alt="Lodestone" width="480">
</p>

<p align="center">
  <a href="#getting-a-server"><img src="https://img.shields.io/badge/Platform-Windows_10%2F11%2FServer-blue.svg" alt="Platform"></a>
  <a href="https://store.steampowered.com/app/2710040/"><img src="https://img.shields.io/badge/Game-Delverium-darkgreen.svg" alt="Game"></a>
  <a href="https://github.com/HumanGenome/LodestoneServer"><img src="https://img.shields.io/badge/Server_Source-LodestoneServer-brightgreen.svg" alt="Server source"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License"></a>
</p>

# Lodestone — always-on Delverium servers

Delverium co-op is friends-only and lives on one player's machine. Whoever started the world has to be online for anyone else to play, and when they log off, the world goes with them.

A Lodestone server changes that. The world lives on a server that stays up around the clock, your friends join it whenever they want, and nobody has to wait for the host. [Delverium](https://store.steampowered.com/app/2710040/) itself is unmodified — you still buy and run it from Steam.

<!-- Screenshot of the Lodestone app goes here once the visual pass is signed off:
     <p align="center">
       <img src="docs/img/launcher.png" alt="The Lodestone app showing a Delverium server" width="860">
     </p>
     Keep it a real capture of the shipped build, matching the sibling hubs. -->

<p align="center">
  <em>Lodestone is in development for Delverium's Early Access launch on 22 September 2026.<br>
  There are no public downloads yet — releases will appear on this page.</em>
</p>

---

## Highlights

### The world never logs off
Your world runs on the server, not on somebody's gaming PC. Play at 3am on a Tuesday without rounding anyone up first.

### Join from the game's own server list
Open Delverium, look at the Online list, click your server. It sits alongside every other result and behaves the same way.

### Your character comes with you
Characters belong to you and travel between servers. The world belongs to the server and stays put.

### Room for the full group
Up to eight players, the same as Delverium's own limit — you are not trading players away for persistence.

### Nothing extra to buy
A Lodestone server needs no second copy of Delverium and no extra Steam account. One server, one world, however many friends you have.

### Light on hardware
The server runs without a graphics card and without a desktop, so it is happy on a spare box, a cheap VPS, or managed hosting.

---

## How it works

Three pieces, and you only ever touch the middle one.

| | |
|---|---|
| **The server** | Runs Delverium as a headless host. It owns the world, saves it continuously, and answers the standard Steam server query so monitoring tools and server lists can see it. |
| **The Lodestone app** | A small Windows app you run instead of launching Delverium yourself. Save a server address once, hit Connect, and it puts you in the world. |
| **Your Delverium copy** | Unchanged and bought from Steam as normal. Lodestone does not replace it or ship any part of it. |

Every player needs the Lodestone app to join a Lodestone server — stock Delverium cannot reach one on its own.

---

## Getting a server

### Managed hosting

The shortest path is [SurvivalServers.com Delverium hosting](https://www.survivalservers.com/services/game_servers/delverium/?utm_source=github&utm_medium=readme_install&utm_campaign=lodestone). Lodestone comes pre-installed, the ports are already open, and the control panel hands your players a ready-made connect link.

### Running your own

Server downloads and setup instructions live in [LodestoneServer](https://github.com/HumanGenome/LodestoneServer). You will need a Windows machine, the Delverium game files, and two open UDP ports.

### Players

Once the first release lands, joining is three steps: install the Lodestone app, paste the server address, click Connect. The app remembers your servers and your character between sessions.

---

## Ports

A Lodestone server uses two UDP ports, and the second one follows the first.

| Port | Used for |
|---|---|
| base (default `27016`) | Gameplay — this is the port players connect to |
| base + 1 (default `27017`) | Steam server query, for server lists and monitoring |

---

## Downloads and changelog

Releases are published here as they happen. Each release page lists what changed and which files to download.

- [Latest release](https://github.com/HumanGenome/Lodestone/releases/latest) — the Lodestone app for players
- [LodestoneServer releases](https://github.com/HumanGenome/LodestoneServer/releases/latest) — the server package for hosts
- [Full changelog](https://github.com/HumanGenome/LodestoneServer/blob/main/CHANGELOG.md) — every version in one place

Both sides share a version line, so a given version number means the same build on either.

---

## FAQ

### Do all my friends need this?
Yes. Everyone joining a Lodestone server runs the Lodestone app. Your Delverium install is untouched, and you can still play normal friends-only co-op whenever you want.

### Do I need to leave my PC on?
No — that is the point. Once the world is on a server, your machine has nothing to do with it.

### What happens to my character?
It stays yours. Characters move between servers with you; the world stays on the server it was created on.

### Can I move a world between servers?
Yes. World saves are ordinary files, so a host can copy one from one server to another.

### Is this an official Delverium feature?
No. Lodestone is a community project. Sagestone Games does not ship dedicated servers for Delverium, which is why this exists.

### Where do I report a problem?
[Open an issue](https://github.com/HumanGenome/Lodestone/issues). If you rent a managed server, contact your host for anything about billing or the control panel.

---

## Contributing

Bug reports and feature requests are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Security issues go through [private reporting](.github/SECURITY.md), never a public issue.

## Community note

Lodestone is an independent community project. It is not affiliated with, endorsed by, or supported by Sagestone Games. Delverium is their game; buy it from [Steam](https://store.steampowered.com/app/2710040/).

## License

MIT — see [LICENSE](LICENSE).
