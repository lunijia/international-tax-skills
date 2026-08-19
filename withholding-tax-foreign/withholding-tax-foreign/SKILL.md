---
name: withholding-tax-foreign
description: Guides a step-by-step determination of whether U.S. withholding tax applies to a payment made to a foreign person — which regime governs (FDAP under §§1441/1442, FIRPTA under §1445, or partnership ECI withholding under §1446/1446(f)), what rate applies, and what documentation (W-8BEN, W-8BEN-E, W-8ECI, W-8IMY, Form 8233) is required from the foreign payee. Use whenever the user asks whether a payment to a foreign person requires withholding, what rate applies to a dividend/interest/royalty/rent/compensation/real-property/partnership payment to a foreign payee, which W-8 form a foreign payee needs, or how much to withhold — even without the word "withholding" (e.g. "do we need documentation from this vendor", "how much do we send this foreign investor vs. the IRS"). Walks entry-level tax/finance staff through the analysis, asking for missing facts before concluding. Scoped to foreign payees only — does not cover U.S.-payee backup withholding.
---

# Withholding Tax on Foreign Payments (FDAP / FIRPTA / Partnership ECI)

Walks through whether a U.S. withholding obligation applies to a payment, which of three regimes governs, the applicable rate, and the documentation needed — aimed at entry-level tax/finance staff or non-tax professionals.

**Scope of this version:** Payments to **foreign payees** only — FDAP withholding (I.R.C. §§1441/1442), FIRPTA (I.R.C. §1445/897), and partnership ECI withholding (I.R.C. §1446 and §1446(f)). This skill assumes the payee has already been identified as foreign (or is being evaluated for foreign status) — it does not address backup withholding under I.R.C. §3406, which is a separate regime that applies only to U.S. payees who fail to provide a valid Form W-9/TIN. If a fact pattern turns out to involve a U.S. payee, flag that this skill's analysis doesn't apply and backup withholding rules should be considered separately. FATCA (§§1471-1474) is also a related but separate withholding regime not yet covered by this skill — flag to the user that a payment involving a foreign financial institution or non-financial foreign entity may also need a separate FATCA analysis, but don't attempt to resolve it with this skill's logic.

## Before you start: gather the facts

Don't run the analysis on an incomplete fact pattern. Ask for whatever is missing from this list before concluding (a couple of targeted questions is fine — don't ask everything if most is already obvious from context):

1. **What is the payment?** (dividend, interest, royalty, rent, compensation for services, scholarship/fellowship, sale proceeds from U.S. real property, a partnership distribution or a foreign partner's distributive share of income, proceeds from selling a partnership interest, other)
2. **Who is the payee, and what is their status?** Confirm the payee is foreign (this skill doesn't cover the U.S.-payee backup withholding analysis — if the payee turns out to be a U.S. person, say so and stop). Individual or entity (corporation, partnership, trust, disregarded entity)? If entity, is it itself a partnership with its own partners (may require looking through tiers)?
3. **What documentation is already on file** for the payee — W-8BEN, W-8BEN-E, W-8ECI, W-8IMY, W-8EXP, Form 8233, or none?
4. **Is there an intermediary** between the payor and the ultimate beneficial owner (a bank, broker, or foreign partnership)? If so, has it represented a status (qualified intermediary, nonqualified intermediary, withholding foreign partnership, U.S. branch electing U.S.-person treatment)?
5. **If a treaty-reduced rate is being claimed:** what treaty country, and what income type? Don't ask the user to supply the rate — retrieve it yourself using the IRS lookup process in "Looking up the treaty rate" below, and confirm the payee has a valid W-8 on file supporting the treaty claim before applying it.
6. **If real property is involved:** is the underlying asset a U.S. real property interest (USRPI)? What is the amount realized? Is the seller providing any exemption certification (U.S.-person affidavit, non-USRPHC corporate affidavit, IRS exemption statement)? Is this a personal residence purchase ≤$300,000?
7. **If a partnership is involved:** domestic or foreign partnership? Is this a distributive share of ECI, an actual distribution, or a sale of the partnership interest itself? Are there tiered partnerships?

If the user gives a complete, clean fact pattern up front, skip straight to the analysis.

## Step 1 — Classify the payment into the right regime

Work through these in order — the first one that fits controls:

- **Disposition of a U.S. real property interest (USRPI)** by a foreign person → go to **FIRPTA analysis** (below). This includes stock of a U.S. real property holding corporation and certain partnership interests where ≥50% of gross assets are USRPIs (and ≥90% are USRPIs plus cash/cash-equivalents). Reg. §1.1445-11T(d).
- **A foreign partner's distributive share of income effectively connected with a U.S. trade or business (ECI), a distribution of such income, or a sale of the partnership interest itself** → go to **Partnership ECI withholding analysis** (below). I.R.C. §1446, §1446(f).
- **Compensation for personal services** → not §1441/1442 FDAP withholding; subject to wage withholding instead (see Form 8233 for treaty-exempt compensation). Flag this to the user and stop the FDAP analysis — point them to standard payroll withholding procedures instead.
- **A scholarship or fellowship grant** (amounts not representing pay for services) to a nonresident alien for study/training/research in the U.S. → subject to 14% withholding under I.R.C. §871(c), unless excluded from income under §117.
- **Passive/investment-type U.S.-source income** (dividends, interest, royalties, rents, and other FDAP items) paid to or for the benefit of a foreign person, not otherwise carved out above → go to **FDAP withholding analysis** (below). I.R.C. §§1441, 1442.
- **Income effectively connected with a U.S. trade or business, not from a partnership** (e.g., a foreign corporation's U.S. branch income) → generally not subject to §1441 withholding if a valid W-8ECI is on file; the recipient self-reports and pays tax through its own return (Form 1120-F / Form 1040-NR) instead.

## Step 2 — FDAP withholding analysis (I.R.C. §§1441/1442)

### The six-factor test
Withholding under §1441/1442 generally applies only if **all six** are true:
1. The recipient is a foreign person.
2. The amount paid is U.S.-source income.
3. The income is FDAP (fixed or determinable, annual or periodical — i.e., generally passive investment income).
4. The income is **not** effectively connected with a U.S. trade or business (an ECI payment with a valid W-8ECI on file is exempt from §1441 withholding — the recipient reports and pays tax directly).
5. The payor (or an agent of the payor) is a withholding agent.
6. No exception applies (see below).

If any factor fails, §1441/1442 withholding does not apply on that basis — but double-check Step 1 to make sure a different regime (FIRPTA, §1446) doesn't apply instead.

### Looking up the treaty rate (required whenever a treaty claim is in play)

Never guess a treaty rate from memory or assume a "typical" rate — always retrieve it live from the IRS's own tables. These four PDFs are the official source and should be fetched directly when a treaty rate determination is needed:

- **Table 1** — https://www.irs.gov/pub/irs-lbi/tax-treaty-table-1.pdf — rates on income *other than* personal services: interest, dividends (general and direct-dividend rate), pensions/annuities, social security, and royalties broken out by category (industrial equipment, know-how/other industrial, patents, film & TV, copyrights). This is the table for the FDAP payment types (dividends, interest, royalties) this skill covers. Rows are by country; columns are keyed by Form 1042-S income code (matches the income code you'd report on Form 1042-S).
- **Table 2** — https://www.irs.gov/pub/irs-lbi/tax-treaty-table-2.pdf — personal service income (compensation, independent personal services, students/researchers). Use only if Step 1 routed the payment to the compensation/Form 8233 path rather than FDAP.
- **Table 3** — https://www.irs.gov/pub/irs-lbi/table-3-list-of-tax-treaties.pdf — confirms the treaty is currently in force for that country, its effective date, and lists any amending protocols. Check this when there's any doubt about whether a treaty exists or is still in effect (treaties do get terminated or renegotiated).
- **Table 4** — https://www.irs.gov/pub/irs-lbi/Tax_Treaty_Table_4.pdf — Limitation on Benefits (LOB) — the entitlement test a treaty-country resident must independently satisfy to claim any benefit at all. A country appearing in Table 1 does not by itself mean a given payee qualifies; note to the user that LOB should be confirmed, especially for entities (as opposed to individual payees).

**Process:**
1. Fetch Table 1 (or Table 2 for personal services) via `web_fetch`.
2. Find the payee's country row and the specific income-type column (e.g., "Royalties — Patents" vs. "Royalties — Copyrights" are frequently different rates within the same country — match the specific income sub-type, don't assume all royalties in a treaty get the same rate).
3. **Check the footnote letters next to the rate.** Table 1 is heavily qualified — footnotes can exempt the payment entirely, apply a different rate for a sub-category (e.g., REIT/RIC dividends, contingent interest, pension funds), or impose ownership-percentage or permanent-establishment conditions. Read the specific footnote(s) attached to the cell you're using before quoting the rate to the user.
4. Note the Treaty Article Citation shown for that cell — this is what would go in a memo or on Form 8833 if a treaty position needs disclosure.
5. If there's any doubt about whether the treaty is currently in force, fetch Table 3 to confirm.
6. State the rate, article, and any relevant footnote conditions to the user, and flag that LOB (Table 4) should be confirmed for the specific payee before relying on the rate.

### Common exceptions to FDAP withholding
Portfolio interest; bank deposit interest; short-term original issue discount (OID) on an obligation payable within 183 days of original issue (I.R.C. §871(g)); wages (subject to payroll withholding instead); ECI with a valid W-8ECI. Reg. §1.1441-2(a).

**Portfolio interest carve-outs — check these before applying the exception.** The portfolio interest exception does NOT apply (so the general 30%/treaty rate applies instead) if any of the following describe the recipient: (a) a 10%-or-more shareholder of the payor (I.R.C. §871(h)(3)(B)/§881(c)(3)(B)); (b) a controlled foreign corporation (CFC) receiving interest from a person related to it (I.R.C. §881(c)(3)(C)) — this commonly disqualifies intercompany loans where a foreign subsidiary lends to (or holds a receivable from) its U.S. parent or another related U.S. affiliate; (c) a bank receiving interest on an extension of credit made in the ordinary course of its banking business (I.R.C. §881(c)(3)(A)); or (d) the interest is contingent interest as defined in I.R.C. §871(h)(4). Always check for a related-party relationship between payor and payee before assuming portfolio interest applies — it's a frequent trap in intercompany financing fact patterns.

### Determine the payee's status and rate
- **Foreign person, no treaty claim or no valid documentation:** withhold **30%** of the gross amount. I.R.C. §§1441(a), 1442(a). This is the default statutory rate — confirmed current per the 2025 Instructions for Form 1042 (the escrow procedure under Reg. §1.1441-3(d), used when a withholding agent cannot yet determine the taxable portion of a payment, defaults to withholding 30% on the entire payment).
- **Foreign person claiming a reduced treaty rate**, with a valid Form W-8BEN (individual) or W-8BEN-E (entity) on file establishing treaty-country residence and entitlement: withhold at the treaty rate retrieved via the "Looking up the treaty rate" process above — never assume a number.
- **Foreign person providing a valid Form W-8ECI:** income is ECI, not FDAP — no §1441 withholding; recipient self-reports.
- **Foreign government or controlled entity providing Form W-8EXP:** may be exempt under I.R.C. §892 for certain FDAP income.

### Payments through intermediaries or flow-through entities
- **Nonqualified intermediary (NQI):** no IRS withholding agreement. Must furnish the withholding agent with documentation identifying the ultimate beneficial owners and their allocable amounts (via Form W-8IMY plus the underlying W-8BEN(-E)/W-9 forms); if it doesn't, withhold at the full statutory rate on the whole payment.
- **Qualified intermediary (QI):** has an IRS withholding agreement. May assume primary withholding responsibility (PWR) — in that case, the original withholding agent does not withhold; the QI does. A non-PWR QI collects beneficial-owner documentation but reports it to the withholding agent via withholding-rate pools rather than individually.
- **Withholding foreign partnership (WFP):** has an IRS agreement to assume withholding responsibility; the withholding agent treats payments to it like payments to a domestic partnership (no withholding at the point of payment to the entity) and the WFP withholds later per domestic-partnership timing rules.
- **U.S. branch of a foreign bank/insurance company:** may elect (with proper agreement/documentation) to be treated as a U.S. person for withholding purposes, removing the obligation from the original withholding agent.
- **Payment to a domestic partnership:** no §1441 withholding on the payment to the partnership itself (even if some partners are foreign) — instead, the domestic partnership becomes the withholding agent for the foreign partners' distributive shares (see §1446 below for the ECI case; for FDAP-type income allocated to a foreign partner, the domestic partnership must withhold on distributions or guaranteed payments).
- **Payment to a foreign partnership (not a WFP):** look through to the individual partners (and further, through any additional tiers of pass-through entities) to determine each partner's status and rate. If partner-level information is incomplete, withhold at the highest applicable rate on the unaccounted-for portion.

### Worked example (see references/examples.md for the full walkthrough)
A $120 dividend paid to a foreign partnership with three equal partners in different treaty positions splits into separate withholding calculations per partner, then aggregates to a single amount remitted — see reference file for the full mechanics.

## Step 3 — FIRPTA analysis (I.R.C. §1445, §897)

1. **Is the asset a USRPI?** Direct U.S. real property, or stock of a U.S. real property holding corporation, or (for a partnership interest) an interest where ≥50% of the partnership's gross assets are USRPIs and ≥90% are USRPIs plus cash/cash-equivalents.
2. **Is the transferor foreign?** If the seller provides a valid affidavit of U.S. status, no withholding is required — even if the underlying entity is a partnership with foreign partners (the partnership itself handles its partners' withholding separately).
3. **Check exceptions:** IRS exemption statement; corporate affidavit that it is not (and has not been within the 5-year testing period) a U.S. real property holding corporation; personal-residence purchase where the price does not exceed $300,000; qualified foreign pension fund under I.R.C. §897(l) (certified per Reg. §1.1445-8(e)).
4. **Determine the rate** (absent an exception):
   - General rule: transferee withholds **15%** of the total amount realized. I.R.C. §1445(a).
   - Domestic partnership disposing of a USRPI, on the gain allocable to foreign partners: **21%**. I.R.C. §1445(e)(1). *(Your source notes cite a distribution-related 21% rate to "§1441(e)(2) and (3)" — this is very likely a transcription artifact for §1445(e)(2)-(3); confirm the exact citation against the current Code before relying on it in a work product.)*
5. **Check for overlap with §1446:** if the same gain is also ECI subject to partnership withholding under §1446, §1446 controls and there is no double withholding; a foreign partnership that had tax withheld under §1445(a) gets a credit against its §1446 liability. Reg. §1.1446-3(c)(2).

## Step 4 — Partnership ECI withholding (I.R.C. §1446 and §1446(f))

### §1446 — foreign partner's distributive share of ECI
- Applies whether or not the income is actually distributed.
- Both domestic and foreign partnerships must withhold on a foreign partner's distributive share of ECI.
- Rate: the highest applicable rate for that partner's category (e.g., 21% for a corporate partner; the highest individual rate for an individual partner).
- In tiered structures, the withholding obligation can be pushed down to the lowest-tier partnership with proper documentation from the upper-tier partnership.

### §1446(f) — sale of a partnership interest
- The **buyer** (transferee) must withhold **10%** of the amount realized on the sale.
- Exceptions (per Reg. §1.1446(f)-2): the seller certifies non-foreign status via affidavit, or the partnership's net gain that would be ECI is less than 10% of total net gain.
- If the transferee fails to withhold, the partnership itself must withhold from future distributions to that transferee. I.R.C. §1446(f)(4).

## Step 5 — Documentation reference

| Form | Used for |
|---|---|
| W-8BEN | Foreign individual claiming treaty benefits (or certifying foreign status generally) |
| W-8BEN-E | Foreign entity claiming treaty benefits (or certifying foreign status generally) |
| W-8ECI | Payee certifies income is effectively connected with a U.S. trade or business |
| W-8IMY | Intermediary or flow-through entity, often with underlying W-8BEN(-E)/W-9s attached |
| W-8EXP | Foreign government or other exempt entity under §892 |
| Form 8233 | Nonresident individual claiming a treaty exemption on compensation for personal services |

## Step 6 — Compute and report

- Withholding is generally on the **gross** amount of the payment (Reg. §1.1441-3(a)), though a corporation may reduce dividend withholding based on a reasonable estimate of available earnings and profits — no withholding is required on a distribution that isn't paid from available E&P.
- The withholding agent must deposit withheld tax with a Federal Reserve or authorized bank (I.R.C. §6302), file an annual **Form 1042**, and issue a **Form 1042-S** to each foreign recipient.
- The withholding agent is **personally liable** for any amount required to be withheld, regardless of another party's failure to withhold or advice received from counsel. I.R.C. §1461.

### GL / book treatment for the withholding agent
When explaining the mechanics to finance/accounting staff, distinguish two very different situations:
- **Withholding done correctly (the normal case):** the withheld amount is a **conduit**, not a liability or expense of the withholding agent. The full gross payment (e.g., 100% of an interest payment) is the withholding agent's real expense, driven by the underlying obligation (loan terms, dividend declared, etc.) — that doesn't change based on withholding. Of that gross amount, the net portion goes to the foreign payee and the withheld portion goes to the IRS; both are just different destinations for the same cash outflow. Any "withholding tax payable" account on the withholding agent's books between accrual and remittance is a short-lived clearing account — the withheld funds were always the foreign payee's income, collected at the source, never the withholding agent's own money.
- **Withholding done incorrectly (under-withheld or not withheld at all):** if the IRS later assesses the withholding agent directly under §1461 — which it can do regardless of whether the foreign payee ever pays its own substantive tax liability — that assessment is a **real liability and expense** to the withholding agent, not a conduit. This is especially costly if the full gross amount was already paid out to the foreign payee with nothing withheld, since recovering the shortfall from the foreign payee after the fact may not be practical.
- The substantive tax liability on the income itself always belongs to the foreign payee (I.R.C. §871/§881); the withholding agent's liability under §1461 is a separate, parallel *collection* liability that only becomes a real cost to the withholding agent if withholding wasn't done correctly.

## Delivering the answer

- **Be concise.** Walk through only the steps that actually matter for the fact pattern at hand, and state each briefly. Skip or compress any step, factor, or regime that clearly doesn't apply rather than narrating why it doesn't — e.g., if the payment obviously isn't real property, don't walk through the FIRPTA test to rule it out; just note the payment type and move to the regime that fits. Don't restate the six-factor test or the documentation table in full unless a specific factor or form is actually in question. The goal is the shortest path to a defensible conclusion, not a comprehensive recitation of the whole framework every time.
- **Default:** walk through the applicable steps conversationally, showing which regime applies and why, the rate determination, and documentation needed, ending with a clear bolded conclusion (withholding required or not, at what rate).
- **If the user asks for a memo or something to save/share:** produce it as a Word document — read `/mnt/skills/public/docx/SKILL.md` first, then structure as Facts → Analysis → Conclusion (Withholding Required/Rate/Documentation), citing the same Code/Reg sections used in chat.
- **If the user asks for a workpaper, spreadsheet, or a rate/dollar calculation:** produce it as an Excel workbook — read `/mnt/skills/public/xlsx/SKILL.md` first. Structure: a Facts tab (payment type, payee status, documentation on file, treaty details as blue input cells) and an Analysis tab with formula-driven regime classification, rate lookup, and a gross-up/withholding-amount calculation (`=gross_amount * rate`), with a yellow-highlighted final withholding amount cell.
- Always include a caveat that this is an educational walkthrough of the mechanical rules, not a filing position — treaty eligibility (limitation on benefits provisions), FATCA overlay, state withholding, and entity classification elections can all change the outcome, and any treaty rate used should be verified against the current treaty text before being relied upon. Recommend review by a senior tax professional before finalizing.

## Reference material

See `references/examples.md` for two fully worked examples from the source material: the $120 dividend paid through a foreign partnership (look-through withholding across three differently-situated partners), and the same fact pattern once the partnership becomes a withholding foreign partnership (shifting the obligation to the entity).
