# DuckysMusic — Command reference

All commands are Discord slash commands; type `/` in any text channel
where the bot is present to discover them with native autocomplete.
Commands marked **DJ** require the configured DJ role; configure it
with `/djrole`. If no DJ role is set, anyone can use them.

## Playback

| Command | What it does | Parameters |
|---|---|---|
| `/play` | Play a song or add it to the queue | `query`: song name or URL |
| `/pause` | Pause the current track | — |
| `/resume` | Resume a paused track | — |
| `/stop` | Stop playback and clear the queue | — |
| `/skip` | Skip to the next track | — |
| `/skipto` | Jump to a specific queue position | `position`: 1-based index |
| `/seek` | Seek within the current track | `time`: e.g. `1:30` or `90` (seconds) |
| `/replay` | Restart the current track from the beginning | — |

## Queue

| Command | What it does | Parameters |
|---|---|---|
| `/queue` | Paginated queue view | — |
| `/nowplaying` | Show the current song with progress | — |
| `/history` | Recently played songs | — |
| `/volume` | Set the playback volume | `level`: 0–150 |
| `/loop` | Set the loop mode | `mode`: `off` / `one` / `all` |
| `/shuffle` | Shuffle the queue | — |
| `/remove` | Remove a song from the queue | `position`: 1-based |
| `/move` | Move a song within the queue | `current`, `target` positions |
| `/clearqueue` | Clear the queue (keep current song) | — |

## Voice

| Command | What it does |
|---|---|
| `/join` | Join your voice channel |
| `/leave` | Leave the voice channel |

## Search

| Command | What it does | Parameters |
|---|---|---|
| `/search` | Interactive search across supported sources | `query`: search terms |

## Utility

| Command | What it does |
|---|---|
| `/help` | Interactive help by category |
| `/ping` | Show bot and Discord API latency |
| `/uptime` | Uptime, basic stats, node health |
| `/sources` | List supported music platforms and audio quality |

## Settings (Manage Server required)

| Command | What it does | Parameters |
|---|---|---|
| `/language` | Change or view the bot's language for this server | `code`: ISO language code (e.g. `en`, `es`) — see [the language list](#language-support) |
| `/djrole` | Set, view, or clear the DJ role | `role`: optional |

## Language support

DuckysMusic ships **30 user-facing languages**. The bot picks an initial
language from your Discord client locale and you can override it with
`/language` per server. Supported codes:

`ar` Arabic · `bg` Bulgarian · `cs` Czech · `da` Danish · `de` German ·
`el` Greek · `en` English · `es` Spanish · `fi` Finnish · `fil` Filipino ·
`fr` French · `hi` Hindi · `hu` Hungarian · `id` Indonesian · `it` Italian ·
`ja` Japanese · `ko` Korean · `nl` Dutch · `no` Norwegian · `pl` Polish ·
`pt-BR` Brazilian Portuguese · `ro` Romanian · `ru` Russian · `sv` Swedish ·
`th` Thai · `tr` Turkish · `uk` Ukrainian · `vi` Vietnamese ·
`zh-CN` Chinese (Simplified) · `zh-TW` Chinese (Traditional)

If your language is missing or a translation is wrong, file a feature
request — translations are crowd-improved between minor releases.

## Cooldowns and rate limits

Commands have per-user, per-guild cooldowns to keep the audio thread
fair across servers. You will not normally hit them in casual use.
Lavalink-side load shedding may delay long playlists by a few seconds
during peak hours.

## Reporting incorrect documentation

If a command behaves differently from what is described here, open a
[bug report](https://github.com/aiskaron/duckysmusic/issues/new?template=bug.yml).
Internal command implementation details will not be discussed; we will
fix either the docs or the bot, whichever is wrong.
