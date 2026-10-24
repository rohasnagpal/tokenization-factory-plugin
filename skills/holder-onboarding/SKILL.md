---
name: holder-onboarding
description: Design and run the process for bringing holders into a tokenized asset — eligibility checklist, wallet collection, approving wallets for Restricted or Managed tokens in Sara, welcome messages and holder-register reconciliation. Use when a Sara Tokenization Factory issuer needs to onboard investors or holders, approve wallets, or keep the holder list in line with their legal register.
---

# Holder onboarding

Help an issuer bring holders onto a Sara-created token correctly: the right people, the right wallets, the right records, and clear communication. The issuer stays responsible for eligibility and compliance decisions; this skill organises the process and drafts the materials.

## Sara token record

If the user gives a Sara token record URL (`https://sarawallet.com/tokenize/token/<contract>.json`) or a contract address, fetch the record and prefill the project name (`project.name`) and every on-chain fact from it: token name, symbol, decimals, supply, transfer mode, enabled powers, network, chain ID, contract address, issuer wallet, deployment transaction, block, date and explorer links. Do not ask for these again. Cite it as "[Sara token record, retrieved {retrieved_at}]". The record contains technical facts only; it does not establish ownership, value, regulatory status or compliance. Apart from the project name, the asset description and the issuer's public profile (`issuer_profile`, written by the issuer and not verified by Sara), it does not contain the issuer's asset or project details. A `null` `token.maximum_supply` means no maximum, not missing data. Describe each enabled power using `token.enabled_powers_meaning`; a power not listed does not exist in the contract. If you cannot fetch URLs, ask the user to paste the JSON. The `hi-sara` skill describes the record in full.

## Inputs

1. Sara token facts: name, symbol, blockchain, contract address, transfer mode and enabled powers.
2. The project document from the `project-document` skill, especially: holder rights, eligible investor types, countries, KYC/AML and sanctions approach, lock-ups, holding limits and how the legal register relates to on-chain balances.
3. The issuer's existing materials: subscription agreement, investor questionnaire, KYC provider, cap table or register.

If eligibility rules are not set out in the project document, list them as open items and do not invent them.

## Step 1 — Onboarding design

Produce a one-page process covering:

1. **Eligibility** — who may hold, from the project document: investor type, countries, minimum age, excluded persons, holding limits.
2. **Checks** — what the issuer (or its provider) verifies before approval: identity, investor status, sanctions screening, source of funds where required, signed agreements. Name the responsible person or provider; mark gaps as open items.
3. **Wallet collection** — how the holder submits a wallet address safely:
   - ask for a public address only, never a seed phrase or private key (state this in every message);
   - confirm the network;
   - have the holder prove control of the wallet with a signed message or a small test transfer, where the issuer's process requires it;
   - warn against exchange deposit addresses: the holder may not control them, and they may be shared.
4. **Approval** — for Restricted and Managed tokens, the issuer approves each wallet in the Sara manage dashboard before tokens are sent. Record who approved, when and on what basis.
5. **Issuance or transfer** — how tokens reach the holder: transfer from the issuer wallet, or minting if enabled. Record the transaction hash.
6. **Record-keeping** — the holder register entry (see Step 3).
7. **Changes** — how a holder changes wallet, transfers to another approved person, or is removed. Explain the role of freeze, forced-transfer and recovery powers only if they are enabled, and their disclosed purposes.

## Step 2 — Materials

Draft, ready to send:

- **Invitation email** — what the holder is being invited to, what they need to provide, the process timeline, and the no-seed-phrase warning.
- **Wallet submission form fields** — legal name, email, wallet address, network, wallet type (self-custody or custodian), confirmation of control, and acknowledgements set by the issuer.
- **Approval confirmation** — sent when the wallet is approved, with the contract address, network, symbol and decimals, and instructions to add the token to the wallet.
- **Tokens-sent notice** — amount, transaction hash with explorer link, and where to see holdings.
- **Rejection or more-information-needed message** — neutral and without speculating about the reason beyond what the issuer authorises.

Every message must say Sara and the issuer will never ask for a private key or seed phrase.

## Step 3 — Holder register reconciliation

Provide a register template (CSV columns or a table) with:

holder ID, legal name, wallet address, network, eligibility basis, checks completed and date, approval date and approver, tokens allocated, transaction hash, lock-up end date, notes.

Then, when the user supplies the register and the on-chain balances (from Sara's holder view or a block-explorer export), reconcile them:

- wallets on-chain but not in the register;
- register entries with no on-chain balance;
- balance mismatches;
- approved wallets holding nothing;
- holdings above any limit in the project document.

Report each discrepancy with a suggested action. Never treat the on-chain balance as automatically correct or the register as automatically correct; the project document says which record governs.

## Rules

- Do not decide whether a person is eligible; apply the issuer's stated rules and flag cases that need the issuer's judgement.
- Collect only the personal data the process needs. Do not put identity numbers or documents into chat outputs; refer to them by reference.
- Keep the holder register private. Do not publish it, and do not include personal data in public posts.
