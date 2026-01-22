# Launch Skills

Token and dApp launch operations: preparation, fair launch patterns, liquidity, snipers, and stabilization.

## Skills in This Pillar

| Skill | Description | Difficulty |
|-------|-------------|------------|
| [launch-readiness-checklist](launch-readiness-checklist/) | Pre-flight checklist: infra, wallets, LP, comms, rollback | Intermediate |
| [fair-launch-patterns](fair-launch-patterns/) | What "fair" means operationally, tradeoffs, dynamics | Intermediate |
| [liquidity-and-price-dynamics-explainer](liquidity-and-price-dynamics-explainer/) | LP basics, slippage, volatility mechanics | Beginner |
| [sniper-dynamics-and-mitigation](sniper-dynamics-and-mitigation/) | Threat model, defensive posture | Advanced |
| [post-launch-stabilisation-playbook](post-launch-stabilisation-playbook/) | What to monitor, comms, product milestones | Intermediate |

## Launch Sequence

1. **Planning**: Define scope, timeline, dependencies
2. **Preparation**: `launch-readiness-checklist` - verify everything
3. **Fairness**: `fair-launch-patterns` - choose and implement
4. **Defense**: `sniper-dynamics-and-mitigation` - protect against bots
5. **Go-live**: Execute with monitoring
6. **Stabilize**: `post-launch-stabilisation-playbook` - first 48 hours

## Quick Start

**Pre-launch checklist:**
```
Apply launch-readiness-checklist for a Raydium LP launch.
Return go/no-go assessment with evidence for each checkpoint.
```

**Understand liquidity:**
```
Use liquidity-and-price-dynamics-explainer to explain
how LP depth affects price impact for a $50k trade.
```

## Related Skills

- [tokens/spl-token-create-and-configure](../tokens/spl-token-create-and-configure/) - Token setup
- [infra/rpc-selection-and-resilience](../infra/rpc-selection-and-resilience/) - Infrastructure
- [marketing/launch-announcement-structures](../marketing/launch-announcement-structures/) - Comms
- [trust/legitimacy-signals](../trust/legitimacy-signals/) - Building trust
