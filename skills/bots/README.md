# Bot Skills

Monitoring, alerts, automation, and trading bot architecture.

## Skills in This Pillar

| Skill | Description | Difficulty |
|-------|-------------|------------|
| [wallet-monitoring-bot](wallet-monitoring-bot/) | Architecture, events, safety, rate limiting | Intermediate |
| [launch-alert-bot](launch-alert-bot/) | Signals, filters, false positives, safe output | Intermediate |
| [social-signal-bot](social-signal-bot/) | X posting cadence, rate limits, content templates | Intermediate |
| [trading-bot-architecture](trading-bot-architecture/) | Execution engine, position management, risk controls | Advanced |
| [automation-governance](automation-governance/) | What bots should never do, guardrails, logging | Intermediate |

## When to Use These Skills

- **Tracking wallets**: Use `wallet-monitoring-bot` for whale alerts
- **Finding new tokens**: Use `launch-alert-bot` for discovery
- **Automated trading**: Use `trading-bot-architecture` for full system design
- **Social automation**: Use `social-signal-bot` with `automation-governance`

## Quick Start

**Build a whale alert bot:**
```
Apply wallet-monitoring-bot to create a Discord alert bot
that tracks top 10 holders of [TOKEN] for transfers > $10k.
```

**Design a trading bot:**
```
Use trading-bot-architecture to spec a Jupiter-based swap bot
with position limits, slippage controls, and risk management.
```

## Safety First

All bot skills include:
- Rate limiting to respect API quotas
- Logging for debugging and auditing
- Safety checks to prevent unintended actions
- Governance guardrails

See `automation-governance` for what bots should **never** do.

## Related Skills

- [infra/rpc-selection-and-resilience](../infra/rpc-selection-and-resilience/) - RPC setup
- [infra/jito-bundles-and-priority-fees](../infra/jito-bundles-and-priority-fees/) - Transaction optimization
- [trading/jupiter-swap-integration](../trading/jupiter-swap-integration/) - Swap implementation
