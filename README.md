# ATF Miner Bot Scripts 🚀

This collection of Python scripts automates mining, social tasks, and referral rewards on the **ATF (AITRADINGFOREX)** platform — a Telegram-based mining ecosystem where users earn **ATF** tokens by running mining sessions, completing social tasks, and inviting friends.

🔗 Register: [ATF Miner](https://t.me/AITradingForex_Bot?start=921415493)

---

## ✨ Features Overview

### General Features

- **Multi-Account Support**: Reads Telegram initData from `accounts.txt` to process multiple accounts in parallel.
- **Colorful CLI**: Uses `colorama` for visually appealing output with box-drawing borders and colored icons.
- **Asynchronous Execution**: Built with `asyncio` for efficient concurrent task processing (configurable thread count).
- **Error Handling**: Comprehensive error catching with retry logic (configurable attempts) for API failures.
- **Bilingual Support**: Supports both English and Vietnamese output.
- **Proxy Support**: Supports SOCKS5 proxies via `proxies.txt` (`host:port:user:pass` format).
- **Stable Device IDs**: Device IDs are cached in `atf_devices.json` per account for anti-detection.

---

### Included Scripts

✨ **Mining Bot** (`mining.py`)

- ✅ Automatic mining start for inactive accounts
- ✅ Math challenge auto-solving to start mining
- ✅ Automatic boost activation & mining rate display
- ✅ Detailed mining info: Level, Pool Balance, Mined Balance, Freeze Time
- ✅ Automatic claim with preview balance estimation
- ✅ ATF price & friends info display
- ✅ Proxy & multi-threading support

✨ **Task Bot** (`social.py`)

- ✅ Automatic completion of one-time tasks (join, follow, subscribe)
- ✅ Automatic completion of repeatable tasks (React latest post, website visit, Retweet, Like & Comment)
- ✅ Respects task cooldowns automatically
- ✅ Correct start → wait → claim flow for repeatable tasks
- ✅ Secure referer headers included
- ✅ Proxy & multi-threading support

✨ **Referral Claim Bot** (`claimref.py`)

- ✅ Automatic friend list fetching
- ✅ Referral reward claiming with balance & level update
- ✅ Reward per referral & team wallet display
- ✅ Proxy & multi-threading support

---

## 🛠️ Prerequisites

Before running the scripts, ensure you have the following installed:

- **Python 3.8+**
- **pip** (Python package manager)
- **Dependencies**: Install via `pip install -r requirements.txt`
- **accounts.txt**: Add Telegram initData (one per line) — obtain via browser DevTools on the ATF Miner mini app
- **proxies.txt** (optional): Add proxy addresses for network requests

---

## 📦 Installation

1. **Clone or download this repository:**
   ```sh
   git clone https://github.com/thog9/ATF-miner.git
   cd ATF-miner
   ```

2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Prepare Input Files:**

   Create `accounts.txt` in the root directory with Telegram query data (one per line):
   ```
   query_id=AAFFr-s9AAAAA...
   query_id=AAFFr-s9AAAAA...
   ```

   Create `proxies.txt` (optional) — one proxy per line:
   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ```

4. **Run:**
   ```sh
   python main.py
   ```
   - Choose a language (Vietnamese / English).
   - Select the script you want to run.

**Language Selection:**
- Choose between Vietnamese (Tiếng Việt) and English.
- All scripts support bilingual output.

---

## 📁 Project Structure

```
ATF-Miner/
├── main.py                # Central menu system
├── accounts.txt           # Telegram initData
├── proxies.txt            # Proxies (optional)
├── atf_devices.json       # Cached device IDs (auto-generated)
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── scripts/               # Individual scripts
    ├── mining.py          # Mining automation bot
    ├── social.py          # Task automation bot
    └── claimref.py        # Referral reward claim bot
```

---

## ⚙️ Environment Variables

| Variable | Default | Description |
|---|---|---|
| `ATF_MODE` | `mine` | Run mode: `mine` or `info` (display only) |
| `ATF_CYCLES` | `0` | Mining cycles (0 = unlimited) |
| `ATF_TASK_WAIT` | `60` | Wait seconds before claiming repeatable tasks |
| `ATF_REPEATABLE` | `1` | `0` to skip repeatable tasks in social.py |

---

## 📨 Contact

Connect with us for support or updates:

- **Telegram**: [thog099](https://t.me/thog099)
- **Channel**: [CHANNEL](https://t.me/thogairdrops)
- **X**: [Thog](https://x.com/thog099)

---

## ☕ Support Us

Love these scripts? Fuel our work with a coffee!

🔗 BUYMECAFE: [BUY ME CAFE](https://buymecafe.vercel.app/)

🔗 WEBSITE: [BUY SCRIPTS](https://thogtoolhub.com/)
