# 🎯 Peffbot Features - Complete Guide

Complete breakdown of everything Peffbot can do for your stream.

---

## 🤖 AI-Powered Features

### !peffai - Conversational AI Assistant
**What it does:** Viewers can ask the AI questions about your stream.

**Examples:**
```
Viewer: !peffai when does the stream start?
Bot: Stream usually starts Mon/Wed/Fri at 7pm EST!

Viewer: !peffai what game is this?
Bot: Rocket League - been grinding ranked for about 2 hours now.
```

**For Mods:** Enhanced with bot diagnostics
```
Mod: !peffai why is !weather broken?
Bot: Weather command failing due to API timeout. Wait 5 mins and try again.
```

**Features:**
- Context-aware responses
- Natural language understanding
- Bot troubleshooting for mods
- Rate-limited to prevent spam

---

## 📊 Stream Info Commands

### !followers
Shows current follower count.

### !viewers
Shows current live viewer count.

### !uptime
Shows how long stream has been live.

### !subs
Shows subscriber count (if enabled).

### !status
Shows if stream is live, current game, title, and viewer count.

### !created [username]
Shows when a Kick account was created.

### !following [username]
Shows if someone is following the channel.

---

## 🎮 Game Stats Integration

### Fortnite Stats
```
!fortnite <username>
!setepic <your_username>
!stats (auto-detects your linked profile)
```

**Shows:**
- Win rate
- K/D ratio
- Season stats
- Account level

### Apex Legends Stats
```
!apex <username>
!setorigin <your_username>
!stats
```

**Shows:**
- Current rank
- Kills, wins
- Season performance
- Platform info

### Rocket League Stats
```
!rocketleague <username>
!rl <username>
!setsteam <your_username>
!stats
```

**Shows:**
- Rank by playlist
- MMR rating
- Win streaks
- Season rewards level

### Profile Management
```
!myprofiles - See your linked gaming profiles
!setepic <name> - Link Epic Games (Fortnite)
!setorigin <name> - Link Origin (Apex)
!setsteam <name> - Link Steam (Rocket League)
```

---

## 💻 PC Specs Commands

### For Viewers
```
!pc / !pcspecs / !build
```
Shows broadcaster's PC specs (if set).

### For Users
```
!setmypc - Save your own PC specs
!pcsetup - View your saved specs
!clearmypc - Delete your specs
```

**Example:**
```
User: !setmypc
Bot: DM me your specs in this format:
CPU: AMD Ryzen 9 5950X
GPU: RTX 3090
RAM: 32GB DDR4
```

### For Mods/Broadcaster
```
!pctemps - Show real-time CPU/GPU temperatures
!setpcbuild - Set broadcaster's default PC specs
```

---

## 📱 Social Links Management

### Available Platforms
Instagram, Twitter (X), TikTok, Snapchat, YouTube, Discord, Twitch, Facebook, Reddit, GitHub, LinkedIn, Patreon, OnlyFans, Throne, StreamElements, PayPal, Cash App, Venmo

### For Viewers
```
!socials - Show all social links
!instagram - Show Instagram
!twitter - Show Twitter
!tiktok - Show TikTok
!discord - Show Discord
(etc. for any platform)
```

### For Mods
```
!setinstagram <link> - Set Instagram link
!settwitter <link> - Set Twitter link
!settiktok <link> - Set TikTok link
(etc. for any platform)

!socialstatus - Check which socials are set up
```

---

## 🔧 Mod Diagnostic Tools

### !errors (Mods Only)
View recent command failures.

**Example:**
```
Mod: !errors
Bot: ⚠️ Recent errors: !weather (APIError), !stats (TimeoutError) |
     Total: 2 | Use !peffai to diagnose
```

### !peffai (Enhanced for Mods)
Mods get access to bot diagnostics.

**Example:**
```
Mod: !peffai why is !stats broken?
Bot: Stats command failing because user hasn't linked their profile yet.
     Tell them to use !setepic <username> for Fortnite.
```

---

## 👑 Broadcaster Commands

### Stream Management
```
!title [new title] - Update stream title
!setfollowergoal <number> - Set follower goal
!setsubgoal <number> - Set subscriber goal
!settimezone <timezone> - Set timezone (usually auto-detected)
```

### Authentication
```
!auth - Connect Kick.com account (enables stream title updates)
!deauth - Disconnect Kick.com account
```

### Bot Control
```
!rejoin - Reconnect bot to channel
!leave - Make bot leave channel
!setmodrejoin on/off - Allow mods to use !rejoin
!setmodleave on/off - Allow mods to use !leave
!channelsettings - View current settings
```

### Analytics
```
!topchatters [period] - Show most active chatters
  Periods: hour, day, week, month, all
```

---

## 🎬 Stream Interaction Commands

### For Mods/Broadcaster
```
!shoutout <user> - Give a shoutout
!hype - Hype up the chat
!starting <minutes> - Announce stream starting soon
```

### For Broadcaster
```
!brb <reason> - Announce BRB
!ending - Announce stream ending
```

### For Everyone
```
!lurk - Announce lurking
```

---

## ⚙️ Custom Commands

### Admin Commands (Broadcaster Only)
```
!!addcom <name> <response> - Create custom command
!!addtimer <name> <message> - Create auto-timer
!!delcom <name> - Delete command
!!listcoms - List all custom commands
!!coms - Show all admin commands
```

**Example:**
```
!!addcom discord Join our Discord: discord.gg/yourserver

User: !discord
Bot: Join our Discord: discord.gg/yourserver
```

---

## 🛡️ Built-In Safety Features

### Smart Rate Limiting
- **Tiered cooldowns** based on user role
- **Spam detection** with automatic muting
- **Global rate limits** prevent bot abuse
- **Per-user hourly limits** on AI commands

### Role-Based Access
- **Broadcaster**: Full control
- **Mods**: Diagnostic tools + moderation commands
- **VIPs**: Reduced cooldowns
- **Subscribers**: Reduced cooldowns
- **Regular viewers**: Standard cooldowns

---

## 🚀 Advanced Features

### Persistent Storage
- Message history tracking
- User activity monitoring
- Error logging for diagnostics
- Custom command storage
- SQLite database (auto-cleanup)

### OAuth Integration
- Secure Kick.com authentication
- Automatic timezone detection
- Token management
- Refresh token handling

### Real-Time Updates
- Pusher WebSocket connection
- Instant message processing
- Live chat tracking
- Sub-second response times

---

## 📈 Coming Soon

Features in development:
- Analytics dashboard
- Custom AI personality
- More game integrations
- Enhanced mod tools
- Stream overlay integration

---

## 💡 Pro Tips

**For Streamers:**
1. Set up !auth first to enable title updates
2. Configure social links during setup stream
3. Train mods to use !errors for quick troubleshooting
4. Use custom commands for FAQs

**For Mods:**
1. Check !errors when users report issues
2. Use !peffai to diagnose problems
3. Learn common fixes to help faster
4. Update social links as needed

**For Viewers:**
1. Link your gaming profiles with !setepic/!setorigin/!setsteam
2. Use !peffai to ask questions
3. Save your PC specs with !setmypc
4. Be patient with rate limits

---

**Have feature requests? Contact [@bestpeff](https://kick.com/bestpeff)!**
