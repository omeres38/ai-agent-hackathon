# Architecture and scope

## What the prototype demonstrates
AgentPay models a simple task lifecycle:
1. A task is available with a fixed reward and acceptance criteria.
2. The agent accepts the task; the demo marks its reward as escrowed.
3. A reviewable deliverable is created from a built-in template.
4. A human approves the deliverable.
5. The app records a simulated payout and moves the task to completed.

The entire demo runs client-side in one HTML file, with no build step and no external dependency.

## Deliberate limitations
- Task data and draft outputs are hard-coded demonstration data.
- No external LLM is called.
- No wallet is connected; balances and payouts are simulated.
- No escrow contract or on-chain transaction is deployed or sent.
- No production security, identity, or dispute-resolution layer is present.

## Suggested next engineering steps
1. Extract task state and deliverable generation into tested modules.
2. Connect a model provider through a server-side API that protects credentials.
3. Attach evidence URLs, timestamps, provenance, and reviewer feedback to every deliverable.
4. Integrate a testnet wallet and a reviewed escrow contract only after defining threat models and acceptance rules.
5. Add end-to-end tests for task acceptance, review, reset, and payout-state transitions.
