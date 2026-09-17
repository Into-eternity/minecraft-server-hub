# Minecraft Server Hub

A self-hosted control plane for managing Minecraft Java Edition servers.

Minecraft Server Hub is designed to simplify deployment, operation, monitoring, networking, backups, recovery, and modded-server administration from one local web interface.

> This repository is the public project profile used to document the application and its CurseForge integration. It intentionally does **not** contain private server data, API keys, authentication state, world data, or other secrets.

## Project goals

Running modded Minecraft servers often involves many repetitive manual steps:

- selecting the correct Minecraft version and mod loader
- installing the correct Java runtime
- resolving modpack dependencies
- selecting a free Minecraft server port
- configuring memory and EULA state
- registering and controlling server instances
- exposing the correct `IP:PORT` to players
- managing backups and crash recovery
- working with mod-specific commands and configuration

Minecraft Server Hub brings these workflows together into one self-hosted administration interface.

## Core capabilities

- Multi-server lifecycle management
- MCSManager integration
- Server status and realtime console
- Automatic Minecraft port selection
- Radmin VPN / ZeroTier / LAN / public endpoint generation
- One-click copy of player connection addresses such as `26.x.x.x:25565`
- Server pack analysis and deployment
- CurseForge manifest-based server-pack materialization
- Minecraft / loader / Java / EULA detection
- Automatic MCSManager instance registration
- First-start health checks
- Backup and rollback workflows
- Watchdog restart and crash-loop protection
- Crash report and `latest.log` inspection
- Player administration
- Mod-aware command shortcuts
- User-defined command macros
- Mod configuration shortcuts
- JSON, `.properties`, and safe TOML scalar/table configuration support
- Responsive desktop, tablet, and mobile management UI

## CurseForge integration

Minecraft Server Hub can analyze user-supplied CurseForge manifest-based server packs.

The CurseForge API is used only to:

1. resolve project and file metadata referenced by a user-provided CurseForge manifest;
2. determine whether a referenced file is available for third-party distribution;
3. download files that CurseForge and the relevant project author permit third-party applications to distribute;
4. materialize those files into the user's own self-hosted Minecraft server installation.

Minecraft Server Hub:

- does **not** re-host CurseForge files;
- does **not** operate a public mod mirror;
- does **not** attempt to bypass project distribution settings;
- does **not** redistribute CurseForge API keys;
- does **not** expose the API key to Minecraft players;
- does **not** treat CurseForge as the only project feature — CurseForge integration is one component of a larger server-management application.

If a project author disables third-party distribution, the application is intended to respect that restriction and require an authorized/manual acquisition path instead of bypassing it.

See [CURSEFORGE_INTEGRATION.md](CURSEFORGE_INTEGRATION.md) for details.

## Privacy and security

The application is self-hosted.

Private operational data should stay on the server running Minecraft Server Hub and must not be committed to this public repository.

Examples of data that must remain private:

- CurseForge API keys
- MCSManager API keys
- administrator authentication state
- `config/hub.config.json`
- server registry data
- runtime state
- Minecraft worlds
- backups
- logs containing private information
- local network configuration

See [SECURITY.md](SECURITY.md) and [PRIVACY.md](PRIVACY.md).

## Website

This repository includes a static project page suitable for GitHub Pages.

After enabling GitHub Pages, the default project URL will be:

```text
https://into-eternity.github.io/minecraft-server-hub/
```

## Project status

Minecraft Server Hub is an independently developed self-hosted Minecraft server-management project.

The CurseForge integration is designed for legitimate server-pack deployment while respecting CurseForge API terms and mod-author distribution settings.

## CurseForge API application

A prepared application draft is included in:

[CURSEFORGE_APPLICATION.md](CURSEFORGE_APPLICATION.md)

Replace the placeholders for your real name, nickname, email, Discord username, and final URLs before submitting the form.
