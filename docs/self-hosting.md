# DuckysMusic — Self-hosting policy

DuckysMusic is **not** self-hostable. The source code is closed and
distribution is forbidden by the license.

This page exists because some operators have asked whether AIskaron
Inc. would license a private build for a single Discord server. That
is the only path, and it has not yet been opened. Watch the changelog
for an announcement.

## What you can do today

- Add the AIskaron-hosted DuckysMusic to your server via the
  [invite link](../README.md#invite-the-bot).
- Configure the bot per-guild with `/settings`.
- Reach out to hello@aiskaron.com if you have a high-volume,
  high-uptime use case that the public hosted bot does not cover.

## How the bot is built (for the curious)

The bot uses a public stack with no proprietary dependencies of its
own:

| Layer | Technology | Why we picked it |
|---|---|---|
| Discord client | [discord.py](https://discordpy.readthedocs.io/) | First-party Discord library, asyncio-native, mature. |
| Audio backend | [Lavalink v4](https://lavalink.dev/) | Out-of-process JVM service, isolates audio decoding from the bot, multi-language clients. |
| Lavalink client | [Wavelink](https://wavelink.dev/) | Idiomatic Python wrapper for Lavalink, production-tested. |
| Web admin | aiohttp | Lightweight, asyncio-native, integrates with the bot's event loop. |
| Storage | SQLite (per-guild settings) | One file, atomic backups, no separate database to operate. |
| Hosting | Docker Compose on Ubuntu LTS | Reproducible, restart-on-failure, autoheal sidecar. |

Anyone with a few weekends and the discord.py + Lavalink documentation
can replicate the playback core. The non-trivial parts (queue
persistence, DJ-mode voting, anti-abuse, GDPR endpoints, container
self-heal, observability) are not described here in any detail because
they are operationally sensitive.

## Migration path if AIskaron Inc. ever stops hosting

If, at some future date, AIskaron Inc. decides to discontinue the
hosted bot, the company will publish:

- A 60-day shutdown notice in this repository.
- An export tool so each guild can dump its `/settings` configuration.
- A list of recommended alternative hosted bots.

These commitments do not include releasing the source.
