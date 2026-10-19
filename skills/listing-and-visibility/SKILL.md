---
name: listing-and-visibility
description: Build a realistic, step-by-step visibility and listing plan for a tokenized asset — block explorer verification and token profile, wallet visibility, RWA data platforms such as rwa.xyz, RWA marketplaces, DEX and exchange options — matched to the token's transfer mode and legal position. Use when a Sara Tokenization Factory issuer asks where to list the token, how to get it seen, or how to make it show up in wallets and explorers.
---

# Listing and visibility plan

Produce a prioritised plan that gets a Sara-created token seen and recorded in the right places, without recommending venues the token cannot technically use or the issuer is not legally permitted to use.

"Listing" means very different things. Separate them clearly:

| Kind | What it is | Typical requirement |
|---|---|---|
| **Record and metadata** | Block explorer token page, verified source, logo, website and socials | Proof that you control the contract or issuer wallet |
| **Wallet visibility** | Token showing correctly in holders' wallets | Correct metadata and an "add token" link; some wallets use token lists |
| **Data and analytics platforms** | Sites that track tokenized real-world assets and publish data about them, such as rwa.xyz | Platform's own submission or partnership process and data requirements |
| **Marketplaces and trading venues** | Places where the token can be bought or sold: RWA marketplaces, regulated tokenized-securities venues, DEXes, centralised exchanges | Legal permission, venue onboarding and due diligence, and transfer compatibility |

## Inputs

1. Sara token facts: name, symbol, decimals, blockchain and chain ID, contract address, transfer mode (Open, Restricted or Managed), enabled powers, issuer wallet, explorer link.
2. The project document from the `project-document` skill, especially holder rights, offering basis, eligible investors and jurisdictions. If it is missing, ask the user these questions directly and record the answers as unverified.
3. Goals: awareness, secondary trading, primary fundraising, investor reporting, or credibility with partners.

## Step 1 — Compatibility check

State the token's constraints before recommending anything:

- **Restricted or Managed transfer mode:** only approved wallets can hold or receive the token. A DEX liquidity pool, aggregator or exchange hot wallet is not an approved holder unless the issuer approves that specific address, and approving one effectively opens trading to anyone who can use that venue. **Do not recommend DEX pools for these tokens.** Venues must support allowlisted or permissioned transfers, or the issuer must deliberately approve the venue's addresses after legal advice.
- **Managed powers** (pause, freeze, forced transfer, recovery) must be disclosed to any venue or data platform, because they affect holder risk.
- **Open transfer mode:** technically tradable anywhere. Whether it *should* be listed depends on the legal analysis in Step 2.
- **Blockchain:** a venue or platform must support the token's network. Check, never assume, that a named venue supports it today.

## Step 2 — Legal gate for trading venues

Before recommending any marketplace, DEX or exchange:

1. Does the token represent economic or investment rights? Use the project document.
2. Is secondary trading permitted under the issuer's offering basis, in which countries, and to whom?
3. Does the venue need to be licensed for this kind of token where the holders are?

If any answer is unclear, recommend **record, wallet and data-platform steps only**, and list the trading questions for the issuer's lawyer. Never describe a trading venue as appropriate for a token whose legal status has not been confirmed.

## Step 3 — The plan

Present the plan in this order, skipping items that do not apply and explaining why.

### A. Record and metadata (do first)

1. **Confirm the contract on the block explorer.** Sara deploys from a controlled, reviewed build. Check whether the explorer shows verified source code for the address; if not, follow that explorer's source-verification process using the build information Sara provides.
2. **Complete the token profile.** Most explorers let the contract owner submit a logo, website, description and social links, usually after proving control of the deployer or owner wallet with a signed message. Prepare:
   - logo: square SVG or PNG, at least 256×256 px, transparent background;
   - one-sentence description taken from the project document and free of investment language;
   - official website and support contact.
3. **Publish the contract address on the issuer's own website** so holders can check they have the real token.

### B. Wallet visibility

1. Create an "add token to wallet" link or button using the wallet's standard asset-watch request with the address, symbol, decimals and logo.
2. Tell holders in the holder FAQ how to add the token manually: network, contract address, symbol and decimals.
3. Token lists used by wallets and DEX interfaces are relevant mainly to Open tokens. Do not pursue them for Restricted or Managed tokens unless a permissioned venue requires it.

### C. RWA data and analytics platforms

- **rwa.xyz** tracks tokenized real-world assets and publishes market data on them. Recommend it as a priority visibility target for most Sara projects. Tell the user to check rwa.xyz's current process for adding an asset or issuer, and prepare a submission pack:
  - issuer legal name, website and contact;
  - asset class and subcategory;
  - blockchain, contract address and explorer link;
  - token supply and decimals;
  - transfer mode and holder eligibility;
  - what the token represents, from the project document;
  - documentation link (public summary or project document if it is approved for distribution);
  - any reporting or valuation data the issuer can supply on a regular basis.
- Suggest other RWA-focused data, research and directory sites the user names or finds, and apply the same pack. Do not claim that any platform will list the token, or name its requirements, unless the user has checked them.
- Accuracy matters more than reach: data platforms are only useful if the issuer can keep supply, holder and valuation data current.

### D. Marketplaces and trading venues (only after Step 2 clears)

- **Regulated tokenized-securities venues and RWA marketplaces:** suit tokens with investment rights. Expect issuer due diligence, legal opinions, KYC on holders, and support for permissioned transfers. Prepare the project document, holder-onboarding process and transfer rules.
- **Private or bilateral transfers between approved holders:** often the realistic first secondary market for Restricted tokens. The issuer approves the buyer's wallet in Sara, then the transfer happens wallet to wallet.
- **DEX liquidity pool:** Open tokens only, and only where legal analysis permits public trading. Explain liquidity, price-manipulation and impermanent-loss risks, and that a thin pool sets a misleading "price".
- **Price-tracking sites and centralised exchanges:** typically require active trading and liquidity on tracked venues, plus their own review. Treat them as later-stage goals, not launch steps.

## Output format

Return:

1. **Token constraints** — transfer mode, network, powers and legal status in plain words.
2. **Plan table** — step, why it matters, what to prepare, who does it (issuer, lawyer, platform), and status (ready now, needs legal confirmation, later stage, not suitable).
3. **Submission pack** — the reusable facts block from section C, filled in from the inputs, with gaps marked "To confirm".
4. **Questions for the lawyer** — anything that blocks a trading venue.
5. **What not to do** — specific to this token, for example "Do not create a Uniswap pool: Restricted tokens cannot be held by the pool contract."

Never invent a venue's requirements, fees, supported networks or approval decisions. Never promise that a listing will happen.
