# DuckysMusic — Frequently asked questions

## Can I get the source code?

No. DuckysMusic is a closed-source AIskaron Inc. product. This
repository is a public showcase, deliberately without source. See
the README for the rationale.

## Is there a free tier?

The hosted bot is free to add and use. AIskaron Inc. covers the
infrastructure costs. There is no paid tier today. If a paid tier is
introduced later, existing guilds keep current functionality at no
charge for at least 90 days, with notice in this CHANGELOG.

## How is my data handled?

The bot stores:

- **Per guild:** DJ role, language, default volume.
- **Per user:** opt-out flags for queue history and search-suggestion
  recording.
- **Transient runtime state:** the active queue, current track,
  voice-channel context. This is in memory and is cleared on bot
  restart unless you ran `/play` to add a track within the last
  session.

The bot does **not** store:

- Message contents from your channels.
- Audio data (it is streamed, not recorded).
- Voice activity metadata.
- IP addresses of users.

If you want a copy of the data the bot holds about you, or you want
it removed, email **privacy@aiskaron.com** with your Discord user ID
(right-click your name, Copy User ID). Requests are handled within 30
days, in line with GDPR Article 12.

## Why can't I find the bot in the public bot list?

The bot is invite-only at the moment. Use the invite link from the
[README](../README.md#invite-the-bot); there is no public top.gg
listing today.

## The bot is online but it does not respond in my server. Why?

Three common causes:

1. **Slash commands are not registered for your guild yet.** They
   propagate within an hour after the bot joins. Try `/help` after
   waiting; if it autocompletes, the registration is done.
2. **Channel permission overrides.** The bot needs Send Messages and
   Use Application Commands on the channel you are typing in. See
   [`permissions.md`](permissions.md).
3. **Voice channel permission overrides.** For playback commands,
   the bot needs Connect and Speak on the voice channel.

If none of these apply, open an issue with `/uptime` output and the
guild ID.

## How does it compare to (Other Bot)?

We don't publish comparison tables. Pick the bot whose feature list
and uptime guarantees match your needs. DuckysMusic is built for
AIskaron Inc. servers first; everything else is gravy.

## Can I commission a feature?

Email hello@aiskaron.com with the use case. Generally, features
that benefit all guilds are prioritised; bespoke features are not
accepted today.

## Will the bot be sold to another operator?

There is no plan to do so. If ownership changes, this repository will
publish the change at least 30 days in advance, with continuity terms.

## Can I run my own copy?

Not legally. The license is proprietary and the source is not
published. If you want to learn how to build a Discord music bot,
the public stack is well documented:
[discord.py](https://discordpy.readthedocs.io/),
[Lavalink](https://lavalink.dev/), and
[Wavelink](https://wavelink.dev/).

## How do I report a bug?

Open a GitHub issue on this repository describing what the bot did
versus what you expected. Include the guild ID, the channel ID, and
the approximate timestamp. We mostly look at server logs at our end;
your description plus those identifiers is usually enough.
