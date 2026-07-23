# 🃏 Poker Settlement Calculator

Settle up poker games with friends — handles buy-ins, rebuys, chip-by-chip counting, and generates a **Pix** QR Code + copy-and-paste code so everyone pays up in seconds.

Built as a single, self-contained HTML file. No install, no backend, works offline.

> ⚠️ The app interface is in **Portuguese (pt-BR)**.

## ✨ Features

- **Players, buy-ins & rebuys** — each player can buy in for any amount and rebuy as many times as they want.
- **Chip counting by denomination** — define chip colors and values, then count each player's final chips; the app converts to money automatically.
- **Cash-balance check** — validates that total money in equals total money out and flags any counting error *before* anyone pays.
- **Smart settlement** — figures out who pays whom using the **minimum number of transfers**.
- **Pix built in** — generates a valid Pix "copia e cola" code and QR Code with the exact amount for each transfer.
- **Local history** — past games are saved in your browser.

## 🎮 How to use

1. **Players** — add each person, their buy-in, any rebuys, and their Pix key.
2. **Chips** — set the chip denominations, then count everyone's chips at the end of the night.
3. **Settle** — see each player's result, confirm the pot balances, and share the Pix codes.

## 🚀 Live version

Hosted with GitHub Pages: **https://YOUR-USERNAME.github.io/poker**

*(Replace with your own link after enabling Pages.)*

## 🛠️ Run it locally

Just download `index.html` and open it in any browser. That's it.

## 🧠 Under the hood

- Vanilla HTML/CSS/JavaScript — zero build step, single file.
- Money is handled in **cents (integers)** to avoid floating-point rounding errors.
- Settlement uses a greedy **debt-simplification** algorithm (largest debtor ↔ largest creditor).
- Pix codes follow the **BR Code (EMV)** spec with a proper CRC16 checksum.
- Data is stored with `localStorage`.

## 📌 Good to know

History is saved **per browser/device** — the app has no central database. In practice one person (the host) runs it and shows the results to the table. If you want multiple people editing the same game live from different devices, that would require a backend.

## 🗺️ Roadmap ideas

- Long-term stats / leaderboard (biggest winners and losers over time)
- Export a game summary
- Multi-device sync

---

*My first GitHub Pages project.* Feedback and ideas welcome!
