# Infrastructure Skills

RPC strategy, Jito bundles, indexing, webhooks, monitoring, and cost management.

## Skills in This Pillar

| Skill | Description | Difficulty |
|-------|-------------|------------|
| [rpc-selection-and-resilience](rpc-selection-and-resilience/) | Providers, fallback, retries, timeouts, cost | Beginner |
| [jito-bundles-and-priority-fees](jito-bundles-and-priority-fees/) | Bundle submission, tip optimization, MEV protection | Advanced |
| [indexing-strategy](indexing-strategy/) | When you need indexing, event streams, tradeoffs | Intermediate |
| [webhooks-and-event-processing](webhooks-and-event-processing/) | Idempotency, dedupe, queueing concepts | Intermediate |
| [monitoring-and-alerting](monitoring-and-alerting/) | Tx failure rates, RPC health, error classification | Intermediate |
| [cost-planning-for-solana-apps](cost-planning-for-solana-apps/) | Budgeting for infra, growth bursts | Beginner |

## When to Use These Skills

- **Setting up RPC**: Start with `rpc-selection-and-resilience`
- **Building a trading bot**: Use `jito-bundles-and-priority-fees` for MEV protection
- **Processing on-chain events**: Use `webhooks-and-event-processing`
- **Planning costs**: Use `cost-planning-for-solana-apps`

## Quick Start

**Design RPC stack:**
```
Use rpc-selection-and-resilience to design an RPC stack for
a trading bot doing 50 TPS with a $500/month budget.
Include primary, fallback, and failover logic.
```

**Implement priority fees:**
```
Apply jito-bundles-and-priority-fees to add MEV protection
to a DEX swap transaction with dynamic tip calculation.
```

## Related Skills

- [bots/trading-bot-architecture](../bots/trading-bot-architecture/) - Bot building
- [frontend/wallet-connection-ux](../frontend/wallet-connection-ux/) - Frontend integration
- [launch/launch-readiness-checklist](../launch/launch-readiness-checklist/) - Launch infrastructure
