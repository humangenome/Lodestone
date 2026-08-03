# Security Policy

## Reporting a vulnerability

If you have found a security issue in Lodestone — the app, the server, or the mods either one loads — please **do not** open a public GitHub issue.

Report it privately through GitHub's security advisory form:

- App and hub: https://github.com/HumanGenome/Lodestone/security/advisories/new
- Server: https://github.com/HumanGenome/LodestoneServer/security/advisories/new

**There is no security mailing address.** The advisory forms above are the only reporting channel; an email address claiming to be ours is not one.

Include:

- A description of the vulnerability
- Steps to reproduce
- Affected component (server / app / host mod / client mod)
- Lodestone version (the release tag, e.g. `v0.1.0`)
- Whether the issue is currently being exploited

Reports are acknowledged within 72 hours and triaged within 7 days.

## Scope

In scope:

- Remote code execution or unauthenticated takeover of a Lodestone server process
- A connected player being able to read or write arbitrary files on the host
- Authentication or admission bypass that lets an unauthorised client join, impersonate another player, or act as the host
- Privilege escalation through a mod Lodestone loads, or through the app's update path
- Tampering with the app's auto-update channel (unsigned or substituted payloads)
- Injection through the control channel between the app and the server

Out of scope:

- Vulnerabilities in the machine your server runs on — those belong to whoever operates it
- Vulnerabilities in retail Delverium itself — report those to the game's developer
- Vulnerabilities in third-party mods running alongside Lodestone
- Cheating and anti-cheat concerns; Lodestone does not provide anti-cheat
- Denial of service by simply sending a server more traffic than its link can carry
- Anything requiring administrative access to the server host, which already implies full control

## Supported versions

Only the latest released version receives security fixes. Lodestone is pre-1.0 and moves fast; there is no long-term support branch.
