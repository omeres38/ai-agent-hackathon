# AgenticPay — Programmable Payments for AI Agents

> Crypto World's Fair hackathon prototype · Early-stage

AgenticPay explores a programmable payment-control layer for autonomous AI agents. An owner defines spending policies; a payment request is evaluated against those rules; the demo explains why the request passes or is rejected.

## What the prototype currently demonstrates

- Set an agent name, daily spending limit, and per-payment limit.
- Choose a payment recipient and purpose.
- Mark whether a recipient is verified/allowlisted.
- Evaluate payment requests against the local policy rules.
- Approve or reject requests with a readable reason.
- Track simulated daily usage and a local decision history.
- Reset the local demo state.

## Run locally

Open `index.html` in a modern browser. No install, API key, wallet, or build step is required.

## Current implementation boundary

This repository contains a **browser-based simulation**. It does not connect to a wallet, hold or transfer real assets, create private keys, call a live AI model, or submit Solana transactions. All payment decisions and balances are local demo state.

Solana and USDC are proposed for a future settlement layer. They are not integrated in this version. The current local policy logic is illustrative and must not be treated as a production security boundary.

## Demo flow

1. Keep the daily limit at 25 USDC and the per-payment limit at 10 USDC.
2. Request a 2 USDC payment to the verified example recipient. The local rules should approve it as a simulation.
3. Change the amount to 12 USDC. The local rules should reject it because it exceeds the per-payment limit.
4. Uncheck recipient verification and request a small payment. The local rules should reject it.
5. Observe how approved simulated requests affect the local daily allowance. Use Reset to start over.

## Planned next steps

1. Add tests for spending-policy edge cases.
2. Build a server-side policy API and signed policy records.
3. Integrate Solana devnet wallet connectivity and a test-token settlement adapter.
4. Add explicit owner permissions, replay protection, and transaction review.
5. Conduct an independent security review before considering real funds.

## Responsible-use note

This is an experimental prototype, not a production payment system and not financial advice. Do not enter seed phrases, private keys, or financial credentials. Do not represent the demo as a real on-chain payment.

## Hackathon transparency

The current commit includes the browser simulation and documentation. Future capabilities should be described as implemented only after they are built and tested.
