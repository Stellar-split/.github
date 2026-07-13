<div align="center">
  <img src="https://raw.githubusercontent.com/Stellar-split/.github/main/assets/stellarsplit-lockup.svg" alt="StellarSplit" width="320" />
  <br/><br/>
  <p><strong>On-chain invoice &amp; payment splitting on Stellar Soroban</strong> — split bills, freelancer payments, and remittances with automatic trustless USDC routing.</p>
</div>

[![Stellar](https://img.shields.io/badge/Network-Stellar-blue?logo=stellar)](https://stellar.org)
[![Soroban](https://img.shields.io/badge/Smart%20Contracts-Soroban-purple)](https://soroban.stellar.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Drips Wave](https://img.shields.io/badge/Drips-Stellar%20Wave%20Program-blueviolet)](https://drips.network/wave)
[![GrantFox](https://img.shields.io/badge/GrantFox-Approved%20Project-orange)](https://maintainer.grantfox.xyz)
[![Live App](https://img.shields.io/badge/Live-stellarsplit--dapp.vercel.app-brightgreen)](https://stellarsplit-dapp.vercel.app)

---

## What is StellarSplit?

StellarSplit lets anyone create on-chain invoices on Stellar where multiple payers each owe a share. The moment the invoice is fully funded, the Soroban smart contract **automatically routes USDC to every recipient** in a single transaction. If the deadline passes unfunded, all contributors are **automatically refunded**.

No middleman. No trust required. Just code.

---

## How it works

```
1. Creator makes an invoice
   └── Sets recipients, amounts, deadline, and optional rules

2. Payers send their share
   └── USDC is locked in the Soroban smart contract

3. Invoice fully funded
   └── Contract instantly routes USDC to every recipient

4. Deadline passes unfunded?
   └── Every payer gets their money back automatically
```

Advanced modes: require co-signer approvals before release, use an oracle to confirm off-chain conditions, set staged tranches, or schedule an automatic release timestamp.

---

## Features

- **Automatic USDC routing** — recipients are paid the moment the invoice is fully funded
- **Multi-sig release** — require N-of-M co-signer approvals before funds move
- **Staged tranches** — release funds in graduated time-locked instalments
- **Oracle-priced invoices** — dynamic funding targets set by an on-chain price oracle
- **Confidential payments** — hide payment amounts using Pedersen commitments; reveal at settlement
- **Payment channels** — stream micro-payments toward an invoice without per-tx fees
- **Invoice cloning** — clone any invoice with optional overrides, full lineage tracked on-chain
- **Subscriptions** — recurring invoice creation from stored templates
- **Fee tiers** — volume-based platform fee discounts for high-volume creators
- **Circuit breaker** — emergency pause that blocks all mutations with no exemptions
- **Cross-chain bridge payments** — accept payments relayed from other chains
- **Creator analytics** — on-chain stats: total raised, released, unique payers, average funding time

---

## Use Cases

- 💸 **Freelancer team payments** — client pays once, contract splits to the whole team
- 🍽️ **Group bills** — dinner, trips, shared purchases split trustlessly
- 🌍 **Remittances** — send payments across LATAM & Africa with near-zero fees
- 🏢 **Business invoicing** — invoice clients with automatic multi-party settlement
- 🔒 **Milestone-based contracts** — release funds only when off-chain conditions are confirmed

---

## Repositories

| Repo | Language | Description |
|---|---|---|
| [split-contracts](https://github.com/Stellar-split/split-contracts) | ![Rust](https://img.shields.io/badge/-Rust-orange?logo=rust) | Soroban smart contracts — invoice creation, payment collection, automatic USDC routing |
| [split-sdk](https://github.com/Stellar-split/split-sdk) | ![TypeScript](https://img.shields.io/badge/-TypeScript-blue?logo=typescript) | npm package (`@stellar-split/sdk`) — typed client for all contract interactions |
| [split-app](https://github.com/Stellar-split/split-app) | ![Next.js](https://img.shields.io/badge/-Next.js-black?logo=next.js) | Next.js 14 frontend — create invoices, track payments, manage splits |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Smart Contracts | Rust, Soroban SDK 22.0.0 |
| Blockchain | Stellar Network (testnet + mainnet) |
| Token | USDC via Stellar Asset Contract (SAC) |
| SDK | TypeScript 5, `@stellar/stellar-sdk` |
| Wallet | Freighter, WalletConnect |
| Frontend | Next.js 14, Tailwind CSS, PWA |

---

## Live Demo

🌐 **[stellarsplit-dapp.vercel.app](https://stellarsplit-dapp.vercel.app)**

---

## Quickstart

**Smart contracts (Rust/Soroban)**
```bash
git clone https://github.com/Stellar-split/split-contracts.git
cd split-contracts
cargo test --workspace
```

**SDK (TypeScript)**
```bash
git clone https://github.com/Stellar-split/split-sdk.git
cd split-sdk
npm install && npm test
```

**Frontend (Next.js)**
```bash
git clone https://github.com/Stellar-split/split-app.git
cd split-app
npm install && npm run dev
```

Each repository has its own `CONTRIBUTING.md` with setup details and code standards.

---

## Contributing

StellarSplit participates in two open-source contributor programs:

### Stellar Wave on Drips

An open bounty program where contributors earn rewards for completing GitHub issues. StellarSplit has **125+ open issues** across the three repositories — from Soroban contract features to SDK utilities and frontend components.

👉 **[Browse issues on Drips](https://drips.network/wave)**

### GrantFox

StellarSplit is an approved project on [GrantFox](https://maintainer.grantfox.xyz) — a Stellar ecosystem collaboration platform with additional bounty issues across all three repositories.

**Rules for both programs:**
> Do NOT start work on any issue until assigned by the maintainer.
> Comment on the issue to express interest and wait for assignment.

---

## License

MIT — see individual repositories for details.

---

<div align="center">
  <sub>Built on <a href="https://stellar.org">Stellar</a> · <a href="https://stellarsplit-dapp.vercel.app">Live App</a> · <a href="https://drips.network/wave">Stellar Wave Program</a> · <a href="https://maintainer.grantfox.xyz">GrantFox</a></sub>
</div>
