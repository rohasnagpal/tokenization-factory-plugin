---
name: project-document
description: Interview a tokenization project owner and produce one consolidated, evidence-based, print-ready HTML project document covering the asset, issuer, token, legal structure, economics, controls, risks and source record. Use when someone has tokenized (or is about to tokenize) an asset with Sara Tokenization Factory and needs the project document, information memorandum or legal-review draft.
---

# Sara consolidated tokenization document

This is the foundation skill of the Tokenization Factory plugin. The launch-kit, listing-and-visibility, holder-onboarding and holder-updates skills draw their facts from the finished document, so produce it first.

Create one self-contained HTML file for a Sara Tokenization Factory project. The HTML is the only deliverable. It must be suitable for saving locally, opening in a modern browser, and printing to PDF on A4 or Letter paper with a table of contents and numbered pages.

Do not create a collection of documents. Do not create Markdown, PDF, Word, CSS, JavaScript, image, or data files alongside the HTML. Embed all styles in the HTML.

## Working rules

1. Treat data exported or copied from Sara as technical deployment facts only. Do not infer legal ownership, regulatory status, value, investor eligibility, enforceability, or compliance from payment, configuration, deployment, a wallet signature, or a blockchain record.
2. Separate:
   - facts supplied by the user;
   - facts supported by documents or authoritative sources;
   - assumptions;
   - analysis and recommendations;
   - unresolved information.
3. Never invent a party name, registration, title record, valuation, contract term, licence, approval, law, citation, quotation, date, address, wallet, transaction, or source.
4. Ask for the jurisdictions that matter: issuer, asset, offering, target investors, governing law, custody, operations, and token-holder location. If jurisdiction is unresolved, identify the gap and avoid a legal conclusion.
5. For current law or regulatory statements, use current primary sources where tools permit. Cite the exact provision, regulator publication, judgment paragraph, registry, or government source. State the access date. Do not treat AI output as authority.
6. Do not describe the asset, title, valuation, identity, compliance, or offering as “verified” unless the document identifies the evidence reviewed and the limits of that verification.
7. Do not silently complete missing answers. Use a visible “Open item” box in the relevant section. Material open items must also appear in the executive summary and completion schedule.
8. Avoid collecting unnecessary personal data. Mask identity numbers, bank details, private addresses, and confidential account information unless their full inclusion is required and the user expressly requests it.
9. The document is a project record and drafting aid. It must not claim to be legal advice, an offering approval, an audit, a valuation, or proof of title.

## Inputs

Accept any Sara project details supplied by the user, including:

- project name and ID;
- asset category and subcategory;
- token name, symbol, initial supply, maximum supply and decimals;
- transfer mode and enabled contract powers;
- issuer wallet;
- blockchain, chain ID, contract address and deployment transaction;
- build or manifest hashes and explorer links.

Validate internal consistency. Flag mismatched chains, wallet addresses, token supply figures, contract addresses, dates, or powers. Never modify a supplied on-chain fact merely to make the narrative consistent.

## Interview method

First inspect all supplied material. Produce a short private gap list, then interview the user in manageable groups. Do not ask again for facts already established. Ask follow-up questions when an answer is ambiguous, internally inconsistent, legally material, or unsupported.

Use this order:

1. Purpose, intended audience and document status.
2. Issuer, asset owner and other material parties.
3. Asset identity, ownership, location, custody and evidence.
4. Valuation and economics.
5. Token-to-asset legal relationship and holder rights.
6. Offering, investor, transfer, AML, sanctions and tax position.
7. Operations, governance, distributions, redemption and exit.
8. Asset-category module.
9. Risks, conflicts, defaults, disputes and contingency arrangements.
10. Source register, open items and approvals.

Before drafting, show the user a concise factual confirmation containing the material parties, asset, rights, supply, transfer controls, economics, jurisdictions, and unresolved matters. Correct the working record before producing the HTML.

## Core information to collect

### Purpose and status

- Intended use: internal planning, counterparty review, investor information, legal-review draft, board approval, or another stated purpose.
- Intended readers and permitted distribution.
- Document date, information cut-off date, version and confidentiality marking.
- Whether the token is already deployed; if so, capture network, address, transaction and deployment date.
- Whether any offering, sale, transfer, distribution or redemption has begun.

### Parties

- Issuer legal name, legal form, registration number, registered address and jurisdiction.
- Asset owner if different from issuer.
- Issuer relationship and authority concerning the asset.
- Directors, managers, trustees, general partners or authorized signatories relevant to the project.
- SPV, trust, nominee, custodian, servicer, manager, operator, registrar, paying agent and valuation provider.
- Related-party relationships, fees and conflicts.
- Evidence of identity, existence, authority and approvals, with source references.

### Asset

- Precise description, quantity, identifiers, location and legal situs.
- Legal and beneficial owner.
- Acquisition history and chain of title where material.
- Registration, title, certificates, serial numbers or registry references.
- Custody, possession, control and inspection arrangements.
- Liens, mortgages, pledges, licences, leases, claims, restrictions and other encumbrances.
- Insurance, condition, maintenance, storage and safeguarding.
- Permits, consents, licences and third-party approvals.
- Existing revenue, expenses, liabilities and contractual commitments.
- Percentage or interest intended to be tokenized.
- Evidence reviewed, evidence unavailable and verification limits.

### Valuation

- Valuation amount, currency and effective date.
- Valuer identity, independence, qualifications and engagement.
- Methodology, assumptions, comparables, discounts and sensitivity.
- Source document and date.
- Frequency and method of future valuation.
- Conflicts, uncertainty, volatility, illiquidity and stale-value risk.
- Clarify that a reference price, token price and asset valuation may differ.

### Legal and economic relationship

- Exactly what each token represents.
- Whether holders receive legal title, beneficial interest, shares, debt, contractual participation, revenue share, royalty, licence, redemption claim, governance rights, or no proprietary interest.
- The instrument, agreement, constitutional document, trust, security, assignment or register creating those rights.
- Priority relative to owners, lenders, creditors and other stakeholders.
- Recourse, security, guarantees and enforcement.
- Whether the blockchain register is legally operative, evidential, or mirrored by another register.
- Process for resolving discrepancies between on-chain balances and legal records.
- Rights on sale, refinancing, loss, destruction, default, insolvency, termination or project failure.

### Token and contract

- Token name, symbol, decimals, initial and maximum supply.
- Token-to-asset ratio and treatment of fractions, rounding and unallocated tokens.
- Initial recipient and allocation schedule.
- Transfer mode and whitelist rules.
- Minting, burning, pausing, freezing, forced transfer and recovery powers.
- Who controls each power, approval thresholds, permitted purposes and recordkeeping.
- Key compromise, succession, multisignature and emergency procedures.
- Upgradeability or immutability.
- Blockchain, chain ID, contract address, transaction hash, source/build status and explorer link.
- Smart-contract limitations, network dependency, gas and third-party infrastructure.

### Offering and holders

- Countries where tokens may be offered, sold or held.
- Investor type and eligibility criteria.
- Minimum age, KYC, AML, sanctions, source-of-funds and beneficial-owner processes.
- Securities, collective investment, crowdfunding, payments, commodities, property, consumer, marketing and licensing analysis for relevant jurisdictions.
- Exemptions or exclusions relied upon, with conditions and evidence.
- Selling restrictions, legends and prohibited persons.
- Subscription process, price, currency, refunds, cancellation, cooling-off and failed-close treatment.
- Transfer approval, lock-up, holding limits and resale process.
- Privacy roles, notices, processors, international transfers, retention and rights handling.
- Tax treatment and reporting as an open item unless supported by qualified advice.

### Economics and lifecycle

- Use of proceeds and budget.
- Fees, commissions, related-party payments and ongoing expenses.
- Revenue source and collection account.
- Distribution calculation, waterfall, deductions, reserves, frequency, record date, currency, payment method and treatment of failed payments.
- Voting, quorum, consent thresholds and reserved matters.
- Information, inspection and reporting rights.
- Redemption eligibility, price, notice, liquidity source, suspension and pro-rata treatment.
- Buyback terms and conflicts.
- Term, maturity, extension, early termination and exit.
- Asset sale, refinancing, winding-up and distribution of proceeds.
- Defaults, remedies, enforcement, replacement of service providers and business continuity.

## Asset-category modules

Apply the core questions plus the selected module. Tailor questions to the actual subcategory; do not reproduce irrelevant questions in the final document.

### Real Estate

Establish title and land-registry evidence; parcel and address; tenure; zoning and permitted use; occupancy; leases and tenant concentration; rent roll; deposits; arrears; property manager; operating expenses; taxes; insurance; condition survey; environmental matters; mortgages and easements; SPV structure; capex; development approvals; construction risk; valuation; sale process; and treatment of rent, refinancing and sale proceeds.

### Agriculture and Biological Assets

Establish land or facility rights; operator; crop, herd, stock or biological identifiers; quantity and stage; production cycle; yield assumptions; health and biosecurity; feed, water and inputs; permits; veterinary or agronomic records; disease and mortality; weather and climate exposure; insurance; storage; offtake contracts; commodity-price exposure; traceability; sustainability claims; harvest or sale schedule; and allocation of operating costs and losses.

### Equity and Business Interests

Establish entity and cap table; class and number of interests; constitutional and shareholder documents; voting, dividend, liquidation and information rights; pre-emption, drag, tag and first-refusal rights; board approvals; existing options and convertibles; dilution; restrictions; legal register reconciliation; financial statements; material contracts; litigation; valuation; corporate actions; distributions; and exit events.

### Debt

Establish borrower, lender and obligors; principal; currency; drawdown; interest or return; payment schedule; maturity; purpose; conditions precedent; security; guarantees; priority; covenants; events of default; grace periods; acceleration; enforcement; intercreditor arrangements; servicing; collections; arrears; credit assessment; concentration; expected losses; recovery assumptions; assignments; and withholding or tax provisions.

### Commodities

Establish type, grade, quantity, units and assay; title; origin; storage location; warehouse or custodian; receipts; inspection; inventory controls; segregation or commingling; liens; insurance; deterioration, shrinkage and contamination; transport; sanctions and responsible-sourcing issues; spot and benchmark price; hedging; roll or storage costs; delivery rights; sale process; and redemption mechanics.

### Energy and Natural Resources

Establish licence, concession, lease or mineral right; boundaries; reserves/resources classification; operator; ownership and working interests; royalties; permits; environmental and rehabilitation obligations; technical reports; production and decline assumptions; capex and opex; offtake; commodity exposure; hedging; transport; decommissioning; safety; community and indigenous rights; insurance; and allocation of production or sale proceeds.

### Carbon and Environmental Assets

Establish programme and methodology; project and registry IDs; vintage; unit status; validation and verification bodies; issuance and retirement; ownership; corresponding adjustments where relevant; additionality; permanence; leakage; reversal buffer; double counting; claims permitted; monitoring; host-country approvals; transfer restrictions; registry custody; invalidation risk; buyer use; and applicable environmental-marketing rules.

### Infrastructure and Projects

Establish project company; concession or project agreement; site and land rights; government counterparty; EPC and O&M arrangements; permits; completion status; budget; funding plan; construction milestones; delay and cost-overrun protection; availability or usage revenue; tariff; offtake; demand; performance deductions; force majeure; political risk; insurance; lenders and security; reserve accounts; lifecycle capex; handback; and termination compensation.

### Transport and Equipment

Establish manufacturer, model, serial/registration/IMO or tail number; title; location; condition; age and utilization; maintenance and technical records; operator and lessee; lease or charter; rent; deposits and reserves; permits and safety certification; insurance; liens; repossession; sanctions and export controls; downtime; depreciation; residual value; appraisal; parts or attachments; and sale or scrap process.

### Art

Establish artist or creator; title, date, medium, dimensions and edition; provenance; authenticity; catalogue raisonné or certificate; title; acquisition; location and custody; condition report; conservation; insurance; image and exhibition rights; copyright distinction; cultural-property, export and restitution issues; liens; appraisal; storage and transport; fractional-interest structure; display loans; and sale authority.

### Luxury Assets

Establish maker, model, serial/reference and unique features; provenance; title; authenticity; service or condition history; location and custody; insurance; appraisal; storage and use restrictions; import/export and duties; liens; fractional possession or usage; maintenance; counterfeiting risk; market comparables; dealer or auction arrangements; and sale or redemption.

### Collectibles

Establish item, set, edition, year and identifiers; provenance; authenticity and grading; population reports; title; condition; alterations; location and custody; insurance; appraisal; storage; image/IP rights; cultural-property restrictions; liens; market concentration; auction history; fractional ownership; and sale process.

### Sports and Entertainment

Establish the underlying contract or right; athlete, club, event, production or rights owner; term and territory; exclusivity; performance obligations; league, union, guild or federation rules; approvals; revenue source; recoupment and waterfall; production budget; completion risk; insurance; talent dependency; cancellation; media platform; accounting and audit rights; morality and injury risk; IP ownership; and termination.

### Intellectual Property

Establish work or invention; creator/inventor; chain of title; registrations and applications; territory; duration; assignments; licences; exclusivity; field of use; sublicensing; source materials; open-source or third-party components; infringement claims; maintenance fees; royalty base; collection statements; audit rights; takedowns; renewals; enforcement authority; and reversion or termination.

### Digital and Technology Assets

Establish asset definition and version; ownership and licences; source code, model weights, data or domain control; repositories and custody; third-party dependencies; open-source terms; training-data provenance; privacy and data rights; cybersecurity; access credentials; hosting and compute; availability; performance; maintenance; obsolescence; export controls; platform dependence; revenue model; usage metrics; transferability; and disaster recovery.

### Revenue and Royalty Rights

Establish the underlying contract and payer; assignability; consent; term; territory; revenue definition; gross-to-net deductions; reporting; audit; collection account; payment history; concentration; minimum guarantees; recoupment; reserves; disputes; set-off; termination; renewal; currency; taxes; servicing; forecast assumptions; default; and enforcement.

### Funds and Investment Interests

Establish fund, manager, general partner and domicile; legal form; governing documents; strategy; portfolio; term; commitment and drawdown; unit class; NAV; valuation policy; fees and carry; distributions; transfer restrictions; investor eligibility; side letters; gates; suspensions; key-person events; conflicts; leverage; service providers; audits; regulatory status; underlying liquidity; and winding up.

### Trade and Supply-Chain Assets

Establish invoice, purchase order, bill of lading, warehouse receipt or goods; seller, buyer, carrier, warehouse and obligors; authenticity; underlying trade; delivery and acceptance; title; assignment; negotiability; duplicate financing; dilution and disputes; payment terms; currency; sanctions; customs; inspection; insurance; liens; inventory controls; servicing; collection account; recourse; reserves; default and recovery.

### Other

Identify the asset’s legal nature and closest economic analogues. Build a tailored module covering identity, ownership, evidence, custody/control, valuation, revenue, expenses, licences, counterparties, transferability, enforcement, lifecycle, failure modes, regulation, tax and exit. Explain why existing modules were insufficient.

## Recognized Sara subcategories

Use the exact selected subcategory when supplied:

- **Real Estate:** Commercial; Residential; Land; Industrial; Hotels and Hospitality; Warehouses; Student Housing; Data Centres; REIT Interests; Co-Living; Development Projects; Healthcare Property; Leasehold Interests; Mixed-Use Property; Parking Assets; Property Debt; Senior Living.
- **Agriculture and Biological Assets:** Agricultural Produce and Inventory; Agricultural Projects and Farms; Aquaculture; Farm Equipment; Forestry and Timber; Livestock; Orchards and Vineyards; Standing Crops.
- **Equity and Business Interests:** Startup shares; Private company shares; Partnership Interests; LLP Interests; SPV Interests; Founder Equity; Employee Equity; Cooperative Interests; Joint-Venture Interests; Listed Shares; LLC Interests; Profit Interests.
- **Debt:** Loans; Bonds; Debentures; Notes; Private Credit; Mortgages; Revenue-Based Financing; Asset-Backed Debt; Consumer-Loan Portfolios; Convertible Debt; Distressed Debt; Mezzanine Debt.
- **Commodities:** Gold; Silver; Copper; Platinum; Palladium; Oil; Natural Gas; Uranium; Agricultural Commodities; Cocoa; Coffee; Commodity Baskets; Cotton; Grains; Livestock Commodities; Sugar.
- **Energy and Natural Resources:** Energy Storage; Exploration and Production Interests; Mineral Rights; Mining Interests; Natural Resource Royalties; Oil and Gas Interests; Renewable Energy Assets.
- **Carbon and Environmental Assets:** Carbon credits; Renewable Energy Certificates; Biodiversity Credits; Water Credits; Emissions Allowances; Nature-Based Credits; Plastic Credits; Renewable Energy Attributes; Water Rights.
- **Infrastructure and Projects:** Data Centre Projects; Logistics Infrastructure; Power and Utilities; Public-Private Partnership Interests; Renewable Energy Projects; Roads and Transport Infrastructure; Social Infrastructure; Telecommunications Infrastructure.
- **Transport and Equipment:** Aircraft; Commercial Vehicles; Construction Equipment; Equipment-Leasing Portfolios; Industrial Machinery; Railway Assets; Ships and Maritime Assets.
- **Art:** Paintings; Sculptures; Photography; Digital Art; Fine Art Collections; Antiquities; Installations; Manuscripts; Prints and Editions.
- **Luxury Assets:** Luxury Watches; Classic and Luxury Cars; Wine; Whisky and Spirits; Jewellery; Handbags and Fashion; Precious Stones and Diamonds; Private Aircraft; Yachts.
- **Collectibles:** Sports Memorabilia; Trading Cards; Rare Coins; Comics; Historical Artefacts; Stamps; Toys and Models.
- **Sports and Entertainment:** Athlete Revenue Rights; Entertainment Projects; Event Revenue; Film and Production Financing; Media Rights; Sports Club Interests; Ticketing and Membership Rights.
- **Intellectual Property:** Music; Software; Books; Films and Movies; Patents; Trademarks; Licensing Rights; Game and Digital IP Rights; Character and Franchise Rights; Copyrights; Datasets; Design Rights.
- **Digital and Technology Assets:** AI Models; Cloud and Compute Capacity; Data Assets; Digital Content; Digital Licences; Domain Names; Gaming Assets; Software Products.
- **Revenue and Royalty Rights:** Royalties; Revenue Share; Music Royalties; Film Royalties; Franchise Revenue; SaaS Revenue; Mining Royalties.
- **Funds and Investment Interests:** Private Equity Funds; Venture Capital Funds; Real Estate Funds; Hedge Funds; Debt Funds; SPV Interests; Fund Units; Commodity Funds; Feeder Funds; Infrastructure Funds; Private-Credit Funds; Tokenized Portfolio Interests.
- **Trade and Supply-Chain Assets:** Trade Receivables and Invoices; Bills of Lading; Export Receivables; Inventory Finance; Purchase Orders; Supply-Chain Finance; Warehouse Receipts.
- **Other:** Custom Asset.

## Analysis before drafting

Perform these checks and reflect the results in the document:

- Reconcile issuer, owner, wallet, asset, token and contract identities.
- Reconcile token supply, maximum supply, token-to-asset ratio and allocations.
- Identify whether stated holder rights are actually created by an identified legal instrument.
- Identify missing consents, registrations, approvals, assignments or perfection steps.
- Compare transfer restrictions in the legal terms with the smart-contract mode and powers.
- Compare distribution/redemption promises with actual revenue, liquidity and operational capacity.
- Identify related-party conflicts and discretionary powers.
- Test downside scenarios: no revenue, delayed sale, valuation decline, service-provider failure, asset loss, issuer insolvency, network outage, key compromise and regulatory restriction.
- Identify statements that require substantiation or qualification.
- Classify each material issue as resolved, open, assumption, recommendation or outside scope.

Do not use a generic “compliant” conclusion. State the reviewed question, jurisdiction, source, conditions and remaining uncertainty.

## Required document structure

The consolidated document must contain:

1. Cover page.
2. Document control and status.
3. Table of contents with internal links.
4. Executive summary.
5. Important notices, scope and limitations.
6. Parties and roles.
7. Asset description and evidence.
8. Ownership, custody and encumbrances.
9. Valuation and financial information.
10. Token structure and on-chain configuration.
11. Legal relationship and holder rights.
12. Offering, eligibility and transfer framework.
13. Economics, distributions and redemption.
14. Governance, administration and contract powers.
15. Operations, reporting and service providers.
16. Regulatory, AML, sanctions, privacy and tax considerations.
17. Risk factors.
18. Defaults, enforcement, termination and exit.
19. Representations, confirmations and required approvals.
20. Open items and completion conditions.
21. Source and evidence register.
22. Technical deployment schedule.
23. Definitions.

Omit a section only when it is clearly inapplicable, and say why in the executive summary. Use tables when they improve verification, especially for parties, token terms, sources, risks and open items.

## Source and evidence register

For each source record:

- source ID;
- title or description;
- issuer/author;
- date;
- version;
- page, clause, paragraph, registry entry or URL;
- date accessed for online sources;
- fact or proposition supported;
- status: reviewed, supplied-not-reviewed, unavailable, or to be obtained;
- confidentiality note where relevant.

Use source IDs in the body, such as “[S-03, clause 7.2]”. Hyperlink public sources. Do not fabricate source identifiers for material that does not exist.

## HTML output contract

Return one complete HTML5 document beginning with `<!doctype html>`. Return no commentary before or after it.

The file must:

- use UTF-8 and include a descriptive `<title>`;
- contain all CSS in one `<style>` block;
- use semantic headings in a logical hierarchy;
- give every table-of-contents destination a stable ID;
- use an ordered, clickable table of contents;
- include a visible version, document date and information cut-off date;
- use restrained professional typography and high-contrast colours;
- render cleanly on screen and in print;
- avoid remote fonts, scripts, images and stylesheets;
- repeat table headers when tables cross pages;
- prevent headings from being stranded at page bottoms;
- avoid splitting important cards, signature blocks and short tables;
- include page numbers in the printed footer;
- include the document title or short project name in the printed header;
- suppress interactive controls and raw URLs in print;
- make hyperlinks readable when printed;
- include a clear status marker such as “Draft for legal review” or the user-approved status.

Use print CSS equivalent to:

```css
@page {
  size: A4;
  margin: 20mm 18mm 22mm;
  @top-center {
    content: string(document-title);
    font: 9pt system-ui, sans-serif;
    color: #5a625d;
  }
  @bottom-center {
    content: "Page " counter(page) " of " counter(pages);
    font: 9pt system-ui, sans-serif;
    color: #5a625d;
  }
}
h1 { string-set: document-title content(); }
h1, h2, h3 { break-after: avoid; }
table, figure, .keep-together { break-inside: avoid; }
thead { display: table-header-group; }
tr { break-inside: avoid; }
@media print {
  nav a { color: inherit; text-decoration: none; }
  a[href^="http"]::after { content: " (" attr(href) ")"; font-size: 8pt; }
  .no-print { display: none !important; }
}
```

Include a small on-screen notice explaining that page numbering appears in print preview or PDF output. Do not use a fixed-position HTML footer to simulate pagination; use paged-media counters.

## Quality gate

Before returning the HTML:

- confirm that every user-supplied material fact is represented accurately;
- confirm that every legal proposition has appropriate jurisdiction and support or is expressly marked for legal review;
- confirm that no placeholder has been silently filled;
- confirm that all material open items appear in the open-items schedule;
- confirm that contract fields match the supplied Sara deployment facts;
- confirm that every TOC link resolves to a unique section ID;
- confirm that HTML tags are balanced and tables have headings;
- confirm that print CSS contains A4 sizing, page counters and page-break controls;
- confirm that the output is exactly one self-contained HTML file.
