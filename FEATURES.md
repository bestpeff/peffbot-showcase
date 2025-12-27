# Peffbot Features

Everything the bot can do, organized by category.

---

## AI Assistant

### !peffai
Ask the AI questions about the stream. Works for everyone but mods get extra diagnostic powers.

**Regular viewer examples:**
```
Viewer: !peffai when does the stream start?
Bot: Stream usually starts Mon/Wed/Fri at 7pm EST!

Viewer: !peffai what game is this?
Bot: Rocket League - been grinding ranked for about 2 hours now.
```

**Mod diagnostic example:**
```
Mod: !peffai why is !weather broken?
Bot: Weather command failing due to API timeout. Wait 5 mins and try again.
```

The AI has context awareness, natural language understanding, and bot troubleshooting for mods. Rate-limited to prevent spam.

---

## Stream Info

**!followers** - Current follower count
**!viewers** - Live viewer count
**!uptime** - How long the stream has been live
**!subs** - Subscriber count (if enabled)
**!status** - Stream status, game, title, and viewer count
**!created [username]** - When a Kick account was created
**!following [username]** - Check if someone follows the channel

---

## Game Stats

### Fortnite
```
!fortnite <username>
!setepic <your_username>
!stats (uses your linked profile)
```
Shows win rate, K/D ratio, season stats, and account level.

### Apex Legends
```
!apex <username>
!setorigin <your_username>
!stats
```
Shows current rank, kills, wins, season performance, and platform.

### Rocket League
```
!rocketleague <username>
!rl <username>
!setsteam <your_username>
!stats
```
Shows rank by playlist, MMR rating, win streaks, and season rewards level.

### Profile Management
```
!myprofiles - See your linked profiles
!setepic <name> - Link Epic Games (Fortnite)
!setorigin <name> - Link Origin (Apex)
!setsteam <name> - Link Steam (Rocket League)
```

---

## PC Specs

**For viewers:**
```
!pc / !pcspecs / !build
```
Shows the broadcaster's PC build.

**For users:**
```
!setmypc - Save your own specs
!pcsetup - View your saved specs
!clearmypc - Delete your specs
```

Example setup:
```
User: !setmypc
Bot: DM me your specs in this format:
CPU: AMD Ryzen 9 5950X
GPU: RTX 3090
RAM: 32GB DDR4
```

**For mods/broadcaster:**
```
!pctemps - Real-time CPU/GPU temperatures
!setpcbuild - Set broadcaster's default PC specs
```

---

## Social Links

**Supported platforms:**
Instagram, Twitter (X), TikTok, Snapchat, YouTube, Discord, Twitch, Facebook, Reddit, GitHub, LinkedIn, Patreon, OnlyFans, Throne, StreamElements, PayPal, Cash App, Venmo

**Viewer commands:**
```
!socials - Show all links
!instagram, !twitter, !tiktok, !discord, etc.
```

**Mod commands:**
```
!setinstagram <link>
!settwitter <link>
!settiktok <link>
(etc. for any platform)

!socialstatus - Check which socials are configured
```

---

## Mod Tools

### !errors
Shows recent command failures so mods can troubleshoot without bugging the broadcaster.

Example:
```
Mod: !errors
Bot: ⚠️ Recent errors: !weather (APIError), !stats (TimeoutError) |
     Total: 2 | Use !peffai to diagnose
```

### !peffai (Mod Version)
Mods can ask the AI to diagnose bot issues and get step-by-step fixes.

Example:
```
Mod: !peffai why is !stats broken?
Bot: Stats command failing because user hasn't linked their profile yet.
     Tell them to use !setepic <username> for Fortnite.
```

---

## Broadcaster Commands

### Stream Management
```
!title [new title] - Update stream title
!setfollowergoal <number> - Set follower goal
!setsubgoal <number> - Set subscriber goal
!settimezone <timezone> - Set timezone (auto-detected via OAuth)
```

### Authentication
```
!auth - Connect your Kick.com account (enables title updates)
!deauth - Disconnect account
```

### Bot Control
```
!rejoin - Reconnect bot to channel
!leave - Make bot leave channel
!setmodrejoin on/off - Let mods use !rejoin
!setmodleave on/off - Let mods use !leave
!channelsettings - View current settings
```

### Analytics
```
!topchatters [period]
Periods: hour, day, week, month, all
```

---

## Stream Interaction

**Mods/Broadcaster:**
```
!shoutout <user> - Give a shoutout
!hype - Hype up the chat
!starting <minutes> - Announce stream starting soon
```

**Broadcaster only:**
```
!brb <reason> - Announce BRB
!ending - Announce stream ending
```

**Everyone:**
```
!lurk - Announce you're lurking
```

---

## Custom Commands

**Broadcaster only:**
```
!!addcom <name> <response> - Create custom command
!!addtimer <name> <message> - Create auto-timer
!!delcom <name> - Delete command
!!listcoms - List all custom commands
!!coms - Show all admin commands
```

Example:
```
!!addcom discord Join our Discord: discord.gg/yourserver

User: !discord
Bot: Join our Discord: discord.gg/yourserver
```

---

## Spam Protection & Safety

**Advanced Spam Filtering:**
- Automatically detects and filters duplicate messages
- Catches link spam and repeated commands
- Smart detection for emote spam and short message floods
- Won't store obvious spam in the database (keeps things clean)
- Works silently - no annoying "stop spamming" messages in chat

**Smart Rate Limiting:**
- Different cooldowns per role (broadcaster > mods > VIPs > subs > regulars)
- Prevents command spam without punishing legitimate users
- Global rate limits protect against bot abuse
- Per-user hourly limits on expensive AI commands (keeps API costs down)
- Power users (subs/VIPs) get faster access without breaking things

**Role-Based Access:**
- Broadcaster: Full control over everything
- Mods: Diagnostic tools + moderation commands
- VIPs: Reduced cooldowns
- Subscribers: Reduced cooldowns
- Regular viewers: Standard cooldowns (fair but protected)

---

## Technical Features

**Storage:**
- Message history tracking
- User activity monitoring
- Error logging
- Custom command storage
- SQLite database with auto-cleanup

**OAuth Integration:**
- Secure Kick.com authentication
- Automatic timezone detection
- Token management and refresh

**Real-Time:**
- Pusher WebSocket connection
- Instant message processing
- Sub-second response times

---

## Coming Soon

- Analytics dashboard for tracking viewer activity and top chatters over time
- Train the bot to match your channel's personality and humor style
- More game integrations (Valorant, Call of Duty, Counter-Strike)
- Enhanced mod tools (better error diagnostics, command testing)
- Stream overlay widgets showing bot stats and top commands

---

## Tips

**Streamers:**
- Set up !auth first to enable title updates
- Configure social links early
- Train mods to use !errors for troubleshooting
- Use custom commands for FAQs

**Mods:**
- Check !errors when users report issues
- Use !peffai to diagnose problems
- Update social links as needed

**Viewers:**
- Link gaming profiles with !setepic/!setorigin/!setsteam
- Use !peffai to ask questions
- Save your PC specs with !setmypc

---

Feature requests? Hit up [@bestpeff](https://kick.com/bestpeff)
