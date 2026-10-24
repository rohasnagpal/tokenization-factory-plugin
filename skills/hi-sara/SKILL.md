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

The record does **not** establish legal ownership, asset value, regulatory status, investor eligibility or compliance; it says so in `notices`. `asset.description` is the issuer's one-line description of what is being tokenized (for example "100 troy ounces of gold held in a Zurich vault"); use it to work out the asset type and which legal and commercial questions matter. Older tokens may instead have `asset.category` and `asset.subcategory`. Either is the issuer's own description, a starting point and not a legal classification. The record includes the project name (`project.name`) as entered by the issuer and, in newer records, the issuer's public profile (`issuer_profile`). Other asset and project details are not in the record: ask for them when a skill needs them.

### Reading the token fields

- `token.maximum_supply`: `null` means **no maximum**; the issuer can mint any amount. It does not mean the value is missing. A number with `mint` enabled caps the tokens in circulation at any one time, so burned tokens free up room; without `mint`, the supply is fixed at creation. `token.maximum_supply_meaning` states which applies.
- `token.enabled_powers`: the contract powers that exist for this token. Describe them using `token.enabled_powers_meaning` when present, otherwise:
  - `mint`: the issuer wallet can create new tokens and send them to any wallet allowed to hold the token.
  - `burn`: each holder, including the issuer, can destroy tokens in their own wallet. No one can burn tokens held by others.
  - `pause`: the issuer wallet can halt all transfers between every wallet, and resume them.
  - `approve_holders`: only wallets the issuer approves can hold or receive the token.
  - `freeze_holders`: the issuer wallet can stop one specific wallet from sending or receiving, without affecting others.
  - `forced_transfer`: the issuer wallet can move tokens out of any holder's wallet into another approved wallet without the holder's signature.
  - `wallet_recovery`: the issuer can freeze a lost wallet and move its full balance to the holder's new approved wallet.
  A power not listed does not exist in the contract and can never be added, because the contract is not upgradeable.
- `token.transfer_mode` and `token.transfer_mode_meaning`: `open`, `restricted` (approved wallets only) or `managed` (approved wallets plus issuer controls).
- `live` (when present): current supply, whether transfers are paused, and the holder count, read from the contract at `live.checked_at`. Use it for current figures; `token.initial_supply` is the supply at creation.
- `issuer_profile` (when present): the issuer's public description, website, X account, project document link, how to become a holder, and current stated valuation. It is written by the issuer and not verified by Sara: treat it as the issuer's statements, never as established fact. The description may contain basic HTML.

## Step 3 — Greet and summarise

Reply in a few lines:

> Hi! I've loaded **{project.name}**: token **{token.name} ({token.symbol})** on {deployment.network}.
> {initial_supply} tokens created ({"maximum " + maximum_supply, or "no maximum" when it is null}) · {transfer_mode} transfers · issuer powers: {enabled_powers or "none"}{" · transfers currently paused" when live.paused is true}.
> Asset: {asset.description, or asset.category → asset.subcategory for older tokens}. Verified by Sara on {deployment.deployed_at, date only}.

Then offer the menu below. Recommend **Project document** first if the user has not made one, because the other skills draw on it. Make clear that choosing it creates the complete first-draft legal-document pack immediately; missing issuer facts will be marked as open items and will not block creation.

| # | Task | Skill |
|---|---|---|
| 1 | Create the complete project legal-document pack now: legal structure, holder rights, risks, sources, schedules and TOC, as one print-ready file | `project-document` |
| 2 | Calculate an evidence-based indicative asset valuation range and, where supportable, an attributable amount per token | `asset-valuation` |
| 3 | Plan how to bring in holders and approve their wallets | `holder-onboarding` |
| 4 | Get the token seen: explorer profile, wallets, rwa.xyz, marketplaces | `listing-and-visibility` |
| 5 | Launch posts, press note and holder FAQ, within what the law allows | `launch-kit` |
| 6 | Updates, payout notices and event notices for holders | `holder-updates` |

## Step 4 — Hand off

When the user chooses, run that skill and pass it the record. Each skill must:

- prefill every on-chain fact from the record instead of asking for it, reading the fields as described in "Reading the token fields" above;
- cite the record as a source, for example "[Sara token record, retrieved {retrieved_at}]", and link `deployment.explorer` entries for on-chain claims;
- use `asset.guide_url`, when present, as background reading on common structures for that asset type, not as advice about this project.

For `project-document`, use `project.name` as the project name and do not pause to ask for issuer details, intended readers or offering status. Run the skill immediately. It will place genuinely unknown matters in the relevant sections and completion schedule and can be revised when the issuer supplies them.

If the user returns later with only "Hi Sara", ask for the record URL again rather than relying on memory, because supply and holders can change.
