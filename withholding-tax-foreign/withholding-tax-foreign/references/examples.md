# Worked Examples — Withholding Tax Determination

Both examples are built around the same underlying fact pattern from the source material, showing how the withholding obligation shifts depending on the foreign partnership's status.

---

## Example 1 — Look-through withholding on a payment to a foreign (non-withholding) partnership

**Facts:** USCo, a domestic corporation, makes a dividend payment of $120 to XYZ, a foreign partnership organized in Country X. XYZ has three equal partners — X, Y, and Z — each entitled to a $40 share of the dividend (1/3 of $120).

- **X** is a resident of Country X, which has no U.S. tax treaty.
- **Y** is a U.S. resident.
- **Z** is a resident of the Netherlands, which has a treaty with the U.S. reducing dividend withholding to 15%.

**Analysis:** Because XYZ is a foreign partnership without a withholding agreement (not a withholding foreign partnership), the withholding agent (USCo, or its agent) must look through XYZ to the individual partners and apply each partner's own withholding treatment to their allocable share:

| Partner | Status | Share | Rate | Withheld |
|---|---|---|---|---|
| X | Country X resident, no treaty | $40 | 30% (statutory) | $12 |
| Y | U.S. resident | $40 | 0% (no §1441 withholding on U.S. persons) | $0 |
| Z | Netherlands resident, treaty | $40 | 15% (treaty rate) | $6 |

**Total withheld: $18.** XYZ (the partnership) actually receives a net payment of $120 − $18 = **$102**.

*Takeaway: a payment to a foreign partnership is not withheld on as a single blended rate — the withholding agent must determine each partner's status and apply that partner's own rate to their allocable share, assuming adequate documentation is provided per partner.*

---

## Example 2 — Same facts, but XYZ is a withholding foreign partnership (WFP)

**Facts:** Same as Example 1, except XYZ has since entered into a withholding agreement with the IRS, making it a withholding foreign partnership, and has notified USCo of that status with the necessary documentation.

**Analysis:** Because XYZ is now a WFP, the withholding obligation shifts entirely to XYZ. USCo is no longer required to withhold under I.R.C. §1441 on this payment — USCo pays the **full $120** to XYZ with no withholding at the point of payment.

XYZ itself then becomes responsible for withholding on its partners' shares, at the time and under the procedures that would apply to a domestic partnership with foreign partners (i.e., XYZ withholds when each partner's distributive share of FDAP income is required to be recognized under U.S. tax timing principles, not necessarily only when cash is actually distributed).

*Takeaway: WFP status doesn't eliminate withholding — it relocates who is responsible for it (and potentially when it happens), shifting the compliance burden from the original U.S. payor to the foreign partnership itself. This is analogous to how a domestic partnership is never itself subject to §1441 withholding on payments it receives, but becomes the withholding agent for its own foreign partners.*

---

## Quick-reference rate table

| Regime | Rate | Citation |
|---|---|---|
| FDAP statutory (no treaty/no documentation) | 30% | I.R.C. §§1441, 1442; confirmed current per 2025 Instructions for Form 1042 |
| FDAP with valid treaty claim | Treaty rate (varies — verify current rate, don't assume) | Applicable treaty; Reg. §1.1441-6 |
| Scholarship/fellowship (non-services) | 14% | I.R.C. §871(c) |
| FIRPTA general rule | 15% of amount realized | I.R.C. §1445(a) |
| FIRPTA — domestic partnership disposing of USRPI (foreign partners' share) | 21% of allocable gain | I.R.C. §1445(e)(1) |
| §1446 ECI (partnership) | Highest applicable rate per partner type (e.g., 21% corporate partner) | I.R.C. §1446 |
| §1446(f) sale of partnership interest | 10% of amount realized | I.R.C. §1446(f) |
| FATCA (separate regime — not covered by this skill's logic yet) | 30% | I.R.C. §§1471-1474 |
