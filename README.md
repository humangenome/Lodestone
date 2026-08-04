<p align="center">
  <img src="docs/img/lodestone-lockup.png" alt="Lodestone" width="460">
</p>

# Lodestone

[![Platform](https://img.shields.io/badge/Platform-Windows_10%2F11%2FServer-blue.svg)](#install)
[![Game](https://img.shields.io/badge/Game-Delverium-6abe30.svg)](https://store.steampowered.com/app/2710040/)
[![Players](https://img.shields.io/badge/Players-up_to_8-brightgreen.svg)](#-up-to-eight-players)
[![Server Source](https://img.shields.io/badge/Server_Source-LodestoneServer-444.svg)](https://github.com/HumanGenome/LodestoneServer)
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)](LICENSE)

Lodestone gives **Delverium** always-on dedicated servers: players join through the Lodestone app, hosts run the Lodestone server package next to Delverium's game files, and the world lives on the server with a live map, in-game chat, admin tools, and server query. No world tied to one person's PC, no waiting for the host to come online.

Every player installs Lodestone to join a Lodestone server, the host included: Delverium cannot reach a dedicated server on its own, so the app is how anyone gets in. It installs once per person and takes a minute. Your copy of Delverium is bought, launched, and updated through Steam exactly as normal; Lodestone replaces nothing and ships no part of the game.

<p align="center">
  <img src="docs/img/launcher.png" alt="The Lodestone app: saved servers, who is online right now, and a Connect button" width="860">
</p>

## Features

### 🌙 Your world never sleeps
The world lives on the server, not on anyone's PC. One of you mines at noon, another builds at midnight, and the same world is waiting for both. When the last player logs off, the server keeps running, keeps saving, and holds the door open.

<p align="center">
  <img src="docs/img/in-game.png" alt="Two players together in a Delverium world hosted on a Lodestone server" width="860">
</p>

### 🗺 Live world map
Your whole world in a browser, drawn with the game's own terrain art and redrawn as players mine, build, and explore. Live player markers show where everyone is right now, served straight from the running server.

<p align="center">
  <img src="docs/img/live-map.png" alt="The Lodestone live map rendering a Delverium world with the game's own terrain art" width="860">
</p>

### 💬 In-game chat
Delverium has no chat of its own, so Lodestone adds one. Press **T** in game to talk. Player messages, join and leave notices, and server announcements all land in one feed, rendered by the game's own UI in the game's own font.

<p align="center">
  <img src="docs/img/chat.png" alt="In-game chat on a Lodestone server: player messages and a server broadcast in the same feed" width="860">
</p>

### 🧭 Join by address
Save a server's address once. From then on the app shows the server's status and who is online at a glance, and joining is one click: **Connect** readies Delverium and takes you straight into the world.

### 🧑‍🤝‍🧑 Up to eight players
The full co-op limit Delverium supports, with nobody's PC doing the hosting. Characters are made in the game, the same as always, and they travel with you between servers; the world stays on the server.

### 🛠 Admin console
Roster, kick and ban, world save, restart, shutdown, and broadcasts into the in-game chat, over Source RCON or a signed HTTP API. A host, a scheduler, or a hosting panel can run the server without ever touching the machine.

### 📡 Server query
The server answers Source A2S query with live status and real player counts, so monitoring tools, Discord bots, and hosting panels can see it.

### 🚦 Refuses to run broken
If the server cannot come up healthy, it refuses to start and writes exactly what stopped it to its boot report, instead of limping up half-working with no way to tell.

### 🪶 Light on the machine
The server package installs in 328 MB and idles at about 6.6% of one CPU core, so it runs happily on modest hardware and leaves the rest of the box alone.

## Install

### Managed hosting
[Delverium hosting from SurvivalServers.com](https://www.survivalservers.com/services/game_servers/delverium/?utm_source=github&utm_medium=readme_install&utm_campaign=lodestone) comes with Lodestone installed and kept up to date, the ports open, and a connect link ready to hand to your players.

### Players
1. Download `LodestoneSetup-<version>.exe` from the [latest release](https://github.com/HumanGenome/Lodestone/releases/latest).
2. Run the installer. It is a one-time install per person.
3. Open Lodestone, add the server address your host gave you, and click **Connect**. The app readies Delverium and takes you in. Characters are made in the game, the same as always.

### Self-hosted servers
Downloads and setup live in [HumanGenome/LodestoneServer](https://github.com/HumanGenome/LodestoneServer). You will need a Windows machine, a copy of Delverium's game files on it (from your own Steam copy; the server package ships no part of the game), and a couple of open ports.

## Releases

This repo publishes the player side:

- `LodestoneSetup-<version>.exe`, the installer for players
- Release notes for each version

The server package for hosts lives on the [LodestoneServer release page](https://github.com/HumanGenome/LodestoneServer/releases/latest), and the public changelog for both sides is [LodestoneServer's CHANGELOG.md](https://github.com/HumanGenome/LodestoneServer/blob/main/CHANGELOG.md).

<p align="center">
  <em>Lodestone is in development for Delverium's Early Access launch on 22 September 2026.<br>
  There are no public downloads yet; releases will appear here.</em>
</p>

## Source

Lodestone is split into two repos:

- **Lodestone** (this repo): the player side, the desktop app players install, plus the public downloads and documentation.
- **[LodestoneServer](https://github.com/HumanGenome/LodestoneServer)**: the dedicated server package hosts run next to Delverium's game files.

Players only need this repo's releases; hosts run the server from LodestoneServer's.

## FAQ

### Do all my friends need the app?
Yes, and so do you. Delverium cannot reach a Lodestone server without it. It installs once per person, and normal Delverium co-op still works whenever you want it.

### Do I need to leave my PC on?
No. That is the entire point. Once the world is on a server, your machine has nothing to do with it.

### Does this change my copy of Delverium?
No. You buy, run, and update Delverium through Steam as normal, and your ordinary single-player and co-op games are untouched.

### Will my server show up inside Delverium?
Delverium has no server browser; its Online menu lists your Steam friends. On a PC with Lodestone installed, your saved servers appear in that menu too, so you can join from inside the game. Players without the app never see them.

### Can I move a world between servers?
Yes. World saves are ordinary files, so a host can copy one across. Characters are not part of the world file; they travel with the players who made them.

### Is this an official Delverium feature?
No. Lodestone is an independent community project. Sagestone Games does not ship dedicated servers for Delverium, which is why this exists.

### Where do I report a problem?
[Open an issue](https://github.com/HumanGenome/Lodestone/issues). If you rent a managed server, your host handles billing and control-panel questions.

## Contributing

Bug reports and feature requests are welcome; see [CONTRIBUTING.md](CONTRIBUTING.md). Security issues go through [private reporting](.github/SECURITY.md), never a public issue.

## Community Note

Lodestone is a community project and is not affiliated with, endorsed by, or supported by Sagestone Games. Delverium is their game: [buy it on Steam](https://store.steampowered.com/app/2710040/).

## License

MIT. See [LICENSE](LICENSE).

## Credits

- [BepInEx](https://github.com/BepInEx/BepInEx), the Unity modding framework the server side runs on
- [Avalonia](https://avaloniaui.net/), the .NET UI framework used by the Lodestone app
- [Pixel Operator](https://www.dafont.com/pixel-operator.font) (CC0), the typeface in Lodestone's brand art
