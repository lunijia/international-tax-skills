---
name: cfc-determination
description: Guides a step-by-step analysis of whether a foreign corporation is a Controlled Foreign Corporation (CFC) under I.R.C. § 957, including U.S. Shareholder status (§951(b)), direct/indirect ownership (§958(a)), constructive/attribution ownership (§958(b)), and the OBBBA-era §951B "foreign-controlled U.S. Shareholder" / FCFC rules. Use this skill whenever the user asks whether an entity is a CFC, asks about U.S. Shareholder status, subpart F or GILTI/NCTI inclusion eligibility, foreign ownership/attribution structures, or presents an ownership chart/cap table of a foreign corporation and wants to know the U.S. tax consequences — even if they don't use the term "CFC" explicitly (e.g. "does this foreign sub trigger a US inclusion", "who counts as a 10% owner here"). Designed to walk entry-level tax staff or non-tax users through the analysis in plain language, asking for missing ownership facts before concluding.
---

# CFC Determination

Walks the user through determining whether a foreign corporation is a Controlled Foreign Corporation (CFC), aimed at entry-level tax staff or non-tax professionals who need a rigorous but understandable analysis.

## Before you start: gather the facts

Do not run the test on an incomplete fact pattern. If any of the following are missing from what the user gave you, ask for them before concluding (a couple of quick targeted questions is fine — don't interrogate the user with everything at once if the answer is likely obvious from context):

1. **Is the entity actually a foreign corporation?** (Not a foreign partnership, disregarded entity, or U.S. corporation.)
2. **Full ownership list**, including:
   - Every shareholder (direct owners) and their % of vote and % of value (these can differ — always ask if only one is given, and note if unknown)
   - Any ownership held *through* other entities (partnerships, other corporations, trusts) — need the ownership chain, not just the ultimate individual
3. **Related-party relationships** among the shareholders — family members (spouse, children, parents, grandchildren — see attribution notes below), or common ownership of other entities in the chain. Users often omit this; explicitly ask "are any of these owners related to each other, or do any of them own the other entities in this structure?"
4. **The tax year at issue** — needed because §958(b)(4)'s repeal/reinstatement timing matters (see below).
5. Whether the user cares only about classic CFC status, or also wants the §951B FCFC check (relevant if there's foreign-parent ownership above a U.S. entity in the chain — see Step 6).

If the user gives a clean, complete fact pattern up front, skip straight to the analysis — don't ask questions just to ask them.

## The analysis

Work through these steps in order and show your work at each step — don't jump to the conclusion. Use the user's actual entity/person names throughout, not generic labels.

### Step 1 — Foreign corporation?
If not a foreign corporation, stop: not a CFC (CFC status only applies to foreign corporations). I.R.C. § 957(a).

### Step 2 — Identify all U.S. persons in the ownership chain
A "U.S. person" is defined in I.R.C. § 957(c) (citizens, residents, domestic corporations/partnerships/trusts/estates, etc.). Only U.S. persons can be "U.S. Shareholders."

### Step 3 — Calculate each U.S. person's ownership using all three measures
For each U.S. person, compute:
- **Direct ownership** — stock held in their own name
- **Indirect ownership** (§958(a)) — ownership through foreign entities in the chain (e.g., 10% of a foreign parent that owns 51% of the target = 5.1% indirect). Ownership through domestic (U.S.) entities is treated as direct-equivalent for this purpose — a U.S. partnership/corporation/trust that owns stock is itself a U.S. person capable of being a U.S. Shareholder in its own right.
- **Constructive ownership** (§958(b)) — attribution from related parties, applying §318 as modified by §958(b)(1)-(4). Common triggers: spouse/children/grandchildren/parents owning stock (family attribution), a person owning >50% of an entity that owns stock (entity-to-owner attribution), or an entity being deemed to own 100% of a subsidiary's stock in an upper-tier corporation once that entity owns >50% of the subsidiary (used in chains — see Example 8 in references/examples.md).

**Important nuance:** indirect and constructive ownership are not simply added — for a given block of stock, if constructive ownership rules produce a *larger* ownership percentage than the indirect ownership rules do, constructive ownership controls for that block (Reg. § 1.958-2(f)(2)). Walk through both computations and use the larger figure per relevant block; don't double count the same shares twice.

**§958(b)(4) timing:** This provision limits certain downward attribution from foreign persons to U.S. persons. It was repealed by the TCJA (2017) and reinstated by OBBBA for tax years of the foreign corporation beginning after December 31, 2025. For tax years straddling or before that date, flag this explicitly to the user and note the constructive-ownership analysis may differ — don't silently assume one regime.

### Step 4 — Identify the U.S. Shareholders
A "U.S. Shareholder" (capitalized) is any U.S. person from Step 2 whose combined direct + indirect + constructive ownership (per the Step 3 rule) is **≥10%** of either total voting power or total value. I.R.C. § 951(b). Use ≥10% (not >10%) — this is a bright-line inclusive threshold.

If no U.S. person meets 10%, stop here: **not a CFC** (no U.S. Shareholders to test).

### Step 5 — Aggregate and test the >50% threshold
Add together the ownership of *all* U.S. Shareholders identified in Step 4. If their combined vote **or** combined value exceeds 50% (strictly greater than, not equal to), the foreign corporation **is a CFC**. I.R.C. § 957(a). If combined ownership is exactly 50% or less, it is **not a CFC** under the classic test — but continue to Step 6 before concluding.

**Don't double-count stock between related U.S. Shareholders.** When two or more U.S. Shareholders are related to each other (e.g., spouses, parent/child) and each one's Step 4 percentage includes stock attributed *from the other*, that same underlying stock will inflate both of their individual percentages. When aggregating in Step 5, count the underlying shares actually held by the group once, not each person's (overlapping) attributed percentage summed together. Concretely: if A owns 7% directly and A's spouse owns 5% directly (nothing else in play), A's individual total is 12% and spouse's individual total is 12% — each independently clears the 10% U.S. Shareholder threshold — but the group's real combined stake is only 7%+5%=12% of the company, not 24%. Aggregate the actual underlying stock held by all U.S. Shareholders as a group, then check that group total against 50%. See references/examples.md for a worked version of this.

### Step 6 — Check the §951B FCFC rule even if Step 5 says "not a CFC"
OBBBA's new I.R.C. § 951B can still trigger a subpart F / net CFC tested income (NCTI) inclusion for a U.S. person even when the entity fails the classic CFC test, if there's a foreign-parent-controlled group structure — typically: a foreign parent owns a U.S. subsidiary, and that U.S. subsidiary (directly or indirectly) owns a minority stake in another foreign corporation that the foreign parent also owns. Ask whether there's a foreign parent above any U.S. entity in the ownership chain; if so, flag that §951B analysis may independently require an inclusion for the U.S. entity even though the foreign corporation itself is not a CFC under §957. This is a narrower, specialized check — flag it as something to raise with a senior reviewer rather than fully resolving it yourself unless the user gives you a complete picture of the group structure.

## Delivering the answer

- **Default:** walk through Steps 1–6 conversationally in chat, showing the percentage math at each step, and end with a clear bolded conclusion (**CFC** / **Not a CFC**) plus a one-line reason.
- **If the user asks for a memo, writeup, or something to save/share:** produce it as a Word document — read `/mnt/skills/public/docx/SKILL.md` first, then structure it as Facts → Analysis (steps 1-6) → Conclusion, citing the same Code/Reg sections used in chat.
- Always include a short caveat that this is an educational walkthrough of the mechanical test, not a filing position — real fact patterns often have wrinkles (options, convertible instruments, PFIC overlap, treaty issues) that warrant review by a senior tax professional before relying on the conclusion.

## Reference material

See `references/examples.md` for nine fully worked examples (equal-ownership groups, partnership ownership, attribution chains, the constructive-vs-indirect override case, and the §951B FCFC fact pattern) — use these to sanity-check your own math on a new fact pattern, or to explain a step to the user by analogy.
