# 🚀 Agunnaya Labs — AI + Web3 Autonomous Ecosystem

> Smart Contracts · AI Security · Blockchain Games · SaaS Infrastructure on Base Mainnet

![Auto Assign](https://github.com/Agunnaya-Labs/agunnaya-labs-showcase/actions/workflows/auto-assign.yml/badge.svg)
![Proof HTML](https://github.com/Agunnaya-Labs/agunnaya-labs-showcase/actions/workflows/proof-html.yml/badge.svg)
[![Base Mainnet](https://img.shields.io/badge/Base-Mainnet-0052FF?logo=coinbase)](https://basescan.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-38bdf8.svg)](LICENSE)

-----

## Overview

This repository is the public showcase and landing page for the **Agunnaya Labs** ecosystem — a full-stack Web3 platform combining AI-powered smart contract security, on-chain blockchain gaming, and SaaS infrastructure, all deployed on [Base mainnet](https://base.org) (Chain ID: 8453).

-----

## What’s Inside

|File                               |Purpose                                                 |
|-----------------------------------|--------------------------------------------------------|
|`index.html`                       |Single-page landing site (self-contained, no build step)|
|`.github/workflows/auto-assign.yml`|Auto-assigns reviewers/assignees on new PRs and issues  |
|`.github/workflows/proof-html.yml` |Validates HTML on every push and pull request           |

-----

## Ecosystem

### 🧠 AI Security System

|Tool                      |Description                                 |Link                                                         |
|--------------------------|--------------------------------------------|-------------------------------------------------------------|
|Smart Contract Auditor Bot|GitHub App — static analysis on Solidity PRs|[Install](https://github.com/apps/smart-contract-auditor-bot)|
|Audit Dashboard           |Live vulnerability detection interface      |[Open](https://v0-smart-contract-auditor-bot.vercel.app/)    |

**Detectors:** Reentrancy · tx.origin misuse · Unchecked low-level calls · Selfdestruct · Honeypot/rug-pull patterns · Hardcoded secrets

-----

### ⚔️ Arena Protocol — Deployed Contracts (Base Mainnet)

|Contract                   |Address                                                                                                                |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------|
|**ArenaToken** (ERC-20)    |[`0x3b855F88CB93aA642EaEB13F59987C552Fc614b5`](https://basescan.org/address/0x3b855F88CB93aA642EaEB13F59987C552Fc614b5)|
|**ArenaChampion** (ERC-721)|[`0x68f08b005b09B0F7D07E1c0B5CDe18E43CE2486A`](https://basescan.org/address/0x68f08b005b09B0F7D07E1c0B5CDe18E43CE2486A)|
|**ArenaBattle**            |[`0xF6fc2B6a306B626548ca9dF25B31a22D0f8971CF`](https://basescan.org/address/0xF6fc2B6a306B626548ca9dF25B31a22D0f8971CF)|
|**ArenaMarketplace**       |[`0x67817157Dd6E5945ac2fAf1a822e7f1dE26C698E`](https://basescan.org/address/0x67817157Dd6E5945ac2fAf1a822e7f1dE26C698E)|
|**ArenaPVP**               |[`0xd0C4Af12E95f9590e7314D079C58597771E57533`](https://basescan.org/address/0xd0C4Af12E95f9590e7314D079C58597771E57533)|

All contracts are deployed and verified on Base mainnet.

-----

### 💰 SaaS Infrastructure

- **Analytics Engine** — On-chain event indexing and wallet analytics
- **Automation System** — Trigger-based contract interactions and bot infrastructure
- **Stripe Monetization** — Fiat on-ramp with Checkout, subscriptions, and pro tier

-----

## Setup & Development

### 1. Clone

```bash
git clone https://github.com/Agunnaya-Labs/agunnaya-labs-showcase.git
cd agunnaya-labs-showcase
```

### 2. Configure Backend

In `index.html`, replace the placeholder with your actual backend URL:

```js
const API = "https://YOUR_BACKEND_URL";
```

**Required API endpoints:**

|Method|Endpoint          |Body                 |Response         |
|------|------------------|---------------------|-----------------|
|`POST`|`/events`         |`{ event, data, ts }`|`200 OK`         |
|`POST`|`/waitlist`       |`{ email }`          |`200 OK`         |
|`POST`|`/stripe/checkout`|—                    |`{ url: string }`|

### 3. Run Locally

No build step required — open directly in a browser or serve with any static server:

```bash
npx serve .
# or
python3 -m http.server 8080
```

-----

## Deploy

### GitHub Pages (Automatic)

Push to `main` and the included workflow deploys automatically:

```bash
git add .
git commit -m "feat: update landing page"
git push origin main
```

Then enable GitHub Pages in **Settings → Pages → Source: GitHub Actions**.

### Manual Deploy

Any static host works: Vercel, Netlify, Cloudflare Pages, or a CDN bucket.

-----

## Tech Stack

|Layer    |Tech                                                     |
|---------|---------------------------------------------------------|
|Frontend |Vanilla HTML/CSS/JS — no framework, no bundler           |
|Wallet   |ethers.js v6 (CDN) via EIP-1193                          |
|Fonts    |Syne (headings) + Space Mono (monospace) via Google Fonts|
|Contracts|Solidity / OpenZeppelin v5 / Hardhat                     |
|Chain    |Base Mainnet (Chain ID 8453)                             |
|CI/CD    |GitHub Actions → GitHub Pages                            |

-----

## External Dependencies

|Dependency                                                |Version|Purpose                |
|----------------------------------------------------------|-------|-----------------------|
|[ethers.js](https://docs.ethers.org/)                     |6.13.4 |Wallet connection (CDN)|
|[Syne](https://fonts.google.com/specimen/Syne)            |—      |Display font           |
|[Space Mono](https://fonts.google.com/specimen/Space+Mono)|—      |Monospace UI font      |

-----

## Links

- **GitHub Organization:** [github.com/Agunnaya-Labs](https://github.com/Agunnaya-Labs)
- **Auditor Bot:** [github.com/apps/smart-contract-auditor-bot](https://github.com/apps/smart-contract-auditor-bot)
- **Audit Dashboard:** [v0-smart-contract-auditor-bot.vercel.app](https://v0-smart-contract-auditor-bot.vercel.app/)
- **Base Explorer:** [basescan.org](https://basescan.org)

-----

## License

MIT © 2026 Agunnaya Labs
