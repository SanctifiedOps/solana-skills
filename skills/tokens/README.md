# Token Skills

SPL token creation, authorities, distribution, tokenomics, and post-launch operations.

## Skills in This Pillar

| Skill | Description | Difficulty |
|-------|-------------|------------|
| [spl-token-create-and-configure](spl-token-create-and-configure/) | Mint creation, authorities, decimals, revoke flows | Beginner |
| [token-authority-and-risk](token-authority-and-risk/) | Mint/freeze authority implications, best practices | Beginner |
| [token-distribution-planning](token-distribution-planning/) | Wallet splits, allocations, vesting, transparency | Intermediate |
| [tokenomics-design-for-memecoins](tokenomics-design-for-memecoins/) | Supply narrative, burns, sinks, incentives | Intermediate |
| [post-launch-token-ops](post-launch-token-ops/) | Treasury policy, unlock communications, LP considerations | Intermediate |
| [token-2022-extensions](token-2022-extensions/) | Transfer fees, permanent delegate, metadata pointer, confidential transfers | Advanced |

## When to Use These Skills

- **Creating a new token**: Start with `spl-token-create-and-configure`
- **Designing tokenomics**: Use `tokenomics-design-for-memecoins`
- **Planning distribution**: Use `token-distribution-planning`
- **Adding advanced features**: Use `token-2022-extensions`
- **Managing post-launch**: Use `post-launch-token-ops`

## Quick Start

**Create a memecoin:**
```
Run spl-token-create-and-configure to create a 6-decimal token
with 1 billion supply. Revoke mint and freeze authorities.
Output the disclosure block with txids.
```

**Design tokenomics:**
```
Apply tokenomics-design-for-memecoins to create the supply
narrative and sink mechanics for a dog-themed memecoin.
```

## Related Skills

- [launch/launch-readiness-checklist](../launch/launch-readiness-checklist/) - Pre-launch preparation
- [trust/legitimacy-signals](../trust/legitimacy-signals/) - Building trust
- [trading/token-analysis-checklist](../trading/token-analysis-checklist/) - Buyer perspective
