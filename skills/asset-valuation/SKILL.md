---
name: asset-valuation
description: Calculate and document an evidence-based indicative valuation range for an asset intended for or subject to tokenization, using issuer details, supporting documents and current market evidence. Use when a Sara Tokenization Factory issuer asks what an asset, tokenized interest or attributable amount per token may be worth. Do not use as a substitute for a required independent or certified valuation.
---

# Indicative asset valuation

Produce a transparent, reproducible estimate rather than a confident-looking guess. The result is an indicative analytical valuation as at a stated date, not an appraisal, fairness opinion, audit, investment recommendation or assurance report. Never describe it as independent, certified, verified or compliant with professional valuation standards unless a qualified valuer has actually provided that status.

## Define the subject before calculating

Establish, from the user and supplied evidence:

- the asset category, subcategory, precise identity, quantity and location;
- the interest being valued: the whole asset, a fractional interest, equity, debt, contractual revenue right or another legally defined interest;
- legal and beneficial ownership, material encumbrances and the percentage intended to be tokenized;
- valuation date, currency, purpose, intended audience and relevant jurisdiction;
- requested basis, such as market value, investment value, orderly-sale value, liquidation value or replacement cost; and
- condition, age, utilization, income, expenses, restrictions, remaining life and other category-specific value drivers.

Do not silently choose a basis that changes the meaning of the result. If the user has not specified one, use **indicative market value on an orderly-sale basis** as a clearly labelled analytical assumption only when that basis is coherent for the asset. Otherwise ask for the minimum clarification needed.

If the user provides a Sara token record URL (`https://sarawallet.com/tokenize/token/<contract>.json`) or contract address, fetch the record and use its project name and on-chain facts. Cite it as `[Sara token record, retrieved {retrieved_at}]`. The record does not establish the asset's identity, ownership, condition, value, legal rights or regulatory status.

## Evidence and input discipline

Separate every material input into:

1. user-supplied fact;
2. fact supported by a supplied document;
3. current external market evidence;
4. assumption;
5. calculation or analytical inference; or
6. unresolved item.

Never invent a comparable, transaction, quotation, yield, discount rate, growth rate, useful life, depreciation factor, exchange rate or source. For current prices, benchmarks, transactions and economic inputs, use current reliable sources where tools permit, record the access date and link the source. Prefer registries, exchanges, government data, audited reports and direct transaction records; identify the limitations of broker listings, asking prices, promotional material and thin or illiquid markets.

Photographs may support limited observations about visible characteristics or apparent condition. They do not establish identity, ownership, authenticity, hidden condition, location, date or value. Apply the asset-photograph privacy and evidentiary rules in the `project-document` skill when images are supplied.

Reconcile units, dates, currencies, quantities and ownership percentages before calculating. Use deterministic calculation tools when available. Show enough formulae and intermediate amounts for a reviewer to reproduce the result. Do not calculate from materially inconsistent inputs without identifying and resolving or bracketing the inconsistency.

## Choose methods that fit the asset

Use one or more methods supported by the evidence. Explain why each selected method fits and why any obvious alternative was excluded.

- **Market approach:** derive a value indication from genuine comparable transactions or observable prices, with explicit, evidence-based adjustments for time, location, condition, scale, rights and liquidity. Keep asking prices distinct from completed transactions.
- **Income approach:** calculate the present value of supportable future cash flows. Show revenue, costs, taxes if applicable, capital expenditure, working capital, forecast period, discount rate, terminal value and timing conventions. Do not infer a discount or capitalization rate without support.
- **Cost approach:** estimate current replacement or reproduction cost, then deduct physical deterioration and functional or economic obsolescence. Use only where cost is meaningfully related to value.
- **Quoted or unit-price approach:** apply a reliable quoted price, index or benchmark to verified quantity and grade, with explicit location, quality, custody, delivery and transaction-cost adjustments.
- **Net asset value:** value the underlying assets and liabilities consistently, including debt and senior claims, and apply any discount or premium only when supported.
- **Contractual-rights approach:** present-value the cash flows legally attributable to the specific revenue, royalty, receivable or debt right, reflecting term, priority, counterparty risk, dilution, default and enforceability.

For a company or operating business, distinguish enterprise value from equity value and reconcile cash, debt and other claims. For a portfolio, avoid double counting exposures shared across components.

## Result and uncertainty

Lead with a range. Provide a point estimate only when the evidence supports one, and identify how it was selected within the range. Do not manufacture narrow precision from sparse data.

Include:

- indications from each method and the reconciliation weighting or reasoning;
- a low, central and high case with the variables that drive each case;
- sensitivity to the two or three inputs with the greatest effect;
- evidence quality, market liquidity and confidence assessment;
- material limitations, omitted liabilities and open items; and
- the date after which the estimate should not be treated as current without refresh.

If the evidence cannot support a monetary range, do not invent one. Provide a **valuation not presently supportable** conclusion, identify the minimum missing inputs and, where useful, show a clearly labelled formula or scenario framework without presenting it as the asset's value.

## From asset value to an attributable per-token amount

Never equate the asset valuation with the token price. Calculate an attributable per-token indication only if the evidence establishes:

- the legal interest represented by the tokens;
- the percentage of that interest represented by the fully diluted token supply;
- debt, liens, senior claims, reserves and transaction costs that rank ahead of holders;
- issued, maximum, treasury, burned and unallocated token treatment; and
- any waterfall, fees, dilution, redemption limits or transfer restrictions.

Where supported, show the bridge explicitly:

`gross asset value - debt - senior claims - identified disposal costs + attributable cash = net attributable value`

`net attributable value × tokenized percentage ÷ relevant fully diluted token units = indicative attributable amount per token`

Label this as an allocation of the analytical asset value, not an observable token price, guaranteed redemption amount or forecast return. Do not apply a token liquidity premium, blockchain premium or fractionalization premium merely because tokens exist.

## Output

Return one self-contained, print-ready HTML5 file unless the user asks for another format. The report must include:

1. status, purpose, audience, valuation date and currency;
2. subject asset and interest valued;
3. basis of value and key assumptions;
4. input and evidence table with source IDs;
5. methods selected and excluded;
6. calculation schedules with formulas and units;
7. valuation range, reconciliation and confidence;
8. sensitivities and downside cases;
9. attributable per-token bridge, or a clear explanation why none is supportable;
10. limitations, unresolved items and required independent review; and
11. source register with links and access dates.

Use embedded CSS, semantic headings, a linked table of contents, A4 print rules and paged-media page numbers. Do not use remote fonts, scripts, images or stylesheets. If asset photographs are embedded, follow the inline Base64, privacy, caption and source-register rules in the `project-document` skill.

Do not append commentary outside the HTML. If critical information is missing before any meaningful calculation can be made, ask only for the minimum missing inputs instead of generating an empty report.

## Quality gate

Before returning a valuation:

- confirm the subject interest, basis, date, currency, jurisdiction and units;
- confirm that each material input is sourced or expressly labelled as an assumption;
- recalculate totals, percentages, present values and per-token arithmetic;
- confirm that market evidence is dated and no comparable or source was invented;
- confirm that the range reflects uncertainty and that method reconciliation is explained;
- confirm that asset value, equity or net value, attributable value and token price are not conflated;
- confirm that material encumbrances, senior claims and transaction costs are addressed or shown as unresolved; and
- confirm that the report does not claim professional certification, independence or assurance it does not have.
