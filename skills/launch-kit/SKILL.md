---
name: launch-kit
description: Create launch communications for a tokenized asset — tweets and threads, LinkedIn post, press note, one-page summary and holder FAQ — after first establishing whether promotion is legally permitted. Use when a Sara Tokenization Factory issuer wants marketing copy, social posts, announcement text or launch ideas for their token.
---

# Tokenized asset launch kit

Produce launch communications for a token created with Sara Tokenization Factory. Communications must be accurate, consistent with the project document, and limited to what the issuer is legally permitted to say in the places it will be seen.

A public post about a token that represents ownership, profit, revenue, debt or other economic rights can be an offer or promotion of a regulated investment. Publishing it can break the conditions of an exemption the issuer depends on (for example, a ban on general solicitation) or breach financial-promotion rules. The gate below exists to stop that. Never skip it to be helpful.

## Sara token record

If the user gives a Sara token record URL (`https://sarawallet.com/tokenize/token/<contract>.json`) or a contract address, fetch the record and prefill every on-chain fact from it: token name, symbol, decimals, supply, transfer mode, enabled powers, network, chain ID, contract address, issuer wallet, deployment transaction, block, date and explorer links. Do not ask for these again. Cite it as "[Sara token record, retrieved {retrieved_at}]". The record contains technical facts only; it does not establish ownership, value, regulatory status or compliance, and it does not contain the issuer's project name or asset details. If you cannot fetch URLs, ask the user to paste the JSON. The `hi-sara` skill describes the record in full.

## Inputs

1. **The project document** produced by the `project-document` skill. Ask for it first. If it does not exist, offer to run that skill, or proceed only with facts the user states directly and mark every claim as unverified.
2. Token facts from Sara: name, symbol, blockchain, contract address, transfer mode (Open, Restricted or Managed) and explorer link.
3. Brand inputs: issuer name, website, social handles, tone of voice, any approved wording or disclaimers from the issuer's lawyer.

Never invent a fact, figure, partner, audit, listing, valuation, yield, user count or quotation. Every factual statement in the output must trace to the project document, Sara token facts, or something the user stated in this conversation.

## Step 1 — Promotion gate (always first)

Ask, and do not draft until answered:

1. **What does the token give holders?** Use the project document's holder-rights section. Classify as: (a) economic or investment rights — ownership share, profit, revenue, interest, royalty, redemption, NAV; (b) utility, access, membership or record-keeping only; (c) unclear.
2. **Is any offer or sale happening or planned?** Including private placements, presales, allocations to investors, or future sales.
3. **Under which regime?** The exemption, licence, prospectus or other basis the issuer's lawyer has confirmed, and the countries covered.
4. **Who may receive promotion?** Public, professional/accredited investors only, existing holders only, or named contacts only.
5. **Has a lawyer approved promotional content?** If yes, ask for the approved disclaimer and any restrictions.

Then choose a mode and state it at the top of the output:

| Mode | When | What you may write |
|---|---|---|
| **Awareness only** | Rights are (a) or (c) and there is no confirmed basis for public promotion; or the answers are unclear | That the asset exists and has been tokenized, the technology used, the issuer's story and the asset's non-financial qualities. **No** price, valuation, returns, yield, "investment", "opportunity", "buy", "invest", "early access", "limited supply", allocation size, how to participate, or links to subscription pages. |
| **Restricted audience** | Lawyer-confirmed basis allows promotion only to a defined audience | Full factual content, delivered only through private channels to that audience: one-page summary, email, direct message. Public social posts stay in Awareness mode. |
| **Public promotion** | Lawyer-confirmed basis expressly permits public promotion in the named countries | Factual offering communications using only the approved disclaimer and restrictions, plus the required risk wording. |
| **Utility / record** | Rights are (b), and the user confirms no investment features | Product-style launch content. Still no return, price-appreciation or resale-profit language. |

If the user pushes for a less restrictive mode without a confirmed legal basis, explain the risk once, keep the safer mode, and list the question for their lawyer.

## Step 2 — Content rules (all modes)

- No promises or projections of returns, yield, APY, price appreciation, "passive income", "guaranteed", "risk-free", "safe", or "to the moon"-style hype.
- Do not say "audited" unless an independent audit exists and is named. Sara's automated security review is not a professional audit; describe it, if at all, as an automated security review.
- Do not say "listed", "trading", "liquid" or "available on [venue]" unless that is true today and the user has confirmed it.
- Do not call the token "compliant", "regulated" or "approved" without the specific approval, regulator and jurisdiction.
- Do not imply that a token transfers legal title unless the project document confirms the legal instrument that makes it so.
- For Restricted and Managed tokens, say clearly that transfers are limited to approved wallets.
- Name the blockchain and include the contract address only from Sara facts, and only in full or clearly truncated form (`0x1234…abcd`) with a full-address link to the block explorer.
- Add the lawyer-approved legend or disclaimer required for the relevant mode, audience and jurisdiction. A generic disclaimer does not determine whether content is legally an offer, solicitation or financial promotion. If no wording has been approved, the following may be used only for **Awareness-only** content: "For general information only. This is not an offer to sell or a solicitation to buy any security or investment. Tokens may be subject to transfer restrictions and are not available in all jurisdictions." Do not release Restricted-audience or Public-promotion content until the required wording is confirmed.
- Respect platform norms: X/Twitter posts at most 280 characters each; threads 4–7 posts; LinkedIn 120–250 words; no more than two hashtags per post.

## Step 3 — Deliverables

Ask which pieces the user wants. Default set:

1. **Launch post** — 3 variants of a single post for X/Twitter.
2. **Launch thread** — 5–7 posts: what the asset is, why it was tokenized, how the token works (blockchain, transfer mode), what holders can see, where to learn more, disclaimer.
3. **LinkedIn post** — one professional announcement.
4. **Press note** — 300–450 words: headline, dateline placeholder `[CITY, DATE]`, summary paragraph, issuer quote **only if the user supplies or approves it**, background, about-the-issuer boilerplate, media contact placeholder.
5. **One-page summary** — for Restricted-audience mode only, delivered as a self-contained HTML file with print CSS, suitable for sending privately.
6. **Holder FAQ** — 8–12 questions: what the token represents (from the project document), how to receive it, approved-wallet rules, how to view holdings, what happens if a wallet is lost (only if recovery is enabled), where updates are published, who to contact.
7. **Launch-week plan** — a short day-by-day posting and outreach schedule using only the deliverables above.

## Step 4 — Ideas, not just copy

When asked for marketing ideas, give options that do not depend on financial promotion:

- Behind-the-scenes content about the asset (provenance, craftsmanship, site visits, the team).
- An explainer on how tokenization works for this asset class.
- Showing the on-chain record: block explorer screenshot of the contract and holder count (when holder count is not sensitive).
- Partner and community announcements the user confirms.
- Educational posts on transfer restrictions and why they protect holders.
- Thought-leadership posts by the issuer on their industry.

Mark any idea that would move into investment promotion, and say which mode it needs.

## Output format

Return:

1. **Mode and reasons** — one short paragraph.
2. **Open questions for the lawyer** — if any.
3. **Deliverables** — each under its own heading, ready to copy, with the disclaimer attached.
4. **Fact trace** — a table listing each factual claim used and its source (project-document section, Sara token facts, or user statement).

Keep the language plain and specific. Prefer concrete facts about the asset over adjectives.
