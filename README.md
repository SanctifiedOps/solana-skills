# Solana Skills

**A comprehensive set of agent skills that turns an AI into a practical Solana project operator: dev, token, launch, trading, frontend, infra, automation, trust.**

Built for the trenches. Written by people who ship, not people who pontificate.

---

## Who This Is For

- **Solana devs** building programs, tokens, and dApps
- **Memecoin operators** launching and managing tokens
- **Traders and trenchers** analyzing launches, tracking whales, avoiding rugs
- **Frontend engineers** shipping wallet UX and transaction flows
- **Bot builders** automating monitoring, alerts, and trading
- **Community leads** running comms, marketing, and trust ops

---

> **CTA: Early Access**
> Visit [This Will Do Millions](https://thiswilldomillions.com/) to get notification and early access to our future projects and releases.

> **CTA: Tip Jar**
> If you found this useful, please consider tipping my son's Solana wallet: `A23U9FWCF6tdQ95nuvXaNMN3FYPegCntN4T715svL3HF`.

## Quick Install

```bash
# Install all skills (local clone)
codex skills install ./skills/

# Install from GitHub (once published)
codex skills install git+https://github.com/SanctifiedOps/solana-skills

# Install a single skill
codex skills install ./skills/core-dev/solana-account-model

# Update skills
codex skills install ./skills/  # Re-run to refresh
```

---

## Start Here (Top 5)

| Skill | What It Does |
|-------|--------------|
| [solana-account-model](skills/core-dev/solana-account-model/) | Accounts, owners, signers, PDAs, rent, CPIs - the mental model you need |
| [spl-token-create-and-configure](skills/tokens/spl-token-create-and-configure/) | Create mints, set authorities, revoke, publish txids |
| [launch-readiness-checklist](skills/launch/launch-readiness-checklist/) | Go/no-go gate with infra, LP, comms, rollback planning |
| [token-analysis-checklist](skills/trading/token-analysis-checklist/) | Buyer's rug detection - LP analysis, authority checks, red flags |
| [rpc-selection-and-resilience](skills/infra/rpc-selection-and-resilience/) | Choose providers, timeouts, fallbacks, cost control |

---

## All Pillars

### core-dev/
Program and account model, Anchor, validation, security, upgrades.

| Skill | Description |
|-------|-------------|
| [solana-account-model](skills/core-dev/solana-account-model/) | Accounts, owners, signers, rent, PDAs, CPI mental model |
| [anchor-project-scaffold](skills/core-dev/anchor-project-scaffold/) | Project setup, program/client layout, env config, dev workflow |
| [instruction-design-and-validation](skills/core-dev/instruction-design-and-validation/) | Inputs, constraints, invariants, authority checks |
| [pda-design-playbook](skills/core-dev/pda-design-playbook/) | Seed strategy, collisions, upgrade considerations |
| [common-anchor-errors-debugger](skills/core-dev/common-anchor-errors-debugger/) | Account discriminator mismatch, constraint failures, etc. |
| [program-security-basics](skills/core-dev/program-security-basics/) | Authority checks, unsafe patterns, attack surfaces |
| [upgrade-vs-immutable-decision](skills/core-dev/upgrade-vs-immutable-decision/) | Tradeoffs, trust, governance, operations |
| [compressed-nfts-basics](skills/core-dev/compressed-nfts-basics/) | Merkle trees, concurrent trees, cNFT minting and transfers |

### tokens/
SPL lifecycle, authorities, distribution, tokenomics, post-launch ops.

| Skill | Description |
|-------|-------------|
| [spl-token-create-and-configure](skills/tokens/spl-token-create-and-configure/) | Mint creation, authorities, decimals, revoke flows |
| [token-authority-and-risk](skills/tokens/token-authority-and-risk/) | Mint/freeze authority implications, best practices |
| [token-distribution-planning](skills/tokens/token-distribution-planning/) | Wallet splits, allocations, vesting, transparency |
| [tokenomics-design-for-memecoins](skills/tokens/tokenomics-design-for-memecoins/) | Supply narrative, burns, sinks, incentives |
| [post-launch-token-ops](skills/tokens/post-launch-token-ops/) | Treasury policy, unlock communications, LP considerations |
| [token-2022-extensions](skills/tokens/token-2022-extensions/) | Transfer fees, permanent delegate, metadata pointer, confidential transfers |

### trading/
Token analysis, whale tracking, DEX integration, launch dynamics.

| Skill | Description |
|-------|-------------|
| [pump-fun-mechanics](skills/trading/pump-fun-mechanics/) | Bonding curves, graduation, migration, sniping dynamics |
| [jupiter-swap-integration](skills/trading/jupiter-swap-integration/) | Swap APIs, route optimization, slippage, frontend integration |
| [token-analysis-checklist](skills/trading/token-analysis-checklist/) | Rug detection, LP analysis, authority checks, red flags |
| [whale-wallet-analysis](skills/trading/whale-wallet-analysis/) | Smart money tracking, wallet clustering, signal vs noise |

### launch/
Fair launch patterns, liquidity, snipers, stabilization.

| Skill | Description |
|-------|-------------|
| [launch-readiness-checklist](skills/launch/launch-readiness-checklist/) | Pre-flight checklist: infra, wallets, LP, comms, rollback |
| [fair-launch-patterns](skills/launch/fair-launch-patterns/) | What "fair" means operationally, tradeoffs, dynamics |
| [liquidity-and-price-dynamics-explainer](skills/launch/liquidity-and-price-dynamics-explainer/) | LP basics, slippage, volatility mechanics |
| [sniper-dynamics-and-mitigation](skills/launch/sniper-dynamics-and-mitigation/) | Threat model, defensive posture |
| [post-launch-stabilisation-playbook](skills/launch/post-launch-stabilisation-playbook/) | What to monitor, comms, product milestones |

### frontend/
Wallet connect, signing UX, on-chain reads, security.

| Skill | Description |
|-------|-------------|
| [wallet-connection-ux](skills/frontend/wallet-connection-ux/) | Phantom/Solflare/Backpack UX, connect/disconnect, state |
| [transaction-signing-and-feedback](skills/frontend/transaction-signing-and-feedback/) | Pending/fail states, retries, confirmations |
| [reading-onchain-state](skills/frontend/reading-onchain-state/) | Fetch patterns, caching, reactivity, indexing |
| [frontend-security-basics](skills/frontend/frontend-security-basics/) | Phishing vectors, approval UX, safety prompts |

### infra/
RPC strategy, indexing, webhooks, monitoring, cost control.

| Skill | Description |
|-------|-------------|
| [rpc-selection-and-resilience](skills/infra/rpc-selection-and-resilience/) | Providers, fallback, retries, timeouts, cost |
| [jito-bundles-and-priority-fees](skills/infra/jito-bundles-and-priority-fees/) | Bundle submission, tip optimization, MEV protection |
| [indexing-strategy](skills/infra/indexing-strategy/) | When you need indexing, event streams, tradeoffs |
| [webhooks-and-event-processing](skills/infra/webhooks-and-event-processing/) | Idempotency, dedupe, queueing concepts |
| [monitoring-and-alerting](skills/infra/monitoring-and-alerting/) | Tx failure rates, RPC health, error classification |
| [cost-planning-for-solana-apps](skills/infra/cost-planning-for-solana-apps/) | Budgeting for infra, growth bursts |

### bots/
Monitoring, alerts, automation, trading architecture.

| Skill | Description |
|-------|-------------|
| [wallet-monitoring-bot](skills/bots/wallet-monitoring-bot/) | Architecture, events, safety, rate limiting |
| [launch-alert-bot](skills/bots/launch-alert-bot/) | Signals, filters, false positives, safe output |
| [social-signal-bot](skills/bots/social-signal-bot/) | X posting cadence, rate limits, content templates |
| [trading-bot-architecture](skills/bots/trading-bot-architecture/) | Execution engine, position management, risk controls |
| [automation-governance](skills/bots/automation-governance/) | What bots should never do, guardrails, logging |

### marketing/
Narratives, announcements, cadence, community ops.

| Skill | Description |
|-------|-------------|
| [memecoin-narrative-engine](skills/marketing/memecoin-narrative-engine/) | Meme frame, story arcs, symbols, cultural hooks |
| [launch-announcement-structures](skills/marketing/launch-announcement-structures/) | Thread format, Telegram pinned message, FAQs |
| [post-launch-content-cadence](skills/marketing/post-launch-content-cadence/) | Day 0-7, week 2-4, maintaining attention ethically |
| [community-ops-playbook](skills/marketing/community-ops-playbook/) | Mods, rules, expectations, handling FUD, legitimacy |

### trust/
Legitimacy signals, disclosures, reputation recovery.

| Skill | Description |
|-------|-------------|
| [legitimacy-signals](skills/trust/legitimacy-signals/) | What buyers look for, what to publish, what to avoid |
| [transparency-and-disclosures](skills/trust/transparency-and-disclosures/) | Clear claims, risk statements, wallet disclosures |
| [rug-detection-checklist](skills/trust/rug-detection-checklist/) | Red flags, contract analysis, LP checks, insider patterns |
| [reputation-recovery-playbook](skills/trust/reputation-recovery-playbook/) | How to respond to mistakes, communicate credibly |

---

## Shareable Prompts (Copy-Paste These)

**For Devs:**
```
Use solana-account-model to design the account structure for a staking program
with user stakes, pool state, and reward distribution. Include PDA seeds,
rent calculations, and CPI considerations.
```

```
Apply anchor-project-scaffold to set up a new Anchor program for a token
vesting contract. Include the folder structure, test setup, and deployment
config for devnet and mainnet.
```

**For Token Launches:**
```
Run spl-token-create-and-configure to create a 6-decimal memecoin with
1 billion supply. Revoke mint and freeze authorities after minting.
Output the full disclosure block with txids.
```

```
Apply launch-readiness-checklist for a pump.fun graduation to Raydium.
Return the go/no-go assessment with evidence for each checkpoint.
```

**For Traders/Trenchers:**
```
Use token-analysis-checklist to analyze this token: [PASTE_MINT_ADDRESS].
Check LP lock status, authority state, holder distribution, and
surface any red flags.
```

```
Apply whale-wallet-analysis to track the top 10 holders of [TOKEN].
Identify which are smart money vs exchange wallets. Look for clustering.
```

**For Infra/Bots:**
```
Use rpc-selection-and-resilience to design an RPC stack for a trading bot
doing 50 TPS with a $500/month budget. Include primary, fallback, and
Jito endpoints with failover logic.
```

```
Apply trading-bot-architecture to spec out a Jupiter-based swap bot with
position limits, slippage controls, and transaction retry logic.
```

**For Trust/Marketing:**
```
Use legitimacy-signals to draft the transparency page for a new memecoin.
Include the address registry, authority disclosures, and risk statements.
```

```
Apply memecoin-narrative-engine to create the brand kit for a dog-themed
token. Output the origin story, 3 core symbols, and a 2-week content calendar.
```

---

## Skill Structure

Every skill follows the same battle-tested format:

```
---
name: skill-name
description: When to use this skill and what it does
---

# Skill Title

Role framing: "You are an expert in..."

## Initial Assessment
Questions to ask before starting

## Core Principles
Invariants that prevent mistakes

## Workflow
Step-by-step process with decision points

## Templates / Playbooks
Reusable structures, tables, checklists

## Common Failure Modes + Debugging
What breaks and how to fix it

## Quality Bar / Validation
How to verify outputs are correct

## Output Format
Exactly what the agent should produce

## Examples
Simple and complex real-world cases
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for:
- Naming conventions (kebab-case)
- Required sections
- Style guide (procedural, specific, verifiable)
- Testing checklist

PRs welcome. Keep it practical. No fluff.

---

## License

MIT - Use it, fork it, ship it.

---

## Quick Reference

See [CHEATSHEETS.md](CHEATSHEETS.md) for copy-paste commands:
- SPL token CLI commands
- Common RPC endpoints
- Anchor CLI workflow
- Jupiter API snippets
- Helius webhook setup

---

Built for builders. Ship fast, stay safe.

> **CTA: Early Access**
> Visit [This Will Do Millions](https://thiswilldomillions.com/) to get notification and early access to our future projects and releases.

> **CTA: Tip Jar**
> If you found this useful, please consider tipping my son's Solana wallet: `A23U9FWCF6tdQ95nuvXaNMN3FYPegCntN4T715svL3HF`.
