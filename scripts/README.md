# Polymarket Sniper Bot (Standalone) 🌌

An autonomous trading agent designed for **Polymarket** (Polygon network). It scans 15-minute crypto markets for momentum signals and executes trades automatically.

## 🚀 Quick Start

1.  **Bootstrap:** Run the setup script to install dependencies and initialize the database.
    ```bash
    ./scripts/bootstrap.sh
    ```
2.  **Configure:** Edit `config.yaml` with your **Polygon RPC URL** and **Wallet Private Key**.
3.  **Run Dashboard:** Start the local UI to monitor the bot's activity.
    ```bash
    python3 dashboard.py
    ```
4.  **Orchestration:** Use **OpenClaw** to schedule the bot's background tasks.
    ```bash
    openclaw cron add --agent polymarket-sniper
    ```

## 🛠️ Tech Stack

*   **Runtime:** OpenClaw (Orchestration & Scheduling)
*   **Language:** Python (Trading Logic)
*   **Web3:** Web3.py (Interacting with Polygon)
*   **Database:** SQLite (Local storage of positions, logs, heartbeats)
*   **UI:** Flask (Real-time monitoring dashboard)
*   **Alerts:** Discord Webhooks

## 🧠 Strategy: Momentum Sniping

The bot filters for crypto markets with over **$5,000 liquidity** and calculates price momentum over a **3-period window (15m each)**.

*   **Buy YES:** If momentum > +2% (0.02)
*   **Buy NO:** If momentum < -2% (-0.02)

---

## 🗺️ Roadmap

- [x] Base project structure (Standalone)
- [x] Momentum-based scanning logic
- [x] Flask monitoring dashboard
- [x] OpenClaw orchestration (agent.yaml)
- [ ] Transition from simulated to on-chain execution (CTF/CLOB)
- [ ] Real-time P&L tracking based on current market prices
- [ ] Add Chart.js to the dashboard for visual performance tracking
- [ ] Strategy refinement (e.g., volume-weighted momentum)

---

*This bot is an autonomous agent. Use with caution. Not financial advice.*
