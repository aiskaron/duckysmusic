# Security Policy

## Reporting a vulnerability

If you have found a security issue in the hosted DuckysMusic bot — for
example a way to bypass the DJ-mode permission check, exhaust a guild's
queue limit, leak another user's data, or cause the bot to disconnect a
voice channel without authorization — please report it privately.

**Email:** security@aiskaron.com

Include:

- A short description of the issue.
- Steps to reproduce against the hosted bot, including the guild ID
  and channel context if relevant.
- The impact you observed.
- Your Discord handle (so we can credit you in the changelog if you
  wish).

We aim to acknowledge reports within 72 hours and to ship a fix or a
mitigation within 14 days for critical issues.

## What is in scope

- Behaviour of the hosted DuckysMusic bot in any Discord server it is a
  member of.
- The public `/api/health` endpoint of the bot.
- Trademark misuse of the DuckysMusic name or icon by other GitHub
  repositories.

## What is out of scope

- Source code review or audits: the bot is closed source, and this
  repository deliberately does not contain it.
- Reverse-engineered exploits derived from binary or network
  observation that do not affect the hosted bot in production. We will
  not negotiate bug bounties for theoretical issues against
  reconstructed implementations.
- Issues in the underlying technology stack (Lavalink, discord.py,
  Wavelink). Report those upstream.
- Vulnerabilities in third-party Discord servers that integrate the bot
  but expose their own services.

## Coordinated disclosure

We follow a 90-day coordinated disclosure window for non-trivial
issues. We will publish a CHANGELOG entry once a fix has shipped and
the affected guilds have been migrated.

Thank you for keeping the people who use DuckysMusic safe.
