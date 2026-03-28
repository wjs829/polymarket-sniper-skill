---
name: polymarket-sniper
description: An autonomous trading agent for Polymarket (Polygon). Scans 15-minute markets for momentum and trades automatically. Includes dashboard, simulation mode, and live execution.
metadata:
  openclaw:
    emoji: "🤖"
  tags:
    - "trading"
    - "crypto"
    - "automation"
    - "momentum"
  license: "MIT"
upgrade_url: https://wessmith3.gumroad.com/l/cmdcpl
  version: "1.0.1"
  author: "innieai"
  website: "https://github.com/wjs829/polymarket-sniper-skill"
---

# Polymarket Sniper Bot Skill 🚀

**Production-ready autonomous trading agent for Polymarket** — built with security, observability, and deployment in mind. Features real-time momentum detection, HMAC-SHA256 order signing, and a Flask dashboard.

## ✨ Features
- **Auto-Scanning:** Cron-driven market scans every 5 minutes
- **Momentum Strategy:** 15-minute candle RSI + volume surge detection
- **CLOB Integration:** Direct Polymarket order book API
- **Dashboard:** Real-time positions, balance, and logs (Flask)
- **Simulation Mode:** Paper-trade safely before going live
- **License Enforcement:** Optional server-side license validation via Railway (prevents unauthorized use)
- **Persistent Storage:** Postgres‑backed for reliable state across restarts

## 🛠️ Production‑Ready
Unlike hobbyist agents, this skill is designed for production:
- **Deployment guide** (`DEPLOYMENT.md`) covers Railway, Docker, and VPS setup
- **Isolated execution** — run in its own environment; no access to your main workstation files
- **Observability** — structured logs, health endpoint, and dashboard
- **Secure secrets** — API keys stored in environment variables; recommended use of secret manager (e.g., AgentCreds)
- **Idempotent operations** — avoids duplicate orders and handles network hiccups

## 📦 What's Included
- `scripts/polymarket.py` — Core trading engine
- `scripts/dashboard.py` — Monitoring UI (Port 5000)
- `scripts/db.py` — Postgres persistence (SQLite for local dev)
- `scripts/agent.yaml` — OpenClaw orchestration
- `scripts/bootstrap.sh` — One-command setup
- `scripts/config.yaml.example` — Configuration template
- `DEPLOYMENT.md` — Full setup guide (Railway, Docker, security hardening)
- `LICENSE_SERVER.md` — Optional license server integration

## 🛡️ Security Considerations
This agent executes real financial transactions. Follow these best practices:
- **Run in a sandbox** — separate VM or container; never on your personal desktop
- **Least‑privilege credentials** — create a dedicated Polymarket API key with only trading permissions
- **Enable MFA** on your Polymarket and wallet accounts
- **Use a hardware wallet** for signing transactions; keep private keys offline
- **Monitor logs** — set up alerts for unexpected trades or errors
- **Upgrade path** — purchase a PRO license to access advanced risk controls and priority support

## 🚀 Quick Start
```bash
git clone https://github.com/wjs829/polymarket-sniper-skill.git
cd polymarket-sniper-skill/scripts
chmod +x bootstrap.sh && ./bootstrap.sh
python3 dashboard.py  # View at http://localhost:5000
```

## 📜 License
MIT — see LICENSE file. Commercial use requires a PRO license for advanced features.
