# Contributing to Solana Skills

We keep skills Corey-style: **procedural, specific, and verifiable**.

---

## How to Add or Update a Skill

### 1. Folder Structure
- Use kebab-case folder names under the correct pillar
- Path format: `skills/<pillar>/<skill-name>/SKILL.md`
- Example: `skills/core-dev/new-skill/SKILL.md`

### 2. YAML Frontmatter (Required)
Every SKILL.md must start with:
```yaml
---
name: skill-name
description: When to trigger and what it does (one concise sentence)
---
```

### 3. Required Sections (In This Order)

```markdown
# Skill Title

Role framing: "You are an expert in [domain]. Your goal is to [outcome]."

## Initial Assessment
- Questions to ask before starting
- Context to gather
- Dependencies to check

## Core Principles
- Invariants that prevent dumb mistakes
- Rules that always apply
- Things to never do

## Workflow
1. Step-by-step process
2. Include decision points
3. Commands with actual syntax
4. Checkpoints for validation

## Templates / Playbooks
- Reusable tables
- Checklists
- Code snippets
- Configuration examples

## Common Failure Modes + Debugging
- What breaks and why
- How to detect each failure
- How to fix each failure
- Prevention strategies

## Quality Bar / Validation
- How to verify outputs are correct
- What "done" looks like
- Acceptance criteria

## Output Format
- Specify exactly what the agent should produce
- Section structure
- Required artifacts

## Examples
### Simple Example
[Realistic basic case with inputs and outputs]

### Complex Example
[Realistic advanced case with edge cases]
```

---

## Style Guide

### Tone
- Match Corey Haines's marketingskills approach
- Expert SOPs, not tutorials
- Write like internal documentation from someone in the trenches
- Imperative voice ("Do X", not "You should do X")

### Content
- **Be specific**: Include actual commands, real addresses (devnet), concrete numbers
- **Be practical**: Every workflow step should be executable
- **Be honest**: Call out what doesn't work, what's risky, what's unknown
- **No fluff**: Cut marketing language, cut obvious statements, cut filler

### Formatting
- Prefer bullets and short paragraphs
- Use tables for comparisons and checklists
- Include code blocks with language tags
- Keep sections scannable

### Examples Must Include
- At least 2 examples (simple + complex)
- Real-world scenarios, not toy examples
- Actual inputs and expected outputs
- Edge cases in complex example

---

## Code Standards

When including code:

```typescript
// Include language tag
// Use realistic variable names
// Show error handling
// Include comments for non-obvious parts
```

When including CLI commands:

```bash
# Include actual flags
# Show expected output format
# Note environment requirements
spl-token create-token --decimals 6 --mint-authority <KEYPAIR>
# Output: Creating token <MINT_ADDRESS>
```

---

## Testing / QA Checklist

Before submitting:

- [ ] YAML frontmatter parses (name + description only)
- [ ] All required sections present and non-empty
- [ ] Role framing states expertise and goal clearly
- [ ] Initial Assessment has 5+ relevant questions
- [ ] Core Principles has 4+ actionable rules
- [ ] Workflow has numbered steps with decision points
- [ ] Templates section has at least one reusable artifact
- [ ] Failure Modes has 4+ specific failures with fixes
- [ ] Quality Bar has measurable criteria
- [ ] Output Format specifies exact deliverables
- [ ] Simple Example is realistic and complete
- [ ] Complex Example shows edge cases
- [ ] No broken links or placeholder text
- [ ] Commands are tested or clearly marked as examples
- [ ] Spell-check passed (especially addresses)

---

## Pillar Descriptions

Use these to decide where your skill belongs:

| Pillar | Scope |
|--------|-------|
| `core-dev/` | Solana program development, Anchor, accounts, security |
| `tokens/` | SPL token creation, authorities, distribution, tokenomics |
| `trading/` | Token analysis, DEX integration, whale tracking, market dynamics |
| `launch/` | Launch operations, fairness, liquidity, snipers, stabilization |
| `frontend/` | Wallet UX, transaction signing, state reading, security |
| `infra/` | RPC, indexing, webhooks, monitoring, cost management |
| `bots/` | Automation, monitoring bots, trading bots, governance |
| `marketing/` | Narratives, announcements, content cadence, community ops |
| `trust/` | Legitimacy, disclosures, rug detection, reputation |

---

## Submitting Changes

### Pull Request Guidelines
- One skill per PR (unless tightly related)
- Keep diffs focused
- Include brief summary of changes
- Note any commands or tests you ran

### What to Include in PR Description
```markdown
## Summary
What this skill does and who it's for.

## Changes
- Added/modified sections
- New examples added
- Commands tested

## Testing
- [ ] Tested on devnet
- [ ] QA checklist completed
- [ ] Examples verified
```

### After Merging
- Update README.md if adding a flagship skill
- Update CHEATSHEETS.md if adding commonly-used commands

---

## Questions?

Open an issue or ping in the community channel. We're here to help you ship.
