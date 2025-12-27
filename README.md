# Peffbot - Kick.com Chat Bot

An AI-powered chat bot built specifically for Kick.com streamers.

[![Status](https://img.shields.io/badge/Status-Private%20Beta-blue)](https://github.com/bestpeff/peffbot-showcase)
[![Platform](https://img.shields.io/badge/Platform-Kick.com-green)](https://kick.com)

---

## What is this?

Peffbot is a chat bot I built for my own Kick stream that handles viewer questions, displays game stats, manages social links, and helps mods troubleshoot issues without bugging me mid-stream. After testing it live for a while, I'm opening it up to other streamers.

---

## Main Features

**AI Assistant (!peffai)**
- Viewers can ask questions and get actual helpful responses (powered by Claude AI)
- Mods can use it to diagnose bot issues and get troubleshooting steps
- Handles common stream questions automatically

**Game Stats**
- Fortnite, Apex Legends, Rocket League, and CS:GO/CS2 stats
- Viewers link profiles: !setepic (Fortnite/Rocket League), !setorigin (Apex), !setsteam (CS:GO)
- Then just use !stats to pull up their current rank/stats
- CS:GO players use !csgo or !cs2 with their Steam ID

**Social Links**
- Support for 20+ platforms (Instagram, Twitter, TikTok, Discord, YouTube, etc)
- Mods can update links without broadcaster intervention
- Simple commands like !discord, !twitter, !instagram

**Mod Tools**
- !errors command shows recent failures
- AI can help diagnose what's broken
- Mods can fix most issues without waiting for you

**Spam Protection**
- Smart rate limiting that actually works (different cooldowns per role)
- Detects and filters duplicate messages automatically
- Prevents command spam without annoying regular viewers
- Protects against bot abuse and API spam

**Custom Commands**
- Create your own commands with !addcom, !editcom, !delcom
- Set up auto-timers for periodic messages
- Channel-specific or manage existing commands easily

---

## Commands

Basic commands: !followers, !viewers, !uptime, !subs, !created
Game stats: !stats, !fortnite, !apex, !rocketleague, !csgo, !cs2
Social links: !socials, !instagram, !twitter, !tiktok, !discord
AI help: !peffai <question>
Mod tools: !errors
Custom commands: !addcom, !editcom, !delcom, !listcoms

Full command list available in [FEATURES.md](FEATURES.md)

---

## See it live

Chat with Peffbot at: **[kick.com/bestpeff](https://kick.com/bestpeff)**

---

## Why invite-only?

Right now I'm manually adding channels because:
- API costs aren't cheap (Claude + other services add up)
- Want to make sure it works well for everyone before scaling
- Gives me time to add features streamers actually request
- Better support when there's fewer channels to manage

---

## Getting access

Currently in private beta. If you're interested, hit me up:

- X: [@bestpeff](https://x.com/bestpeff)
- Discord: [https://discord.gg/zvFJFQjY](https://discord.gg/zvFJFQjY)
- Kick: [@bestpeff](https://kick.com/bestpeff)

I manually review each request - just want to make sure it's a good fit.

---

## Tech Stack

Python 3.10+ with Kick.com API and Pusher WebSockets for real-time chat.

**AI:**
- Claude (Anthropic) for diagnostics and smart responses
- Grok AI for conversational stuff

**Storage:**
- SQLite for persistence

**Integrations:**
- Tracker.gg for game stats
- OAuth 2.0 for authentication

---

## Current Status

**Version:** 1.0.2 (Released December 2025)

Recently added:
- Better AI diagnostics for mods
- Message database with spam detection
- Role-based AI access
- Error tracking for easier troubleshooting

Working on:
- Analytics dashboard for viewer activity and engagement
- Train the bot to match your channel's personality and humor
- Granular mod permission controls (let specific mods do specific things)
- Multi-channel management for streamers running multiple channels

---

## FAQ

**Is it free?**
Yes for beta users. Pricing TBD if I open it up publicly.

**Can I self-host?**
No, it's a hosted service. Code is proprietary.

**What makes this different from other bots?**
Built specifically for Kick (not a Twitch port). Has AI-powered diagnostics so mods can fix issues themselves. Active development based on real streamer feedback.

**Does it work on Twitch?**
No, Kick.com only.

---

## License

© 2025 bestpeff - All Rights Reserved

Peffbot is proprietary software. No unauthorized use or distribution.

---

## Support

Questions or issues?

- Live during streams: [kick.com/bestpeff](https://kick.com/bestpeff)
- X: [@bestpeff](https://x.com/bestpeff)
- Discord: [https://discord.gg/zvFJFQjY](https://discord.gg/zvFJFQjY)

---

## Testimonials

Released December 2025, still collecting testimonials from beta users. Looking to add more streamers.

---

Built for the Kick.com community
