# CurseForge Integration

## Purpose

Minecraft Server Hub uses CurseForge API access as one part of a broader self-hosted Minecraft server-management application.

Its CurseForge integration is intended to make a user-provided CurseForge manifest usable as a Minecraft server installation without requiring the user to manually resolve every project and file reference.

## Intended workflow

```text
User selects a CurseForge manifest-based server pack
        ↓
Minecraft Server Hub validates the archive
        ↓
manifest.json is parsed
        ↓
Minecraft version and loader are identified
        ↓
Referenced CurseForge project/file IDs are resolved
        ↓
Distribution permission is respected
        ↓
Permitted files are downloaded
        ↓
Overrides are applied
        ↓
Server loader is installed
        ↓
Port / memory / EULA settings are applied
        ↓
Server instance is registered
        ↓
First startup and health check
```

## Distribution principles

Minecraft Server Hub is not intended to:

- mirror the CurseForge catalog;
- re-host CurseForge artifacts;
- circumvent disabled third-party distribution;
- expose or redistribute a CurseForge API key;
- provide a public download endpoint for CurseForge files.

When a referenced project is not available for third-party distribution, the application should stop automatic retrieval for that file and present a legitimate/manual acquisition path.

## API usage

API requests are tied to explicit user actions such as:

- analyzing a manifest;
- resolving referenced project/file metadata;
- deploying a server pack.

The project is not intended to continuously crawl or mirror CurseForge.

## Credentials

CurseForge API credentials are server-side secrets.

They must not be:

- embedded in client-side JavaScript;
- returned by public configuration APIs;
- committed to Git;
- included in screenshots;
- shared with Minecraft players;
- bundled in release archives.
