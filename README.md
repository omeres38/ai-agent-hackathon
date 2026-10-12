# AgentPay — AI work, accountable outcomes

> Hackathon prototype · v0.1 · Early-stage

AgentPay explores a crypto-native workflow where an AI worker accepts a bounded task, creates a reviewable deliverable, and receives a payout after human approval.

**Live code:** [Open the repository](https://github.com/omeres38/ai-agent-hackathon)  
**Run the demo:** open `index.html` in any modern browser. No install or build step is required.

## The problem

Companies and online communities increasingly delegate digital work to AI agents, but it is difficult to make that work accountable: the task scope, acceptance criteria, work product, review decision, and payment status can be scattered across tools.

## The idea

Treat an AI agent like a digital worker with a clear job description and a transparent workflow:
1. A task is listed with a fixed reward and acceptance criteria.
2. The agent accepts the work.
3. It produces a deliverable that a human can inspect.
4. A reviewer approves or rejects the result.
5. A payout is recorded against the task, with the potential for later on-chain settlement.

## What is implemented now

The browser prototype demonstrates the task lifecycle using sample data:
- Three example tasks in research, community, and operations.
- Accepting a task and marking its reward as demo escrow.
- Generating a templated deliverable for review.
- Human approval and a simulated payout.
- Task filters, progress counters, activity history, and reset.

## What is not implemented yet

- No live LLM or external data source is called.
- No wallet is connected.
- No real USDC is held, sent, or received.
- No smart contract, escrow, or on-chain payment is deployed.
- Demo tasks and deliverables are local, built-in examples.

All balances and payment actions are simulated. The prototype does **not** make or recommend trades.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Accept a task, review its generated sample deliverable, then approve the simulated payout.

No API keys or environment variables are needed.

## Next steps

- Add a real agent runtime behind a server-side API, keeping credentials off the client.
- Store tasks, deliverables, source evidence, and review decisions in a database.
- Add test coverage for task-state transitions and review outcomes.
- Investigate testnet wallet and escrow integration with appropriate security review.
- Add reputation, dispute handling, and auditable provenance before any real funds are involved.

## Responsible-use note

This is an experimental hackathon prototype, not financial advice or a production payment system. Generated work must be reviewed. The current demo has no blockchain integration and must not be represented as making real on-chain payments.

## Hackathon transparency

The repository and prototype are being built for the hackathon. The current commit history records the work actually added; future integrations should only be described as complete after they are implemented and tested.
