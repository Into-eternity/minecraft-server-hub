# CurseForge API Application Draft

Replace all placeholders before submitting.

---

## Project name

```text
Minecraft Server Hub
```

## Your nickname

```text
YOUR_NICKNAME
```

## Your real name

```text
YOUR_REAL_NAME
```

## Email

```text
YOUR_EMAIL
```

## Your full Discord username

```text
YOUR_DISCORD_USERNAME
```

## Describe the project goal and scope

```text
Minecraft Server Hub is a self-hosted Minecraft server management application designed to simplify the deployment, operation, monitoring, backup, networking, recovery, and administration of Minecraft Java Edition servers.

The project supports multi-server lifecycle management, realtime console access, server-pack deployment, automatic port selection, networking information, backups, watchdog recovery, mod and modpack detection, mod-specific command shortcuts, configuration management, and MCSManager integration.

CurseForge API access will be used specifically to resolve CurseForge project and file metadata referenced by user-provided CurseForge manifests and to download files that the respective project authors and CurseForge permit to be distributed through third-party applications.

The application does not re-host CurseForge files, does not operate a public file mirror, does not attempt to bypass project distribution settings, and does not redistribute the CurseForge API key.

The initial use case is private and self-hosted Minecraft server administration, with a focus on reducing repetitive manual work when deploying legitimate CurseForge-based server packs.
```

## Why are you building this project?

```text
I am building Minecraft Server Hub because deploying and maintaining modded Minecraft servers currently requires many repetitive manual steps.

A typical CurseForge-based server setup may require identifying the correct Minecraft version, mod loader, Java version, dependencies, server files, ports, memory settings, EULA state, launch scripts, networking information, and individual mod configuration.

Minecraft Server Hub is intended to consolidate these tasks into one self-hosted management interface. The goal is to make legitimate Minecraft server administration safer and easier while respecting CurseForge project authors and their distribution preferences.

When a CurseForge manifest is imported, the application will use the official CurseForge API to resolve its referenced projects and files. Only files permitted for third-party distribution will be automatically downloaded. Files are used to construct the user's own Minecraft server installation and are not re-hosted or exposed as a separate public download service.

The project also provides functionality unrelated to CurseForge, including server monitoring, realtime console management, backups, crash recovery, player management, network endpoint generation, mod-specific command shortcuts, configuration management, automatic port allocation, and server lifecycle automation.

The CurseForge API integration is therefore one component of a broader Minecraft server management application rather than a replacement for CurseForge itself.
```

## Supported games

```text
Minecraft
```

## Website URL

For a repository named `minecraft-server-hub`:

```text
https://into-eternity.github.io/minecraft-server-hub/
```

## Git URL

```text
https://github.com/Into-eternity/minecraft-server-hub
```

## I understand that file distribution through the API is subjected to the mod author's approval

Select:

```text
Yes / checked
```

## Are you looking to monetize the project?

If your current project is private/non-commercial:

```text
No
```

## If you have a business model please describe it

```text
The project currently has no business model. It is being developed as a private, self-hosted Minecraft server management tool. There are currently no advertisements, subscriptions, paid downloads, donations, or other monetization methods.
```

## If you're planning to distribute mods, how would you contribute to the mod authors?

```text
Minecraft Server Hub will not re-host CurseForge files or operate an independent public mod distribution service.

When CurseForge-hosted files are required to materialize a user-provided server pack, the application will obtain project and file information through the official CurseForge API and will respect the distribution permission returned by CurseForge for each project.

If a project author has disabled third-party distribution, Minecraft Server Hub will not attempt to bypass that restriction or retrieve the file through an unofficial mirror.

The application is intended to retain relevant CurseForge project attribution and can direct users back to the corresponding CurseForge project when manual acquisition is required.

My intention is to respect the choices of mod authors and the CurseForge ecosystem rather than replacing or circumventing it.
```

## I understand that above certain volumes I might be required to reduce API calls, or alternatively, pay associated bandwidth costs

Select:

```text
Yes / checked
```

## I have read and agree to the API's TOS

Read the current terms yourself, then select:

```text
Yes / checked
```

## Additional notes

```text
Minecraft Server Hub is designed as a self-hosted control plane. The CurseForge API key remains on the server running the application and is not intended to be exposed to Minecraft players, browser clients, public repositories, or third parties.

API requests are made only when required for explicit user actions such as analyzing or deploying a CurseForge manifest-based server pack. The application is not intended to crawl or mirror the CurseForge catalog.

I am willing to adjust the CurseForge integration if required to comply with API usage, bandwidth, caching, attribution, or distribution requirements.
```
