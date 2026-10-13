<div align="center">

```
    _   _   _ ____   ___  ____    _    
   / \ | | | |  _ \ / _ \|  _ \  / \   
  / _ \| | | | |_) | | | | |_) |/ _ \  
 / ___ \ |_| |  _ <| |_| |  _ </ ___ \ 
/_/   \_\___/|_| \_\\___/|_| \_/_/   \_\

```

<h3>A feature-rich Discord bot paired with a sleek Next.js dashboard</h3>

[FORKED FROM RAYEXO]

<a href="https://nexiohost.in"><img src="https://img.shields.io/badge/⭐%20PREMIUM%20HOSTING-NexioHost-FFD700?style=for-the-badge&labelColor=1a1a2e&color=FFD700&logoColor=FFD700"/></a>

<p>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white"/></a>
  <a href="https://nextjs.org"><img src="https://img.shields.io/badge/Next.js-14+-000000?style=for-the-badge&logo=nextdotjs&logoColor=white"/></a>
  <a href="https://fastapi.tiangolo.com"><img src="https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white"/></a>
  <a href="https://discordpy.readthedocs.io"><img src="https://img.shields.io/badge/Discord.py-v2-5865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
</p>
<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-red?style=for-the-badge"/></a>
  <a href="https://discord.gg/codexdev"><img src="https://img.shields.io/badge/Discord-Join_Server-5865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
  <a href="https://youtube.com/@CodeXDevs"><img src="https://img.shields.io/badge/YouTube-CodeXDevs-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/></a>
  <a href="https://github.com/RayExo"><img src="https://img.shields.io/badge/GitHub-RayExo-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
</p>

</div>

---

## ✦ Overview

Aurora is a fully-featured Discord bot with a modern web dashboard for managing everything from antinuke to music. Built on `discord.py v2`, `FastAPI`, and `Next.js 14` with Tailwind CSS.

```
ZyroX-CV2-With-Dashboard/
├── 🤖  bot/                   Python Discord bot + FastAPI backend
│   ├── api/                   Dashboard REST API (FastAPI)
│   ├── cogs/                  All bot features (commands, events, antinuke, automod…)
│   ├── core/                  Bot client, context, cog base
│   ├── utils/                 Shared utilities (emoji, tools, sync, cloudflare tunnel…)
│   ├── games/                 Standalone game modules
│   ├── assets/                Fonts, backgrounds, GIFs
│   └── CodeX.py               Entry point
│
└── 🌐  dashboard/             Next.js frontend
    ├── app/                   App Router pages & API routes
    ├── components/            Reusable UI components
    ├── hooks/                 Custom React hooks
    ├── lib/                   API helpers & utilities
    └── types/                 TypeScript type definitions
```

---

## ✦ Features

<table>
<tr>
<td width="50%">

**🛡️ Security**
- Antinuke — ban, kick, channel & role flood, webhook abuse, bot adds, prune
- Automod — spam, caps, links, invites, mass mentions, emoji spam
- Anti-member update protection
- Whitelist / unwhitelist system
- Emergency lockdown mode

</td>
<td width="50%">

**🎵 Music**
- Lavalink v4 powered playback
- YouTube, SoundCloud, JioSaavn search
- Queue, loop, autoplay, shuffle
- Seek, rewind, forward controls
- Fully configurable via `.env`

</td>
</tr>
<tr>
<td>

**⚙️ Management**
- Moderation — ban, kick, mute, warn, lock, jail, and more
- Full logging system
- Reaction roles, vanity roles, invite tracker
- Tickets, giveaways, verification
- Join-to-create voice channels

</td>
<td>

**🌐 Dashboard**
- Discord OAuth2 login
- Per-server settings management
- Live bot stats & metrics
- Fully branded & customisable
- HTTPS via Cloudflare Tunnel (permanent URL)
- Deploys to Vercel in minutes

</td>
</tr>
<tr>
<td>

**🎉 Engagement**
- Leveling & XP system with leaderboard
- Birthday tracker
- 12+ mini-games (chess, battleship, wordle, 2048…)
- AFK system, autorole, autoresponder, sticky messages
- Counting, blackjack, slots, booster perks

</td>
<td>

**🔧 Developer**
- Application emoji auto-sync on startup
- Jishaku eval support
- Slash + prefix commands
- FastAPI backend with API key auth + rate limiting
- Cloudflare Tunnel — unlimited bandwidth, permanent URL, zero system installs
- CodeX Devs watermark on every source file

</td>
</tr>
</table>

---

## ✦ Prerequisites

| Requirement | Version / Notes |
|---|---|
| Python | 3.10 or higher |
| Node.js | 18 or higher |
| Lavalink node | v4 |
| Discord bot token | — |
| Discord OAuth app | for dashboard login |
| Cloudflare account (free) | for HTTPS tunnel |

---

## ✦ Bot Setup

**1 — Clone the repo**

```bash
git clone https://github.com/nypryt/Aurora-Bot
cd Aurora-Bot/bot
```

**2 — Install dependencies**

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux / macOS
source .venv/bin/activate

pip install -r requirements.txt
```

**3 — Configure the environment**

Copy `.env.example` to `.env` and fill in the values:

```env
# ── Core ──────────────────────────────────────────────────────────
TOKEN              = your_discord_bot_token
brand_name         = 'Aurora'

# ── Owner IDs (comma-separated) ───────────────────────────────────
OWNER_IDS          = 1538065635223937026

# ── Lavalink ──────────────────────────────────────────────────────
LAVALINK_HOST      = "your-lavalink-host"
LAVALINK_PASSWORD  = "your_password"
LAVALINK_SECURE    = "true"
LAVALINK_PORT      = ""

# ── Emoji Sync ────────────────────────────────────────────────────
EMOJI_SYNC         = "true"

# ── API / Dashboard Backend ───────────────────────────────────────
API_ENABLED        = "true"
API_PORT           = "8000"
DASHBOARD_API_KEY  = "change_this_to_a_strong_secret"
CORS_ORIGINS       = ""

# ── Cloudflare Tunnel ─────────────────────────────────────────────
TUNNEL_ENABLED     = "true"
CF_TUNNEL_TOKEN    = "your_tunnel_token"
CF_TUNNEL_URL      = "https://api.yourdomain.com"

# ── Webhooks ──────────────────────────────────────────────────────
WEBHOOK_URL        = "https://discord.com/api/webhooks/..."
```

**4 — Run the bot**

```bash
python CodeX.py
```

---

## ✦ Dashboard Setup

**1 — Install dependencies**

```bash
cd dashboard
npm install
```

**2 — Configure the environment**

Copy `.env.example` to `.env.local`:

```env
NEXT_PUBLIC_API_URL           = https://api.yourdomain.com/api/v1
NEXT_PUBLIC_DASHBOARD_API_KEY = your_shared_api_key

NEXTAUTH_URL                  = http://localhost:3000
NEXTAUTH_SECRET               = a_long_random_string

DISCORD_CLIENT_ID             = your_discord_oauth_client_id
DISCORD_CLIENT_SECRET         = your_discord_oauth_client_secret

NEXT_PUBLIC_ADMIN_IDS         = your_discord_user_id
NEXT_PUBLIC_BRAND_NAME        = "ZyroX"
NEXT_PUBLIC_BRAND_NAME_WORD   = "ZX"
```

**3 — Run locally**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

---

## ✦ Environment Reference

### Bot — `bot/.env`

| Variable | Default | Description |
|---|---|---|
| `TOKEN` | — | Discord bot token |
| `OWNER_IDS` | — | Comma-separated owner Discord user IDs |
| `LAVALINK_HOST` | — | Lavalink server hostname (no protocol) |
| `LAVALINK_PASSWORD` | — | Lavalink password |
| `LAVALINK_SECURE` | `true` | `true` = HTTPS, `false` = HTTP |
| `LAVALINK_PORT` | _(empty)_ | Port — only needed when `LAVALINK_SECURE=false` |
| `EMOJI_SYNC` | `true` | Run application emoji sync on startup |
| `API_ENABLED` | `true` | Start the FastAPI dashboard backend |
| `API_PORT` | `8000` | Port the backend listens on |
| `DASHBOARD_API_KEY` | — | Shared secret between bot API and dashboard |
| `CORS_ORIGINS` | _(empty)_ | Extra CORS-allowed origins, comma-separated |
| `WEBHOOK_URL` | — | Discord webhook for command logs |
| `TUNNEL_ENABLED` | `true` | Expose the API over HTTPS via Cloudflare Tunnel |
| `CF_TUNNEL_TOKEN` | — | Token from Cloudflare Zero Trust dashboard |
| `CF_TUNNEL_URL` | — | Your permanent public URL (e.g. `https://api.yourdomain.com`) |

### Dashboard — `dashboard/.env.local`

| Variable | Description |
|---|---|
| `NEXT_PUBLIC_API_URL` | Full URL to the bot's FastAPI backend — use Cloudflare Tunnel URL |
| `NEXT_PUBLIC_DASHBOARD_API_KEY` | Must match `DASHBOARD_API_KEY` in the bot |
| `NEXTAUTH_URL` | Your dashboard's public URL |
| `NEXTAUTH_SECRET` | Random secret for NextAuth session signing |
| `DISCORD_CLIENT_ID` | Discord OAuth2 client ID |
| `DISCORD_CLIENT_SECRET` | Discord OAuth2 client secret |
| `NEXT_PUBLIC_ADMIN_IDS` | Comma-separated Discord user IDs with admin access |
| `NEXT_PUBLIC_BRAND_NAME` | Bot name shown in the dashboard UI |
| `NEXT_PUBLIC_BRAND_NAME_WORD` | Short abbreviation shown in the dashboard |

---

## ✦ HTTPS Tunnel (Cloudflare)

The bot uses **pycloudflared** — a Python package that downloads the `cloudflared` binary automatically on first run. No CLI installs, no system packages — works on Pterodactyl and any Python host.

**Why Cloudflare over ngrok:**
- ✅ Unlimited bandwidth & requests — no monthly caps
- ✅ Permanent URL that never changes between restarts
- ✅ Free — no paid plan needed
- ✅ Zero system installs — binary downloads via Python

**Setup (browser only, no CLI needed):**

1. Go to [one.dash.cloudflare.com](https://one.dash.cloudflare.com) → **Networks → Tunnels → Create a tunnel**
2. Choose **Cloudflared**, give it a name (e.g. `zyrox-api`), save
3. On the **Install connector** step, copy the token from the command shown:
   ```
   cloudflared tunnel run --token <COPY_THIS>
   ```
4. Go to **Public Hostname** tab → add a hostname:
   - Subdomain: `api` · Domain: `yourdomain.com` · Service: `http://localhost:8000`
5. Add to `bot/.env`:
   ```env
   CF_TUNNEL_TOKEN = "eyJhIjoiXXXX..."
   CF_TUNNEL_URL   = "https://api.yourdomain.com"
   ```

On every startup the console prints:
```
◈ Tunnel: cloudflared binary ready — starting tunnel on port 8000…
◈ Tunnel: API is live at  https://api.yourdomain.com
  ↳ NEXT_PUBLIC_API_URL = https://api.yourdomain.com/api/v1
```

---

## ✦ Deployment

### 🤖 Bot — any Python host

1. Upload the entire `bot/` folder to your host (Pterodactyl, Render, Railway, Fly.io, VPS…)
2. Set the start command to `python CodeX.py`
3. Add all environment variables
4. `pycloudflared` downloads the binary automatically on first run — no extra steps

> Recommended free/cheap hosts: Render · Railway · Fly.io · VPS
>
> ⭐ **[NexioHost](https://nexiohost.in)** — Premium bot hosting, built for Discord bots. Fast, reliable, and affordable.

### 🌐 Dashboard — Vercel

1. Go to [vercel.com](https://vercel.com) → **Add New Project** → connect your GitHub repo
2. Set root directory to `dashboard/`
3. Add all environment variables under **Settings → Environment Variables**
4. Add the OAuth redirect URI in Discord Developer Portal:
   ```
   https://your-app.vercel.app/api/auth/callback/discord
   ```
5. Hit **Deploy** — done ✓

---

## ✦ Emoji Sync

Runs automatically on startup when `EMOJI_SYNC=true`:

```
★ Starting Application Emoji Sync — 144 unique emojis found in emoji.py
◈ Found 144 templates | Application hosts 202 emojis
↑ Uploading: ztick  (not in application emojis)
✔ Uploaded: ztick  [saved as ID: 1234567890]
✔ emoji.py patched in-place to reflect current API state.
★ Restarting bot to load updated emoji IDs...
```

| Event | Action |
|---|---|
| New emoji found | Uploaded to application, ID written to `emoji.py` |
| Stale ID detected | `emoji.py` patched automatically |
| No changes | Sync completes instantly, no restart |
| After any patch | Bot restarts itself so fresh IDs are live |

---

## ✦ Troubleshooting

| Problem | Fix |
|---|---|
| Bot fails to start | Check `TOKEN` is set and bot has correct gateway intents |
| Music not working | Verify `LAVALINK_HOST`, `LAVALINK_SECURE`, and `LAVALINK_PORT` |
| Dashboard auth error | Check Discord OAuth client ID/secret and redirect URI |
| Dashboard can't load data | Confirm `API_ENABLED=true`, bot is running, `NEXT_PUBLIC_API_URL` is correct |
| Emojis showing as plain text | Run with `EMOJI_SYNC=true` once to upload and patch IDs |
| CORS errors from dashboard | Add your Vercel URL to `CORS_ORIGINS` in `bot/.env` |
| Tunnel not starting | Check `CF_TUNNEL_TOKEN` is valid and `pycloudflared` is installed |
| Tunnel URL changed | Set `CF_TUNNEL_URL` — named tunnels always produce the same URL |

---

## ✦ Security

- Never commit `.env` files — `.gitignore` already covers them
- Use a strong, unique `NEXTAUTH_SECRET` and `DASHBOARD_API_KEY`
- Rotate any secret that gets accidentally exposed
- The bot API is always behind an API key — never expose it without one

---

<div align="center">

## ✦ CodeX Devs

*Built for protection. Designed for style.*

<a href="https://discord.gg/codexdev"><img src="https://discord.com/api/guilds/1301573144817045524/widget.png?style=banner2" alt="CodeX Development Discord Server" width="480"/></a>

<p>
  <a href="https://discord.gg/codexdev"><img src="https://img.shields.io/badge/Discord-Join_Server-5865F2?style=for-the-badge&logo=discord&logoColor=white"/></a>
  <a href="https://youtube.com/@CodeXDevs"><img src="https://img.shields.io/badge/YouTube-CodeXDevs-FF0000?style=for-the-badge&logo=youtube&logoColor=white"/></a>
  <a href="https://github.com/RayExo"><img src="https://img.shields.io/badge/GitHub-RayExo-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
  <a href="https://nexiohost.in"><img src="https://img.shields.io/badge/⭐%20PREMIUM%20HOSTING-NexioHost-FFD700?style=for-the-badge&labelColor=1a1a2e&color=FFD700&logoColor=FFD700"/></a>
</p>

© 2026 CodeX Devs — MIT License

</div>
