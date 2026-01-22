# Core Development Skills

Solana program development fundamentals: accounts, Anchor, PDAs, security, and upgrades.

## Skills in This Pillar

| Skill | Description | Difficulty |
|-------|-------------|------------|
| [solana-account-model](solana-account-model/) | Accounts, owners, signers, rent, PDAs, CPI mental model | Beginner |
| [anchor-project-scaffold](anchor-project-scaffold/) | Project setup, program/client layout, env config, dev workflow | Beginner |
| [instruction-design-and-validation](instruction-design-and-validation/) | Inputs, constraints, invariants, authority checks | Intermediate |
| [pda-design-playbook](pda-design-playbook/) | Seed strategy, collisions, upgrade considerations | Intermediate |
| [common-anchor-errors-debugger](common-anchor-errors-debugger/) | Account discriminator mismatch, constraint failures, etc. | Intermediate |
| [program-security-basics](program-security-basics/) | Authority checks, unsafe patterns, attack surfaces | Advanced |
| [upgrade-vs-immutable-decision](upgrade-vs-immutable-decision/) | Tradeoffs, trust, governance, operations | Intermediate |
| [compressed-nfts-basics](compressed-nfts-basics/) | Merkle trees, concurrent trees, cNFT minting and transfers | Intermediate |

## Learning Path

1. **Start here**: `solana-account-model` - understand the fundamentals
2. **Setup**: `anchor-project-scaffold` - create your first project
3. **Design**: `instruction-design-and-validation` + `pda-design-playbook`
4. **Debug**: `common-anchor-errors-debugger` when things break
5. **Secure**: `program-security-basics` before deploying
6. **Decide**: `upgrade-vs-immutable-decision` for production

## Quick Start

**Understand Solana's account model:**
```
Use solana-account-model to explain PDAs, rent, and CPI
for a staking program design.
```

**Set up a new Anchor project:**
```
Apply anchor-project-scaffold to create a token vesting
contract with devnet and mainnet deployment configs.
```

## Related Skills

- [tokens/spl-token-create-and-configure](../tokens/spl-token-create-and-configure/) - Token creation
- [infra/rpc-selection-and-resilience](../infra/rpc-selection-and-resilience/) - RPC setup
- [frontend/wallet-connection-ux](../frontend/wallet-connection-ux/) - Frontend integration
