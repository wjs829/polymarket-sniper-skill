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
  version: "1.0.0"
  author: "innieai"
  website: "https://github.com/wjs829/polymarket-sniper-skill"
  upgrade_url: "https://wessmith3.gumroad.com/l/cmdcpl"
---

# Polymarket Sniper Bot Skill 🚀

Production-ready autonomous trading agent for Polymarket. Features real-time momentum detection, HMAC-SHA256 order signing, and a Flask dashboard.

## ✨ Features
- **Auto-Scanning:** Cron-driven market scans every 5 minutes
- **Momentum Strategy:** 15-minute candle RSI + volume surge detection
- **CLOB Integration:** Direct Polymarket order book API
- **Dashboard:** Real-time positions, balance, and logs (Flask)
- **Simulation Mode:** Paper-trade safely before going live

## 📦 What's Included
- `scripts/polymarket.py` — Core trading engine
- `scripts/dashboard.py` — Monitoring UI (Port 5000)
- `scripts/db.py` — SQLite persistence
- `scripts/agent.yaml` — OpenClaw orchestration
- `scripts/bootstrap.sh` — One-command setup
- `scripts/config.yaml.example` — Configuration template
- `DEPLOYMENT.md` — Full setup guide

## 🛠️ Quick Start
```bash
git clone https://github.com/wjs829/polymarket-sniper-skill.git
cd polymarket-sniper-skill/scripts
chmod +x bootstrap.sh && ./bootstrap.sh
python3 dashboard.py  # View at http://localhost:5000
```

## 🔑 Upgrade to Pro (Live Trading)
The free version runs in **Simulation Mode** only. Upgrade to unlock live trading.

**Price:** $99 one-time  
👉 [Buy Pro Now](https://wessmith3.gumroad.com/l/cmdcpl)

After purchase, set `pro_mode: true` in your `config.yaml` to enable live trading.

*Note: You'll need your own Polymarket API keys and funded wallet.*

## 📜 License
MIT — see LICENSE file.

