# 07. Billing, budgets, pacing

All amounts come from questionnaire H. Numbers below are worked arithmetic or quoted Domin8te policy, not
benchmarks.

## 1. Before launch
- [ ] Read the ad account currency from the account itself. (Domin8te own account: CAD.)
- [ ] Budget entered in that currency and equal to what the owner approved.
- [ ] Payment method works and belongs to the right payer (client pays Meta directly on client accounts, per
      `brand/lessons.md` 2026-10-20 "clients pay their own ad spend").
- [ ] Billing alerts go to someone who will act on them.
- [ ] Account spending limit (if any) noted. Don't change it without the owner's OK.
- [ ] Start/end dates and timezone match questionnaire H7.

## 2. Daily cap and structure
- Daily cap = approved monthly test budget / 30 (Domin8te playbook "Budget pacing").
- Meta can spend more than the daily budget on a single day while keeping the weekly total in line
  (`CLIENT_AD_CHECKLIST.md` budget check). Exact Meta rule: confirm on Meta's current help page (unverified today).
- Small budgets: one ad set, no split. Splitting a small budget across ad sets starves each one.
- CBO (Advantage+ campaign budget) is described by Meta as best for 2+ ad sets (O23); with one ad set it adds nothing.
- Expect "Learning limited" at small budgets. Example arithmetic from local research: about 50 results a week
  are needed to exit learning (O20); at CA$10/day and a CA$40 CPL that is about 1 to 2 leads a week, far below 50.

## 3. Pacing during the month
- Weekly: month-to-date spend vs plan; days remaining; projected end-of-month spend (label as projection).
- Domin8te practice: reserve about 20% of the month's budget for the winner after week 2 (playbook). Untested
  as a rule; no data on whether it helps.
- Large budget changes can restart learning (O22). Batch them and get approval.

## 4. Red lines (write per launch)
| Account | Rule | Status |
|---|---|---|
| Domin8te own (`act_1700335297732498`) | Per ad set: CPL > CA$40, rolling 7 days = **soft notify Karan only, no pause** | DRAFT, not automated |
| Domin8te own | Per ad set: CA$80+ spent with **zero leads over 8 days = hard pause** | DRAFT only. Lead definition unresolved. No automation, no live pause authority; Karan approves any pause |
| Client | Thresholds from questionnaire H5/H6, approved by the client and Karan | Per launch |

No CA$40 hard pause and no 4-day rule. Those were removed (`DRAFT_CPL_PAUSE_POLICY_2026-11-05.md`).

## 5. Billing problems during a run
- Failed payment = delivery stops. Tell the payer the same day.
- Unexpected charges or spend outside the approved budget: stop recommending further spend, report to the
  approver with the numbers, wait for a decision.

## 6. Customer economics context (2026-11-05 additive, owner-selected Hormozi review items) [ADD #1, #3]
Sections 1 to 5 above are unchanged. The red lines in §4, including the own-account DRAFT CPL rows, keep their
exact wording and status.
- Budget decisions are read next to questionnaire H8 to H14: gross profit after fulfillment per new customer,
  sales-path rates, allowable CAC and allowable CPL. Revenue or price is never used as profit.
- If those are unknown, the launch needs the H14 named human risk signoff, and red lines stay the written H5/H6
  thresholds plus spend-with-zero-leads flags.
- The own-account CA$40 figure is a watch level for `act_1700335297732498` only. It is not a derived allowable
  CPL and is not a client rule.
- Optional red-line row template for client or own launches (**recommend only, not automated, never pauses**):

| Account | Rule | Status |
|---|---|---|
| (per launch) | Quality flag: spend with <N> Meta-reported leads (S0) and zero qualified (S3) / booked (P3) / closed (S4) over <window> → notify the approver | Recommend only. N and window written by the owner per launch; none is set by this package |
