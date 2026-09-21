<p align="center">
  <img src="docs/img/lodestone-lockup.png" alt="Lodestone" width="460">
</p>

<p align="center">
  <a href="#install"><img src="https://img.shields.io/badge/Platform-Windows_10%2F11%2FServer-blue.svg" alt="Platform"></a>
  <a href="https://store.steampowered.com/app/2710040/"><img src="https://img.shields.io/badge/Game-Delverium-6abe30.svg" alt="Game"></a>
  <a href="#-eight-players-eight-seats"><img src="https://img.shields.io/badge/Players-up_to_8-brightgreen.svg" alt="Players"></a>
  <a href="https://github.com/HumanGenome/LodestoneServer"><img src="https://img.shields.io/badge/Server_Source-LodestoneServer-444.svg" alt="Server Source"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License"></a>
</p>

# Lodestone

Delverium has no dedicated server. Its online co-op is a session hosted from one player's copy of the game, and the world only exists while that player has the game open. Lodestone adds a Delverium dedicated server: [LodestoneServer](https://github.com/HumanGenome/LodestoneServer) runs the game headless on a Windows machine with a public IP and port, and the Lodestone app connects players to it by address.

Every player must install Lodestone to join a Lodestone server. Stock Delverium cannot connect to a Lodestone server directly.

<p align="center">
  <img src="docs/img/launcher.png" alt="The Lodestone app: saved servers with their status and player counts, the selected server's roster, and the Connect button" width="860">
</p>

## Features

### 🌙 Your world never sleeps
The world is created, saved and kept on the server. One of you mines at noon, another builds at midnight, and the same world is waiting for both. When the last player logs off, the server keeps running and keeps saving.

<p align="center">
  <img src="docs/img/in-game.png" alt="Two players together in a Delverium world hosted on a Lodestone server" width="860">
</p>

### 🗺️ Live world map
Every Lodestone server draws its world in a browser from the game's own terrain art, redrawn as players mine, build and explore. Every connected player is marked where they stand, the teleporters are marked, and the server keeps a timelapse of how the world changed.

<p align="center">
  <img src="docs/img/live-map.png" alt="The Lodestone live map: a Delverium world drawn with the game's own terrain art" width="860">
</p>

### 💬 In-game chat
Delverium has no chat, so Lodestone adds one. Press **T** in game to talk. Player messages, join and leave notices, server announcements and restart countdowns all land in one feed, drawn by the game's own UI in the game's own font. Admins get chat commands too: teleport a player, set the message of the day, warn everyone before a restart.

<p align="center">
  <img src="docs/img/chat.png" alt="In-game chat on a Lodestone server: player messages and a server broadcast in the same feed" width="860">
</p>

### 🧭 Join by address
Add the server's `ip:port` in the app and click Connect. The app puts the connection files next to your game, starts Delverium and joins the server. The app shows whether the server is up, who is online and your ping before you connect.

### 👥 Eight players, eight seats
Delverium's own co-op limit is eight, and the server takes no seat. Characters are made in the game as always and stay on your PC; you pick which one to bring.

### 🔒 Join password
Set one on the server and only players who enter it in the app get in.

### 🖥️ Console in the app
The Console tab talks to the server's admin port once the admin password is set: who is online, kick, ban, save, restart, and a broadcast into the in-game chat.

### 🛠️ Admin tools for hosts
Source RCON and a signed HTTP API on the server, a live roster file for panels and bots, a ban list that survives restarts, and a boot report that says in plain words why a server did not start. Details in [LodestoneServer](https://github.com/HumanGenome/LodestoneServer).

### 📡 Server query
The server answers Source A2S on the port above the gameplay port with its status and real player count, so monitoring tools and hosting panels can read it.

### 🧩 Mods tab
The Mods tab shows what the selected server runs and what, if anything, it asks of you.

### 🔄 Plain game afterwards
Starting Delverium from Steam after a Lodestone session runs the normal game. Your single-player and ordinary co-op games are untouched.

## Install

### Managed hosting
[SurvivalServers.com Delverium server hosting](https://www.survivalservers.com/services/game_servers/delverium/?utm_source=github&utm_medium=readme_install&utm_campaign=lodestone) comes with Lodestone installed and kept up to date, the ports open, and a control panel with the live map, the console and one-click restores.

### Players
1. Download `LodestoneSetup-latest.exe` from the [latest release](https://github.com/HumanGenome/Lodestone/releases/latest/download/LodestoneSetup-latest.exe).
2. Run it. One install per PC. The app updates itself from then on.
3. Open Lodestone, add the server address, pick a character, click Connect.

### Self-hosted servers
Requirements, ports, setup, the live map page, the admin API and the chat commands are in [LodestoneServer](https://github.com/HumanGenome/LodestoneServer). You need a Windows machine and a copy of Delverium's game files on it from your own Steam copy; the server package ships no part of the game.

## Releases

This repo publishes the player side: `LodestoneSetup-<version>.exe`, a `LodestoneSetup-latest.exe` alias, and the release notes. The server package is on the [LodestoneServer release page](https://github.com/HumanGenome/LodestoneServer/releases/latest), and the changelog for both sides is [LodestoneServer's CHANGELOG.md](https://github.com/HumanGenome/LodestoneServer/blob/main/CHANGELOG.md).

## Source

- **Lodestone** (this repo): the app players install, the downloads and the documentation.
- **[LodestoneServer](https://github.com/HumanGenome/LodestoneServer)**: the server package hosts run next to Delverium's game files.

## FAQ

### Does everyone need the app?
Yes. The game cannot reach a Lodestone server without it. It installs once per PC, and normal Delverium co-op still works whenever you want it.

### Does it change my game?
It adds `winhttp.dll` and a `BepInEx` folder next to `Delverium.exe`. Steam updates the game as normal. Delete those two to remove it.

### Where is my character saved?
On your PC, where Delverium keeps it. The server holds the world.

### Will my server show up inside Delverium?
Delverium's Online menu lists your Steam friends. On a PC with Lodestone installed, the server you last connected to appears in that menu as well.

### Can a world move between servers?
Yes. The world save is a file on the server; copy it to the other server.

### Is this official?
No. Lodestone is an independent project. Sagestone Games does not ship dedicated servers for Delverium.

### Something broke
[Open an issue](https://github.com/HumanGenome/Lodestone/issues). If you rent a server, your host handles billing and control panel questions.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Security issues go through [private reporting](.github/SECURITY.md), never a public issue.

## Community note

Lodestone is an independent community project. It is not affiliated with, endorsed by, or supported by Sagestone Games. Delverium is their game: [buy it on Steam](https://store.steampowered.com/app/2710040/).

## License

MIT, see [LICENSE](LICENSE).

## Credits

- [BepInEx](https://github.com/BepInEx/BepInEx), the Unity modding framework the server side runs on
- [Avalonia](https://avaloniaui.net/), the .NET UI framework used by the Lodestone app
- [Pixel Operator](https://www.dafont.com/pixel-operator.font) (CC0), the typeface in Lodestone's brand art
