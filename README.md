# TradingEngine — On-chain Long/Short Trading Logic

## Overview
TradingEngine is a Solidity smart contract that demonstrates the core mechanics of an on-chain trading protocol.  
It supports **long and short positions**, **stop-loss / take-profit execution**, **PnL calculation**, **protocol fees**, and **liquidation logic**, designed with **keeper-style automation** in mind.

This project focuses on **protocol logic**, not UI.

---

## Features
- Long & short trades
- Margin-based positions
- Stop-loss & take-profit enforcement
- Signed PnL calculation
- Protocol fee accounting (0.1%)
- Liquidation when losses exceed margin
- Event-driven design for bots & keepers

---

## Trade Lifecycle
1. User deposits ETH
2. User opens a trade (LONG or SHORT)
3. Price updates via oracle (mock)
4. Keepers monitor conditions
5. Trade is closed or liquidated automatically

---

## Automation & Keepers
The contract is designed so **anyone** can trigger trade execution.
All rules are enforced on-chain, allowing:
- Chainlink Automation
- Gelato
- Custom off-chain bots

---

## Oracle Design
This project uses a **mock oracle** for simplicity.

In production, this should be replaced with:
- Chainlink Price Feeds
- TWAP-based pricing
- Manipulation checks

---

## Security Considerations
- No trusted keepers
- All trade conditions verified on-chain
- Liquidation prevents negative balances
- Signed arithmetic used for PnL

---

## Disclaimer
This project is for educational and portfolio purposes only.  
It is **not audited** and should not be used in production without proper security review.

## Developer
- Derick spoiler
