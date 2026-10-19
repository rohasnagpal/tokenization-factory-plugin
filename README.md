# Tokenization Factory skills

AI skills for issuers who create tokens with [Sara Tokenization Factory](https://sarawallet.com/tokenize/). They run in your own AI assistant (Claude Code, Codex, or any agent that reads `SKILL.md` files). Sara never sees your conversation.

| Skill | What it does |
|---|---|
| **project-document** | Interviews you and produces one consolidated, print-ready HTML project document: asset, issuer, token, legal structure, economics, controls, risks and sources. **Start here** — the other skills draw their facts from it. |
| **launch-kit** | Launch posts, threads, LinkedIn post, press note, one-page summary and holder FAQ — after first checking whether promotion is legally permitted. |
| **listing-and-visibility** | Block explorer profile, wallet visibility, RWA data platforms such as rwa.xyz, marketplaces and trading options, matched to your token's transfer mode and legal position. |
| **holder-onboarding** | Eligibility checklist, safe wallet collection, approving wallets in Sara, holder messages and register reconciliation. |
| **holder-updates** | Periodic updates, distribution notices, material-event notices and annual summaries. |

## Install with one prompt

Paste this into your AI assistant:

```text
Install the skills from https://github.com/rohasnagpal/tokenization-factory-plugin into your skills folder, then run the project-document skill for my tokenized asset.
```

## Install manually

### Claude Code

```text
/plugin marketplace add rohasnagpal/tokenization-factory-plugin
/plugin install tokenization-factory@tokenization-factory-plugin
```

Skills appear as `/tokenization-factory:project-document`, `/tokenization-factory:launch-kit` and so on. Claude also picks the right skill automatically when you describe what you need.

### Codex CLI

```bash
git clone https://github.com/rohasnagpal/tokenization-factory-plugin.git
mkdir -p ~/.codex/skills
cp -R tokenization-factory-plugin/skills/* ~/.codex/skills/
```

Restart Codex if the skills don't appear.

### Other assistants

Each skill is a single file at `skills/<name>/SKILL.md`. Copy the folder into your assistant's skills directory, or paste the file's contents into the conversation.

## Suggested order

1. **project-document** — after you've configured or deployed your token.
2. **holder-onboarding** — before you send tokens to anyone.
3. **listing-and-visibility** and **launch-kit** — when you're ready to be seen.
4. **holder-updates** — on your reporting schedule and after any contract action.

## Important

These skills produce drafts and plans. They are not legal, tax or investment advice, an audit, a valuation, or an approval of any offering. A token does not by itself transfer legal ownership of an asset. Promoting or trading tokens that carry investment rights is regulated in most countries — have a qualified lawyer review anything you publish or any venue you use.

Never share your private key or seed phrase with an AI assistant, Sara or anyone else.

## License

MIT
