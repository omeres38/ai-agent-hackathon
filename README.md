# AI Agent for Market Intelligence

> Hackathon prototype — early-stage project

An AI-agent concept for collecting market information, organizing evidence, and helping a user investigate market-moving events. The initial focus is an explainable workflow: collect a report, identify affected assets, summarize evidence, and present a reviewable hypothesis rather than placing trades automatically.

## Problem

Market-moving information can be scattered across announcements, project accounts, news sources, and market data. A person may see the price move before discovering the event that caused it.

## Proposed workflow

1. **Collect** — gather links and data from sources that are actually connected/configured.
2. **Extract** — identify the asset, event type, event time, source, and relevant claims.
3. **Assess** — summarize potential impact and distinguish verified facts from hypotheses.
4. **Prioritize** — rank items by freshness, credibility, and potential relevance.
5. **Review** — show evidence and uncertainty to the user before they take action.

## Current implementation status

This repository was just initialized for the hackathon. The workflow above describes the intended prototype, not a claim that these integrations or an autonomous trading system are already implemented. Functionality will be documented as it is added.

## Principles

- **Evidence first:** retain source URLs and timestamps.
- **Freshness matters:** separate event time from the time a report was published or discovered.
- **Explainability:** show why an item was flagged.
- **Human in the loop:** no automatic trade execution in this initial prototype.
- **Risk awareness:** never present a hypothesis as a guaranteed prediction.

## Planned prototype milestones

- [ ] Define a simple event and source data model.
- [ ] Implement a small, reproducible sample workflow.
- [ ] Add tests for parsing and ranking.
- [ ] Document setup and limitations.
- [ ] Demonstrate the workflow with sample data.

## Disclaimer

This project is experimental and is not financial advice. Market events can be misinterpreted, sources can be wrong, and signals may not predict price movements.

## Hackathon note

This repository was initialized to organize the project. Keep the commit history and project description accurate about when code was written and which work was completed during the hackathon.
