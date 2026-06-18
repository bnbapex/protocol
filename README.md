<div align="center">

<img src="https://bnbapex.com/og-image.png" width="600" alt="bnbAPEX — BNB Automated Payout Exchange" />

# bnbAPEX

**BNB Automated Payout Exchange**

*A trustless, self-liquidating yield protocol on BNB Smart Chain*

[![Website](https://img.shields.io/badge/website-bnbapex.com-F0B90B?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyeiIvPjwvc3ZnPg==)](https://bnbapex.com)
[![Whitepaper](https://img.shields.io/badge/whitepaper-v1.2-F0B90B?style=flat-square)](https://bnbapex.com/whitepaper.pdf)
[![Telegram](https://img.shields.io/badge/telegram-@bnbapex-2CA5E0?style=flat-square&logo=telegram)](https://t.me/bnbapex)
[![Twitter](https://img.shields.io/badge/x-@bnbapex-000000?style=flat-square&logo=x)](https://x.com/bnbapex)
[![BscScan](https://img.shields.io/badge/bscscan-verified-0ECB81?style=flat-square)](https://bscscan.com/address/0x8a12167cf620a9659112f5ac9b102518b1783a6f)
[![Bitcointalk](https://img.shields.io/badge/bitcointalk-ANN-F7931A?style=flat-square)](https://bitcointalk.org/index.php?topic=5586103.0)

</div>

---

## What It Is

Commit 1 BNB. The protocol splits it immediately: 30% flows to your referral chain in the same transaction — on-chain, atomic, no intermediary. The remaining 70% buys APXB tokens on PancakeSwap.

The protocol then mints the shortfall between what 70% purchased and what the full 1 BNB would have purchased — crediting the participant with the full 1 BNB equivalent in tokens.

Those tokens vest over 30 days. Each day, 1/30th sells automatically on PancakeSwap and BNB lands in your wallet. No app to open. No button to press. No one to ask.

The protocol guarantees token quantity. BNB output follows market price at the time of each daily sell.

---

## Deployed Contracts — BNB Smart Chain (Chain ID 56)

| Contract | Address | Status |
|---|---|---|
| SystemToken (APXB) | `0x6ee58335d798a2fa184a7c8335945861c661bd0d` | ✅ Verified · Renounced |
| Validator V1 | `0x2fa2d4a5fb09125513f3b5c84d95f2db66eade6f` | ✅ Verified |
| LiquidityVault | `0xe243b7094342d2525219edf0d01ed4fec1e6b4ee` | ✅ Verified |
| MatrixCore | `0x8a12167cf620a9659112f5ac9b102518b1783a6f` | ✅ Verified |
| ValidatorV2 NFT | `0x7632de766e8c21a9a315e3431133e89f427b8c75` | ✅ Verified |
| ProtocolRegistry | `0x92813e8ffdb64abdcc6151f4ed62bfdc01df0e33` | Unverified — intentional (fork resistance) |

---

## Protocol Mechanics

### Package Purchase — Value Flow

```
1 BNB committed
├── 30% → Referral chain (L1: 15%, L2: 9%, L3: 6%) — atomic, same transaction
└── 70% → PancakeSwap V2 → APXB tokens (T70)
         Protocol mints shortfall → T100 (full 1 BNB equivalent in tokens)
         T100 vests over 30 days
         Each day: 1/30 sold on DEX → BNB → user wallet
```

### Two-Tier Validator Economy

**V1 — 100 founding positions (permanently closed)**
- Package claim fees on every daily claim
- 20% of every V2 contribution (protocol constant)
- 5% ERC-2981 royalty on every V2 NFT secondary sale (bytecode immutable)
- Compressed referral commissions

**V2 — Unlimited NFT positions (10 BNB minimum)**
- 30% of each new contribution, pro-rata by position weight
- O(1) pull-payment accumulator — gas cost does not grow with holder count
- ERC-721 — tradeable on OpenSea and any NFT marketplace
- On-chain dynamic SVG metadata — unique image per token, no server

### ERC-2981 Royalties

5% of every V2 NFT secondary sale routes permanently to the V1 founding pool. The recipient address is `address public immutable` in the contract — compiled into bytecode, physically unchangeable.

---

## Token — APXB

| Property | Value |
|---|---|
| Name | APXB Token |
| Symbol | APXB |
| Network | BNB Smart Chain (Chain ID 56) |
| Decimals | 18 |
| Supply | Uncapped — every mint backed by BNB entering the DEX |
| Transfer fee | None |
| Blacklist | None |
| Trading pause | None |
| Ownership | Renounced |

---

## No Pre-Sale

No pre-sale. No private round. No VC allocation. No team token.

The founding team holds genesis validator positions in the V1 pool, declared transparently in the [whitepaper](https://bnbapex.com/whitepaper.pdf) Section 8. Their stake is their early participation in the protocol they built — visible on-chain to anyone.

---

## Ownership

Token contract (APXB) ownership is renounced. Protocol contracts retain owner access during the stabilisation period for parameter adjustment, after which they will be renounced. Full timeline documented in the whitepaper.

The founding team has transitioned to anonymity. The contracts are the protocol. The whitepaper is the complete record.

---

## Links

| | |
|---|---|
| 🌐 Website | [bnbapex.com](https://bnbapex.com) |
| 📄 Whitepaper | [bnbapex.com/whitepaper.pdf](https://bnbapex.com/whitepaper.pdf) |
| 💬 Telegram | [t.me/bnbapex](https://t.me/bnbapex) |
| 🐦 X / Twitter | [x.com/bnbapex](https://x.com/bnbapex) |
| 🔍 BscScan | [MatrixCore](https://bscscan.com/address/0x8a12167cf620a9659112f5ac9b102518b1783a6f) |
| 📈 CMC DEX | [APXB on CoinMarketCap DEX](https://dex.coinmarketcap.com/token/bsc/0x6ee58335d798a2fa184a7c8335945861c661bd0d/) |
| 🥞 PancakeSwap | [Buy APXB](https://pancakeswap.finance/swap?outputCurrency=0x6ee58335d798a2fa184a7c8335945861c661bd0d) |
| 📢 Bitcointalk | [ANN Thread](https://bitcointalk.org/index.php?topic=5586103.0) |

---

<div align="center">
<sub>BNB Smart Chain · Chain ID 56 · Deployed 29 May 2026 · ValidatorV2 v1.1.0: 31 May 2026</sub>
</div>
