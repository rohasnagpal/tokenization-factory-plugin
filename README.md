# Tokenization Factory

Turn a tokenized asset into the documents and operating materials needed to launch and manage it. Tokenization Factory helps you create a comprehensive project document, legally gated launch communications, a listing and visibility plan, a holder-onboarding process, and periodic holder updates—all grounded in your project facts and source materials.

It is designed for issuers creating tokens with [Sara Tokenization Factory](https://sarawallet.com/tokenize/).

## Quick start

On your Sara manage page, copy the prompt under **Build your documents and launch plan with AI** and paste it into ChatGPT, Claude or Codex. It looks like this:

```text
Install the Tokenization Factory plugin from https://github.com/rohasnagpal/tokenization-factory-plugin if not already done. Then run "Hi Sara" for the tokenization project https://sarawallet.com/tokenize/token/<contract-address>.json.
```

The link is your token's public Sara record. The skills read your token's on-chain facts from it, so you don't have to type them.

| Skill | What it does |
|---|---|
| **hi-sara** | Say "Hi Sara" with your token link. Loads your token's record, summarises it and points you to the right skill. |
| **project-document** | Immediately produces one consolidated, print-ready HTML legal-document pack with a linked TOC: asset, issuer, token, legal structure, holder rights, economics, controls, risks, sources and completion schedules. Missing facts are shown as open items and can be supplied for later revisions. **Start here** — the other skills draw their facts from it. |
| **launch-kit** | Launch posts, threads, LinkedIn post, press note, one-page summary and holder FAQ — after first checking whether promotion is legally permitted. |
| **listing-and-visibility** | Block explorer profile, wallet visibility, RWA data platforms such as rwa.xyz, marketplaces and trading options, matched to your token's transfer mode and legal position. |
| **holder-onboarding** | Eligibility checklist, safe wallet collection, approving wallets in Sara, holder messages and register reconciliation. |
| **holder-updates** | Periodic updates, distribution notices, material-event notices and annual summaries. |

## Install

### ChatGPT

After the plugin is published, open **Plugins** in ChatGPT, search for **Tokenization Factory**, and select **Install**. ChatGPT does not reliably install an arbitrary GitHub plugin from a normal chat prompt.

### Codex or Claude Code — one prompt

Paste this into a local Codex or Claude Code session:

```text
Install the Tokenization Factory plugin from https://github.com/rohasnagpal/tokenization-factory-plugin using this assistant's native plugin marketplace. If native plugin installation is unavailable, install the five folders under skills/ in my user-level skills directory. Ask before writing outside the current repository. Verify that all five skills are discoverable, tell me whether I need to restart or open a new chat, and do not run a skill yet.
```

Installation may still require approval for network access or writing to the assistant's configuration directory. Start a new chat after installation.

<details>
<summary>Native command fallback</summary>

#### Codex

```bash
codex plugin marketplace add rohasnagpal/tokenization-factory-plugin
codex plugin add tokenization-factory@tokenization-factory-plugin
```

#### Claude Code

```text
/plugin marketplace add rohasnagpal/tokenization-factory-plugin
/plugin install tokenization-factory@tokenization-factory-plugin
```

</details>

### Other assistants

Copy the folders under `skills/` into the assistant's user-level skills directory. This loads the workflows without plugin listing metadata.

## Start

Open a new chat and say:

```text
Run the project-document skill for my tokenized asset.
```

## Suggested order

1. **project-document** — after you've configured or deployed your token.
2. **holder-onboarding** — before you send tokens to anyone.
3. **listing-and-visibility** and **launch-kit** — when you're ready to be seen.
4. **holder-updates** — on your reporting schedule and after any contract action.

## Important

These skills produce drafts and plans. They are not legal, tax or investment advice, an audit, a valuation, or approval of an offering. A token does not by itself transfer legal ownership of an asset. Promotion, offering and trading may be regulated depending on the token's rights and the relevant jurisdictions. Have qualified counsel review public communications, offering activity and trading arrangements.

Never share your private key or seed phrase with an AI assistant, Sara or anyone else.

## Data and permissions

This is a skills-only plugin. It contains instructions and image assets, with no MCP server, account connection, executable code, lifecycle hooks or telemetry. The plugin does not send conversations to Sara. Conversations remain subject to the terms and data practices of the AI assistant you use.

## License

MIT
