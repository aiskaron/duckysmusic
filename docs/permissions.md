# DuckysMusic — Required Discord permissions

DuckysMusic requests only what it needs to play music. The full set is
listed below so you can audit it before you add the bot to your guild.

## OAuth2 scopes

- `bot`
- `applications.commands`

That is the complete scope list. The bot does not request `guilds.join`,
`guilds.members.read`, or any other scope.

## Bot permissions on the guild

| Permission | Why it is needed |
|---|---|
| View Channels | See text channels where users invoke commands. |
| Send Messages | Reply to slash commands and post the now-playing card. |
| Embed Links | Render queue and now-playing embeds. |
| Read Message History | Resolve message-link references when seeking. |
| Use External Emoji | Render the playback control glyphs. |
| Add Reactions | Drive the now-playing reaction controls when enabled. |
| Connect | Join a user's voice channel. |
| Speak | Stream audio in the voice channel. |
| Use Voice Activity | Connect without a push-to-talk requirement. |
| Move Members | Move itself between voice channels when a user calls `/join` from a different room. |

The bot does NOT request:

- Manage Channels, Manage Roles, Manage Guild
- Kick / Ban / Moderate Members
- View Audit Log
- Mention Everyone
- Administrator
- Any Stage-channel privileged permission

## Per-channel permissions

If you want to restrict the bot to a specific text channel, override
its permissions on the other text channels and remove **Send Messages**
and **Use Application Commands** there.

## Voice channel permissions

The bot must have **Connect** and **Speak** on the voice channel a
user wants to listen in. If you have a music-only voice channel, set
**Connect** to allow only the bot and the listener role.

## Recovering from misconfiguration

If the bot suddenly cannot speak, post messages, or join a channel,
the cause is almost always a permission override that was added after
the bot joined. Use `/uptime` to confirm the bot is online; the
response will tell you the missing permission set.
