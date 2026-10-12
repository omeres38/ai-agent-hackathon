# AgenticPay demo video script (up to 3 minutes)

## Important accuracy note
This is a browser-only simulation. Do not describe it as a real wallet or a real Solana/USDC transaction. The demo does not use a live AI model or any external data.

## Recording plan
1. Open the live demo page and briefly show the AgenticPay header and the “SIMULATION” badge.
2. Show the policy fields: agent name, daily spending limit, per-payment limit, and recipient verification.
3. Leave the daily limit at 25 USDC, the per-payment limit at 10 USDC, the recipient verified, and the amount at 2 USDC.
4. Click “Evaluate payment request”. Point out that the request is approved by local demo rules and no transfer is sent.
5. Change the amount to 12 USDC and click “Evaluate payment request”. Explain that the request is rejected because it exceeds the 10 USDC per-payment limit.
6. Set the amount to 2 USDC, uncheck recipient verification, and run the request again. Explain that unverified recipients are rejected.
7. Point to the allowance and decision history. Mention that approved demo requests count toward simulated daily use.
8. End with the prototype limitation: wallet connectivity and Solana settlement are planned, not implemented.

## Suggested narration
“AgenticPay explores a programmable payment-control layer for AI agents. An owner sets a daily limit, a maximum payment amount, and whether the recipient is trusted. First, I request a 2 USDC payment to a verified service; the local demo policy approves it. Next, I try 12 USDC, above the 10 USDC per-payment limit, and it is rejected. Finally, I mark the recipient as unverified, and the request is rejected even though the amount is small. The dashboard tracks simulated usage and explains decisions. This is a browser prototype only: it does not connect a wallet or send real USDC or Solana transactions. The next development step is a tested policy API and Solana devnet integration.”
