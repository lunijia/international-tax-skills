# international-tax-skills

> 🚧 **Work in progress.** This repo is actively being built out — the skill(s) here have been tested but should be considered early versions, not final. New skills will be added over time, and existing ones may be revised as they're used on more real fact patterns. Feedback and corrections are welcome.

A collection of [Claude Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for international tax work — step-by-step workflows that guide Claude (and the humans using it) through recurring analyses like CFC determinations, subpart F/GILTI inclusion questions, withholding tax on payments to foreign persons, and related international tax mechanics.

Each skill packages a repeatable analysis — the applicable Code/Reg framework, a decision procedure, worked examples, and guidance on output format — so the same rigorous walkthrough is available every time, rather than being re-explained from scratch in each conversation.

## What's in here

| Skill | What it does |
|---|---|
| [`cfc-determination`](./cfc-determination) | Walks through whether a foreign corporation is a Controlled Foreign Corporation under I.R.C. § 957, including U.S. Shareholder status (§951(b)), direct/indirect/constructive ownership (§958), and the OBBBA-era §951B FCFC overlay. Aimed at entry-level tax staff or non-tax users. |
| [`withholding-tax-foreign`](./withholding-tax-foreign) | Determines whether U.S. withholding tax applies to a payment made to a foreign person — which regime governs (FDAP under §§1441/1442, FIRPTA under §1445, or partnership ECI withholding under §1446/1446(f)), what rate applies, and what documentation (W-8BEN, W-8BEN-E, W-8ECI, W-8IMY, Form 8233) is required from the payee. |

More skills will be added here over time as they're built and tested.

## Using these skills

Each skill lives in its own folder with a `SKILL.md` (the instructions Claude follows) and, where relevant, a `references/` subfolder with supporting material like worked examples.

- **Claude.ai / Claude apps:** upload or install the skill from its packaged `.skill` file, or point Claude at the `SKILL.md` directly.
- **Claude Code / API:** drop the skill folder into your skills directory so Claude can discover and load it automatically when a relevant task comes up.

See Anthropic's [Agent Skills documentation](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for setup details.

## Repo structure

```
international-tax-skills/
├── README.md
├── cfc-determination/
│   ├── SKILL.md
│   └── references/
│       └── examples.md
└── withholding-tax-foreign/
    ├── SKILL.md
    └── references/
        └── examples.md
```

Each new skill gets its own top-level folder following this same pattern: `SKILL.md` plus an optional `references/` folder for material that doesn't need to be loaded into context every time.

## Contributing

Skills here are built and reviewed by working through real fact patterns before merging, not just written from memory of the rules — see each skill's PR for the test cases used to validate it. When adding a new skill:

1. Base it on primary source material (Code sections, regs, or reliable secondary sources) rather than general recollection.
2. Include worked examples in a `references/` file where the analysis has enough nuance to benefit from them.
3. Test it against a few realistic fact patterns — including edge cases — before opening a PR.
4. Note any known limitations or areas that still require senior review in the skill's output guidance.

## Disclaimer

These skills are educational aids that walk through the mechanics of a given test. They are not a substitute for professional judgment and do not constitute tax advice or a filing position. Always have conclusions reviewed by a qualified tax professional before relying on them.
