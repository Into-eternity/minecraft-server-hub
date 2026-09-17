# Security

## Do not commit secrets

Never commit any of the following to a public repository:

```text
config/hub.config.json
data/
backups/
runtime/
logs/
.update-staging/
.env
.env.*
*.key
*.pem
```

This includes:

- CurseForge API keys
- MCSManager API keys
- administrator credentials or authentication state
- private IP/network configuration when it should remain private
- Minecraft world data
- backups
- logs containing private information

## API keys

API keys must remain server-side.

Do not place API keys in:

- `index.html`
- browser JavaScript
- GitHub Pages
- README examples
- screenshots
- GitHub Issues
- Discord posts

If a key is accidentally exposed, revoke/rotate it immediately through the relevant provider.

## Public project profile

This repository is intended to contain documentation and a static project profile only.

Operational Minecraft Server Hub installations should keep their local configuration and data outside the public repository.
