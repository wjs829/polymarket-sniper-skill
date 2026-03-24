# 🌌 Polymarket Sniper Bot (Standalone) - Sales README

**The ultimate autonomous trading agent for the Polymarket prediction exchange.**

Stop manual trading and start sniping. This professional-grade OpenClaw skill provides a fully autonomous environment for scanning, analyzing, and executing momentum trades on the Polygon network.

---

## 🚀 The Value Proposition

*   **24/7 Autonomy:** Runs as a background service on your EC2 or local machine via OpenClaw. No browser needed.
*   **Momentum Edge:** Uses a proven 15-minute momentum strategy to catch price moves before the crowd.
*   **Real-Time Monitoring:** Includes a clean, dark-mode Flask dashboard to track every scan, log, and position in real-time.
*   **Security First:** Architected for "Burner Wallets" and scoped API keys. Your main funds stay safe.
*   **Agent-Native:** Built for the future of headless commerce. Pure logic, zero bloat.

---

## 🛠️ Technical Specs

*   **Runtime:** OpenClaw / Claude Code
*   **Language:** Python 3.12+
*   **Blockchain:** Polygon Mainnet (Web3.py)
*   **API:** Polymarket Gamma & CLOB (Order Book)
*   **Database:** SQLite (Local persistence)
*   **UI:** Flask + Tailwind-style CSS

---

## 📦 What’s Inside the Box?

1.  **`polymarket.py`**: The "Brain." Handles HMAC-SHA256 signing, balance verification, and execution logic.
2.  **`dashboard.py`**: The "Command Center." A local web UI for visual confirmation.
3.  **`agent.yaml`**: The "Orchestrator." Pre-configured cron schedules for Heartbeats (1m) and Scans (5m).
4.  **`bootstrap.sh`**: The "Easy Button." A one-command setup script that installs dependencies and initializes the DB.

---

## 🏁 Quick Start (Go Live in 2 Mins)

1.  **Install:** `./scripts/bootstrap.sh`
2.  **Configure:** Add your RPC URL and Private Key to `config.yaml`.
3.  **Start:** `python3 dashboard.py`
4.  **Automate:** `openclaw cron add --agent sniper-bot`

---

## 💰 Investment
**[Link to Gumroad/LemonSqueezy]**

*   **Standard License:** Full source code + setup guide.
*   **Agency License:** Permission to deploy for up to 5 clients + custom `soul.md` templates.

---
*Disclaimer: This is an experimental trading bot. Cryptocurrency markets are volatile. Use at your own risk. Not financial advice.*
