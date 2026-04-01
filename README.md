# Project: Unknown

> A Minecraft anonymity & detective plugin for Paper 1.21.x  
> Made by **@agent0.0_9**

---

## What is it?

Project: Unknown hides every player's identity on the server. All players share the same nickname, skin, and a unique fake UUID — making it impossible to tell who is who. The goal is to find and catch other players using the tools the plugin provides.

---

## Features

- 🎭 **Full Anonymity** — All players are renamed to `Player` with a shared skin and a unique fake UUID
- 🧭 **Detective's Compass** — Right-click to track a random player. Shows direction arrow, distance, and a countdown timer on your action bar
- 🔔 **Bell of Truth** — Place and ring a special bell to reveal the real identity of nearby players temporarily (glowing + red name)
- ⚔️ **Catching System** — Kill a player with a sword named after their real name to catch and ban them
- 📢 **Anonymous Messages** — Join, quit, death, and advancement messages never reveal real names
- 🔄 **Auto skin & nick on join** — Applied automatically when a player joins

---

## CRITICAL DEPENDENCY

- [NickAPI](https://www.spigotmc.org/resources/nickapi.26013/) 7.11+ (Use the fixed verison)
- Without The [NickApi] The Project:Unknown would not work.

---

## Installation

1. Drop `ProjectUnknown-1.1.jar` and `NickAPI-7.11-fixed.jar` into your `plugins/` folder
2. Restart the server
3. Edit `plugins/ProjectUnknown/config.yml` to your liking
4. Use `/projectunknown give <player> detectivecompass` or `belloftruth` to hand out items

---

## Commands

| Command | Description |
|---|---|
| `/projectunknown reload` | Reload the config |
| `/projectunknown give <player> detectivecompass` | Give a Detective's Compass |
| `/projectunknown give <player> belloftruth` | Give a Bell of Truth |

**Permission:** `projectunknown.admin` (default: op)

---

## Config

```yaml
anonymity:
  enabled: true
  nickname: "Player"
  skin: "sondog1"
  join-message: "&ePlayer joined the game"
  quit-message: "&ePlayer left the game"

detectives-compass:
  tracking-duration: 300   # seconds
  cooldown: 300             # seconds

bell-of-truth:
  radius: 8.0               # blocks
  duration: 200             # ticks (~10 seconds)
  cooldown: 300             # seconds

catching:
  enabled: true
  ban-duration: -1          # -1 = permanent
  messages:
    ban-reason: "&cYou have been caught."
```

---

## How the Catching System Works

1. Find out a player's real name (via compass, bell, or deduction)
2. Rename a sword to their exact real username using an anvil
3. Kill them with that sword — they get banned and everyone is notified

---

## License

This project is not open sourced. don't modify or change anything in the orginal plugin. Got permission by **Lusik21556** to fork it.
Original plugin by **Lusik21556**, updated and maintained by **@agent0.0_9**.
- And this is the fork of the Original Project: Unknown. So I do not claim any credit for the original gameplay concept Thnak You..