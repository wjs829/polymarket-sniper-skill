# Polymarket Sniper Bot 🌌

Autonomous trading agent for Polymarket (Polygon). Scans 15-minute markets, detects momentum, and executes trades. Includes a Flask dashboard and OpenClaw orchestration.

> **⚠️ IMPORTANT:** This free version runs in **Simulation Mode** only. [Upgrade to Pro](#upgrade) to trade with real money.

## 🚀 Quick Start

```bash
git clone https://github.com/wjs829/polymarket-sniper-skill.git
cd polymarket-sniper-skill/scripts
chmod +x bootstrap.sh && ./bootstrap.sh
python3 dashboard.py  # Open http://localhost:5000
```

## 🧠 Strategy

- **Liquidity filter:** ≥ $1,000 (sim) / $5,000 (prod)
- **Momentum window:** 3 × 15-minute candles
- **Buy signals:** YES if momentum > +2%; NO if momentum < -2%

## 📦 Package Contents

- `polymarket.py` — Trading engine with HMAC-SHA256 signing
- `dashboard.py` — Real-time UI (Flask)
- `db.py` — SQLite persistence
- `agent.yaml` — OpenClaw cron jobs
- `bootstrap.sh` — Setup automation
- `config.yaml.example` — Configuration template
- `DEPLOYMENT.md` — Full production guide

## 💼 Monetization & Support

This skill is **free to use** in simulation mode. For live trading:

| Feature | Free (Sim) | Pro ($99) |
|---------|------------|-----------|
| Real orders | ❌ | ✅ |
| Priority support | ❌ | ✅ |
| Lifetime updates | ❌ | ✅ |
| Custom risk params | ❌ | ✅ |

**Upgrade Now:** [Buy Polymarket Sniper Bot Pro](https://wessmith3.gumroad.com/l/cmdcpl) (one-time $99)

After purchase, simply set `pro_mode: true` in your `config.yaml` to enable live trading:

```yaml
pro_mode: true
```

For enterprise/custom builds: [wessmith9822@gmail.com](mailto:wessmith9822@gmail.com)

## 📜 License
MIT — see `LICENSE` file.

