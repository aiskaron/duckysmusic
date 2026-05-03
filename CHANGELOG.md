# Changelog (public-facing)

This page summarises what has changed for end users. Internal
refactors, dependency bumps, and developer-only fixes are not listed
here.

The hosted bot rolls forward continuously; the version on a given day
is the number printed by `/uptime`.

## 5.3.x — April 2026

- Improved type discipline across the bot (no user-visible change,
  but fewer rare crashes under contention).
- More robust queue persistence across container restarts: the queue
  now survives a Docker restart of the bot and reattaches to the
  voice channel within a few seconds.
- 24/7 reliability hardening: container-level autoheal restarts the
  bot or Lavalink within 30 seconds of an unhealthy state.

## 5.2.x — April 2026

- Embedded admin web panel for AIskaron operators (not exposed to
  users).
- GDPR-aware in-channel notice when the bot joins a voice channel,
  so members understand what is and is not recorded (nothing is).
- DuckysMic addon merged into the main release.

## 5.1.x — earlier 2026

- Slash-only command surface; legacy `!` prefix retired.
- Localisation expanded from 2 to 30 languages, see
  [the language list](docs/commands.md#language-support).
- DJ role configurable per guild via `/djrole`.
- New playback commands: `/skipto`, `/replay`, `/seek` with
  time-string support (e.g. `/seek 1:30`).
- New utility commands: `/sources` to list supported platforms and
  audio quality settings; `/uptime` to show node health.

## Breaking changes

None for end users in this minor line. If a breaking change ships, it
will be flagged here at least 14 days before rollout.
