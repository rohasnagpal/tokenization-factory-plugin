---
name: hi-sara
description: Entry point for Sara Tokenization Factory issuers. Use when the user says "Hi Sara", pastes a Sara token record URL (https://sarawallet.com/tokenize/token/<contract>.json), or asks what they can do next with a token they created on Sara. Loads the token's public record, summarises it, and routes to the right Tokenization Factory skill.
---

# Hi Sara

Greet the issuer, load their token's public record from Sara, and guide them to the next useful task.

## Step 1 — Load the token record

1. Find a Sara token record URL in the user's message. It looks like `https://sarawallet.com/tokenize/token/0x…json`. If the user gave the page URL without `.json`, add `.json`. If they gave only a contract address, build the URL from it.
2. Fetch the URL. The response is JSON with `schema: "sara.token-record/1"`.
3. If you cannot fetch URLs in this environment, ask the user to open the link and paste the JSON into the chat.
4. If there is no URL, ask for it: "Please paste your token's Sara link. You'll find it on your Sara manage page, under 'Build your documents and launch plan with AI'."
5. If the response is a 404 or has no `schema` field, say the token was not found on Sara and ask the user to check the link.

## Step 2 — Treat the record as the source of on-chain facts

The record is authoritative for these fields only: token name, symbol, decimals, supply, transfer mode, enabled powers, network, chain ID, contract address, issuer wallet, deployment transaction, block, date, explorer links and Sara's verification fields. Use them exactly as given. Never change them to fit a narrative.

The record does **not** establish legal ownership, asset value, regulatory status, investor eligibility or compliance; it says so in `notices`. The `asset.category` and `asset.subcategory` fields show what the issuer selected, which is a starting point, not a legal classification. The record includes the project name (`project.name`) as entered by the issuer. Other asset and project details are not in the record: ask for them when a skill needs them.

## Step 3 — Greet and summarise

Reply in a few lines:

> Hi! I've loaded **{project.name}**: token **{token.name} ({token.symbol})** on {deployment.network}.
> {initial_supply} tokens created (maximum {maximum_supply}) · {transfer_mode} transfers · issuer powers: {enabled_powers or "none"}.
> Asset type: {asset.category} → {asset.subcategory}. Verified by Sara on {deployment.deployed_at, date only}.

Then offer the menu below. Recommend **Project document** first if the user has not made one, because the other skills draw on it. Make clear that choosing it creates the complete first-draft legal-document pack immediately; missing issuer facts will be marked as open items and will not block creation.

| # | Task | Skill |
|---|---|---|
| 1 | Create the complete project legal-document pack now: legal structure, holder rights, risks, sources, schedules and TOC, as one print-ready file | `project-document` |
| 2 | Plan how to bring in holders and approve their wallets | `holder-onboarding` |
| 3 | Get the token seen: explorer profile, wallets, rwa.xyz, marketplaces | `listing-and-visibility` |
| 4 | Launch posts, press note and holder FAQ, within what the law allows | `launch-kit` |
| 5 | Updates, payout notices and event notices for holders | `holder-updates` |

## Step 4 — Hand off

When the user chooses, run that skill and pass it the record. Each skill must:

- prefill every on-chain fact from the record instead of asking for it;
- cite the record as a source, for example "[Sara token record, retrieved {retrieved_at}]", and link `deployment.explorer` entries for on-chain claims;
- use `asset.guide_url`, when present, as background reading on common structures for that asset type, not as advice about this project.

For `project-document`, use `project.name` as the project name and do not pause to ask for issuer details, intended readers or offering status. Run the skill immediately. It will place genuinely unknown matters in the relevant sections and completion schedule and can be revised when the issuer supplies them.

If the user returns later with only "Hi Sara", ask for the record URL again rather than relying on memory, because supply and holders can change.
