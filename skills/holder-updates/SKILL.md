---
name: holder-updates
description: Write accurate holder communications for a tokenized asset — periodic updates, distribution and payout notices, material-event notices and annual summaries — from on-chain data and issuer-supplied figures. Use when a Sara Tokenization Factory issuer needs to report to token holders, announce a distribution, explain a pause, freeze or other contract action, or prepare a yearly summary.
---

# Holder updates

Draft holder communications that are factual, consistent with the project document, and clear about what has and has not happened.

## Inputs

1. Sara token facts: name, symbol, blockchain, contract address, transfer mode and enabled powers.
2. The project document from the `project-document` skill: holder rights, distribution and redemption terms, reporting commitments and risk disclosures.
3. Period data supplied by the issuer, such as revenue, expenses, valuation, occupancy or production, and distributions, with sources.
4. On-chain data for the period: supply changes (mints and burns), holder count, contract actions (pause, freeze, forced transfer, recovery, approvals) with transaction hashes. Take these from Sara's manage dashboard or a block-explorer export.

Never invent a figure. If a number is missing, show "To confirm" and list it before drafting the final version.

## Update types

### 1. Periodic update (monthly or quarterly)

Sections:
- Period covered and date issued.
- Asset summary: operational facts for the period, from issuer data.
- Financial summary: income, costs and net figures as supplied, with the basis (audited, unaudited or management accounts).
- Token summary: total supply at the start and end of the period, changes and reasons, holder count, and contract actions with explorer links.
- Distributions: paid or declared, with the calculation shown (see type 2).
- Outlook: only statements the issuer approves, written as plans rather than promises.
- Risks and changes: anything that changes the risk picture in the project document.
- Contacts and where to find documents.

### 2. Distribution or payout notice

Show the calculation transparently:

- distributable amount and its source (for example net rent for a quarter);
- deductions and reserves, per the project document waterfall;
- record date and how holder balances were captured (block number or snapshot time);
- amount per token and the currency (for example USDC on a named network);
- payment date, method and how failed payments are handled.

Check that the calculation matches the distribution terms in the project document. If it does not, stop and flag the mismatch.

### 3. Material-event notice

For events such as:
- a pause, freeze, forced transfer or wallet recovery;
- a supply change;
- a change of custodian, manager or service provider;
- a valuation change beyond the issuer's threshold;
- a default, dispute, damage or loss, or a regulatory development.

State:
- what happened and when;
- which contract power was used, the transaction hash, and the disclosed purpose of that power;
- what it means for holders;
- what the issuer is doing next;
- when the next update will come.

Send it promptly and keep the tone plain. Do not minimise the event.

### 4. Annual summary

The year in one document: the asset's performance, distributions, supply and holder changes, all contract actions, valuation history, changes to parties or terms, and a link to updated documents. Deliver it as one self-contained HTML file with print CSS, page numbers and a table of contents, following the same HTML rules as the `project-document` skill.

## Rules

- No forecasts presented as facts. No "guaranteed", "risk-free" or return-projection language.
- Past distributions are not promises of future ones; say so when listing distribution history.
- Every on-chain claim links to the block explorer transaction or address.
- Every financial figure states its source and whether it is audited.
- Keep personal data out of updates: no holder names or wallet-to-person mappings.
- If the token is Restricted or Managed, remind holders that transfers require approval and how to request one.
- End every update with the issuer's contact and a reminder that the issuer and Sara will never ask for a private key or seed phrase.
