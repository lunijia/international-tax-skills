# Worked Examples — CFC Determination

Use these to sanity-check your reasoning on a new fact pattern or to explain a step to the user by analogy. All examples assume calendar-year individuals/entities and that the entity being tested is otherwise a foreign corporation (Step 1 satisfied).

---

**Example 1 — 11 equal U.S. individuals**
11 unrelated U.S. individuals each own 9.09%. No one reaches the 10% U.S. Shareholder threshold. No U.S. Shareholders exist.
**Result: Not a CFC.** *Takeaway: must clear the 10% U.S. Shareholder test before aggregation even matters.*

**Example 2 — Same 11 individuals, held through a U.S. partnership**
The partnership itself owns 100% and is a U.S. person; a U.S. partnership can be a U.S. Shareholder in its own right. It owns >50%.
**Result: CFC.** *Takeaway: ownership through a U.S. entity counts as that entity's own direct ownership.*

**Example 3 — 10 equal U.S. individuals**
Each owns exactly 10% — each clears the U.S. Shareholder threshold. Combined = 100% > 50%.
**Result: CFC.** *Takeaway: 10% is the inclusive threshold (≥10%, not >10%).*

**Example 4 — One 50% owner + nine 5.56% owners**
Only the 50% owner clears 10% and is a U.S. Shareholder. The nine small owners are below 10% and don't count toward aggregation. U.S. Shareholders collectively own only 50%, not more than 50%.
**Result: Not a CFC.** *Takeaway: the aggregation threshold is strictly >50%, not ≥50%.*

**Example 5 — 50/50 foreign joint venture**
One U.S. owner at 50%, one foreign owner at 50%. U.S. Shareholder ownership tops out at exactly 50%.
**Result: Not a CFC.** *Takeaway: a true 50/50 JV structure is generally not a CFC.*

**Example 6 — Indirect ownership stacking**
A U.S. individual owns 100% of a foreign corp, which owns 8.33% of the target. The individual also owns 8.33% of the target directly. Direct (8.33%) + indirect (8.33%, from the foreign corp chain) = 16.67% combined.
**Result: U.S. Shareholder (≥10%), and CFC** if that's the only/controlling ownership. *Takeaway: direct and indirect ownership add together for the same person.*

**Example 7 — Parent/child attribution**
Parent owns 9% directly (below 10% alone). Child owns 4%. Under §958(b)/§318 family attribution, Parent is deemed to also own Child's 4%: Parent's total = 13%.
**Result: Parent is a U.S. Shareholder.** *Takeaway: family attribution can push someone over the 10% line even though their direct stake alone doesn't.*

**Example 7b — Aggregation between two related U.S. Shareholders (avoiding double-count)**
Individual A owns 7% of ForCo directly. A's spouse owns 5% of ForCo directly. Remaining 88% held by unrelated foreign individuals.

- Under §958(b)/§318 spousal attribution, A is deemed to also own spouse's 5%: A's individual total = 12%. Spouse is deemed to also own A's 7%: spouse's individual total = 12%.
- Both A and spouse independently clear the 10% U.S. Shareholder threshold (Step 4).
- **Aggregation (Step 5):** the group's actual underlying stock is only 7% + 5% = 12% — the same 12% shows up in both individuals' attributed totals, so summing "12% + 12% = 24%" would double-count it. The correct aggregate U.S. Shareholder ownership for the >50% test is **12%**, not 24%.

**Result: Not a CFC** (12% ≤ 50%). *Takeaway: individual U.S. Shareholder status (Step 4) is tested per-person including attribution, but group aggregation (Step 5) should reflect actual underlying shares held by the group, not the sum of each member's overlapping attributed percentage.*

**Example 8 — Constructive ownership overriding indirect ownership**
USCo owns 10% of ForCo1 (single class of stock; remaining 90% held by unrelated foreign shareholders). ForCo1 owns 51% of ForCo2 (remaining 49% held by one unrelated U.S. shareholder). Assume ForCo1 itself is not a CFC.

- *Indirect ownership (§958(a)) alone:* USCo's indirect stake in ForCo2 = 10% × 51% = 5.1%. Under this measure alone, USCo is below 10% and not a U.S. Shareholder; U.S. Shareholders (just the 49% owner) hold only 49% — not a CFC.
- *Constructive ownership (§958(b)):* Because ForCo1 owns more than 50% of ForCo2, ForCo1 is treated under §958(b)(2)/§318(a)(2)(C) as owning 100% of ForCo2. USCo's deemed ownership = 10% × 100% = 10%.
- *Reg. § 1.958-2(f)(2) rule:* where constructive ownership produces a larger figure than indirect ownership for the same block, constructive ownership controls. So USCo counts as a 10% U.S. Shareholder.
- Aggregate U.S. Shareholders: USCo (10%) + other U.S. shareholder (49%) = 59% > 50%.

**Result: CFC.** *Takeaway: always compute both indirect and constructive ownership for chains through a >50%-owned intermediate entity — constructive ownership can create a CFC that the indirect-ownership math alone would miss.*

**Example 9 — §951B FCFC overlay**
Foreign Parent (FCo) owns 75% of USCo. USCo owns 25% of FSub; FCo directly owns the remaining 75% of FSub.

- *Classic CFC test on FSub:* only U.S. ownership is USCo's 25%, which is below the >50% aggregate threshold (and depends on whether USCo alone clears things) — under §957, FSub is generally **not a CFC**.
- *§951B overlay:* Because USCo is a U.S. subsidiary of a foreign parent (FCo) that also directly owns the rest of FSub, USCo may be a "foreign-controlled U.S. Shareholder" and FSub may be an "FCFC." If so, USCo must still include its pro rata share of FSub's subpart F income and net CFC tested income (NCTI) — **even though FSub is not a CFC under the traditional test.**

**Result: Not a CFC under §957, but a §951B inclusion can still apply to USCo.** *Takeaway: §951B is a separate, additional check — never stop the analysis just because the classic test says "not a CFC" if there's a foreign parent sitting above a U.S. entity in the chain.*

---

## Quick-reference memory aid

- **Test 1 (who's a U.S. Shareholder):** any U.S. person owning ≥10% of vote or value (direct + indirect + constructive, using the larger of indirect/constructive per block).
- **Test 2 (is it a CFC):** do those U.S. Shareholders, combined, own >50% of vote or value?
- **Formula:** CFC = U.S. Shareholders (10%+ owners) collectively own >50%.
- **Don't forget:** §958(b)(4) repeal/reinstatement timing (tax years beginning after 12/31/2025), and the independent §951B/FCFC check.
