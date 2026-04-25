<p align="center">
  <img src="https://raw.githubusercontent.com/QuantumWick/HIVE-releases/main/assets/logo.png" width="128" height="128" alt="HIVE" />
</p>

<h1 align="center">HIVE</h1>

<p align="center">
  <strong>AI-Powered Trading Desktop for MetaTrader 5</strong>
</p>

<p align="center">
  <a href="https://github.com/QuantumWick/HIVE-releases/releases/latest">
    <img src="https://img.shields.io/github/v/release/QuantumWick/HIVE-releases?label=latest&color=00D9A0" alt="Latest release" />
  </a>
  <img src="https://img.shields.io/badge/platform-Windows-blue" alt="Platform" />
  <img src="https://img.shields.io/badge/license-Proprietary-red" alt="License" />
</p>

---

## Download

**[Download the latest installer](https://github.com/QuantumWick/HIVE-releases/releases/latest)**

### Which file should I pick?

| Your PC | Installer |
|---|---|
| **Most Windows PCs** (Intel or AMD) | `HIVE-*-win-x64.exe` |
| **ARM Windows laptops** (Snapdragon, Surface Pro X) | `HIVE-*-win-arm64.exe` |
| **Not sure?** | `HIVE-*-win.exe` (universal — works on both) |

> Not sure which CPU architecture your PC uses? Right-click **This PC** → **Properties** → look at **System type**. If it says "x64" → use x64. If "ARM64" → use arm64.

---

## Installation

### 1. Download the installer

Click the link above, then click the `.exe` file name to start the download. File size is ~150 MB.

### 2. Run the installer

Double-click the downloaded `.exe`.

### Windows SmartScreen Warning

You will probably see a blue warning screen saying **"Windows protected your PC"**. This is normal — the app is not code-signed with a $400/year certificate yet.

**To proceed:**
1. Click **More info** (small link)
2. Click **Run anyway**

### 3. Follow the installer

- Pick install location (default is fine)
- Choose Start menu and Desktop shortcuts (recommended)
- Click **Install**
- Click **Finish** to launch

### 4. First launch

1. The app opens to a **Sign in with Discord** screen
2. Click the button — your browser opens Discord's auth page
3. Authorize — browser redirects back — you are logged in
4. Start chatting with AI or configuring MCP servers

> **Access is invite-only.** You need to be approved by an admin to use the app. If you see a login error, contact the admin in Discord.

---

## Updates

The app auto-checks for updates on launch and every few hours.

When a new version is available:

1. **Settings → Updates** shows a prompt
2. Click **Update Now** — downloads in background
3. Click **Restart** — app quits, new version installs, app relaunches

No manual download needed. No git, no terminal.

---

## Features

### AI Chat with Multi-Provider Failover
- Connect Anthropic (Claude), OpenAI (GPT), Google (Gemini), Ollama (local), OpenRouter, and more
- Drag-and-drop priority ordering — if one provider fails, the next one takes over automatically
- Chat header shows which provider is responding in real-time

### HIVE Console — Live MT5 Trading Dashboard
- Live account balance, equity, floating P/L, free margin
- Open positions with BUY/SELL badges, profit coloring
- Auto-refresh every 10 seconds
- Mission-control view of every licensed EA across your fleet (Sharpe, Calmar, profit factor, equity curve)

### MCP Server Manager
- Configure, start/stop, monitor MetaTrader MCP servers
- MT5 toolkit: account info, place orders, run backtests, optimize EAs
- MetaEditor toolkit: compile MQL5, manage Experts, strategy tester
- One-click filesystem access — grant the AI access to any folder

### Direct Messaging
- Chat 1-on-1 with other approved users in your community
- Real-time messaging powered by Supabase
- Online/offline presence indicators
- Unread counts and admin moderation

### Skills System
- Extend the AI with custom instructions via local markdown files
- Bundled skills: risk management, strategy tester, MQL5 patterns, daily routine, news filter, and more

### Licensing & Downloads
- Per-product license keys for HIVE-distributed EAs and indicators (QuantumShift, QS Scalper, Quantum Worm, Quantum Decipher, FMS)
- Master Keys that unlock every product on a single key
- Built-in Downloads page — bundled `.zip` packages with EA, manuals, and install guides ready to drop into MT5

### Additional Features
- Auto-update built-in
- Dark/light/glass themes
- English / Chinese / Japanese interface
- Cron scheduler for recurring tasks

---

## System Requirements

| Component | Minimum | Recommended |
|---|---|---|
| **OS** | Windows 10 (64-bit) | Windows 11 |
| **CPU** | x64 or ARM64 | Intel i5+, AMD Ryzen 5+, or Snapdragon |
| **RAM** | 4 GB | 8 GB+ |
| **Disk** | 500 MB free | 2 GB free |
| **Display** | 1280×720 | 1920×1080+ |
| **Network** | Internet for AI and Discord login | Broadband |
| **MetaTrader 5** | Installed and logged in (for trading features) | — |

### Optional but recommended

- **Node.js** — needed for the filesystem MCP server (for giving AI file access)
- **MetaTrader 5** — for the trading dashboard and MT5 MCP tools
- **Discord account** — required for sign-in

---

## Getting Help

- **Something broken?** Post in the `#support` channel on Discord
- **Feature request or bug report?** DM an admin on Discord
- **Release notes** for each version: see the [Releases page](https://github.com/QuantumWick/HIVE-releases/releases)

### Common Issues

<details>
<summary><strong>"Windows protected your PC" won't let me install</strong></summary>

This is Microsoft SmartScreen — normal for unsigned apps. Click **More info** → **Run anyway**.

If that button is missing, your Windows admin has blocked unsigned apps. Try installing from an admin account or ask your admin to add an exception.

</details>

<details>
<summary><strong>App crashes on startup</strong></summary>

1. Make sure you are running Windows 10 or newer
2. Try running as Administrator (right-click shortcut → Run as administrator)
3. Uninstall and reinstall — make sure you picked the right architecture (x64 vs arm64)
4. If still broken, post logs in Discord `#support`. Log location: `%APPDATA%\DegenDevOps\logs\`

> Note: the log folder is named `DegenDevOps\logs` (legacy path kept so existing installs are not broken). HIVE is the same app — the folder will be renamed in a future release.

</details>

<details>
<summary><strong>"Sign in with Discord" fails or redirects to a broken page</strong></summary>

1. Make sure your default browser is a modern one (Chrome, Edge, Firefox)
2. After Discord authorization, your browser should redirect to `degendevops://...` (legacy custom protocol — kept for backward compat). If your browser asks "what app should open this link?", pick **HIVE**
3. If you are not on the admin's approved user list, login will fail silently — contact the admin in Discord

</details>

<details>
<summary><strong>MT5 Dashboard shows "Disconnected"</strong></summary>

1. Make sure MT5 is running and logged into your broker
2. In MT5: **Tools → Options → Expert Advisors → check Allow algorithmic trading**
3. In HIVE: **MCP Servers** page — confirm `mt5-mcp-server` shows green "Running" badge
4. If not running, click **Start** on that server card

</details>

<details>
<summary><strong>Update fails to install</strong></summary>

1. Close the app completely (check system tray — right-click icon → Quit)
2. Try updating again via **Settings → Updates → Check for Updates → Update Now**
3. Still failing? Download the latest installer manually from this page and run it over your existing install — settings are preserved

</details>

---

## Privacy & Security

- **Your API keys** are stored encrypted in your Windows user account (via OS keychain). Never sent anywhere except the AI provider you have chosen.
- **Your chat history** is stored locally on your PC at `%USERPROFILE%\.degendevops\sessions\` (legacy folder name)
- **Direct messages** are stored in our Supabase database with Row-Level Security — only you and the recipient can read them
- **Discord login** grants us your Discord username, avatar, and email — nothing else
- **No telemetry.** We do not track what you do in the app.

---

## License

Proprietary. Distributed to approved users only. Do not redistribute the installer or share it outside the approved community.

---

## Credits

Built by the HIVE team at Quantum Labs. Powered by:
- [Electron](https://www.electronjs.org/)
- [Anthropic Claude](https://www.anthropic.com/) and [Model Context Protocol](https://modelcontextprotocol.io/)
- [Supabase](https://supabase.com/) (auth and DMs)
- [MetaQuotes MetaTrader 5](https://www.metaquotes.net/)

---

<p align="center">
  <strong><a href="https://github.com/QuantumWick/HIVE-releases/releases/latest">Download Latest Release</a></strong>
</p>
