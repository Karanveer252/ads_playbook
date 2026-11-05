# 09. Monitoring, reporting, kill rules, rollback

Nothing in this file pauses, edits or reallocates anything by itself. Every action is a **recommendation** to
the approver. No monitoring routine or alarm runs unless it is separately approved and scheduled (none is set
up by this package). Domin8te: don't run daily checks while no ads are spending (`brand/lessons.md` 2026-10-23).

## 1. Daily check while spending (Domin8te practice: about 9 AM CT)
Pull real numbers only. No projections presented as results.
- Delivery: status of every campaign/ad set/ad; rejected or stuck in review.
- Spend vs daily cap and month-to-date.
- Spend, impressions, reach, frequency, CTR, CPC, landing page views, leads, CPL.
- Breakdowns: age, gender, region, placement/platform, device.
- Link clicks vs landing page views (gap = slow page or junk clicks).
- Leads in Meta vs leads actually in the inbox/CRM.
- Attribution setting stated.

## 2. Same-day red flags (raise to the approver the same day)
Source: Domin8te playbook (Part B and rule 13). These are flags, not automatic actions. Thresholds are
Domin8te working rules, not Meta rules.
| Flag | Applies to |
|---|---|
| Any spend in a placement not chosen in questionnaire F3 (own account: any non-FB/IG spend) | All |
| Any age band > 40% of spend outside the intended buyer | Domin8te-managed |
| Any 65+ targeting or heavy 65+ skew | Domin8te-managed |
| > 60% of spend in a placement without matching creative | All |
| Click-to-landing-page-view under 50% | All |
| Frequency > 3 | All |
| CPM jump > 50% day over day (ignore if the denominator is trivial) | All |
| Spend with zero leads at the launch's written threshold | All |
| Soft: frequency > 2 with CTR falling or CPL rising for 3 days → recommend creative refresh | All |

"Learning limited" does not switch these off.

## 3. Kill / pause rules
### Own account (`act_1700335297732498`): DRAFT CPL policy, NOT ENABLED, NOT AUTOMATED
Source: `DRAFT_CPL_PAUSE_POLICY_2026-11-05.md`.
1. Per ad set, CPL > CA$40 over rolling 7 days → **soft notify Karan only. No pause.**
2. Per ad set, CA$80+ spent with **zero leads across 8 days** → **hard pause** (the only pausing rule). DRAFT:
   lead definition unresolved; no automation; no live pause authority. Today this means: report it to Karan with
   the numbers and a recommended action; Karan decides.
- No CA$40 hard pause. No 4-day rule. Both removed.

### Clients
- Use the thresholds written in questionnaire H5/H6, approved by the client and Karan.
- If none were written: recommend only, and flag spend with zero leads to the approver. Do not borrow the
  own-account CPL draft as the client's rule.

### Ad-level candidates (recommend only)
From the 2026-10-19 playbook: an ad with about 2x target CPL in spend and 0 leads, or bottom-quartile CTR after
about 1,000 impressions, is a pause candidate. Label as Domin8te working practice (no controlled data).

## 4. Edit discipline
- Don't edit in the first 3 days unless a red flag shows wasted spend (wrong audience/placement). Fix those fast,
  with approval.
- Batch edits; each significant edit can restart learning (O22).
- Judge lead quality over 14 to 21 days at small budgets (playbook rule 2).
- One change at a time; log it; wait for fresh data (about 7 days) before the next (`CLIENT_AD_CHECKLIST.md` (c)).
- Never call a winner before about day 7 of clean data. Call small samples small.

## 5. Rollback
| Situation | Rollback (after approval) |
|---|---|
| Wrong targeting/placement live | Pause the ad set; fix in a copy or edit; read back; reactivate with approval |
| Wrong creative/copy live | Pause the ad; fix; re-review; reactivate |
| Overspend | Pause or lower budget; report numbers |
| Tracking broken | Pause or keep running is the approver's call; report the gap and the data at risk |
| Policy rejection | Don't resubmit blindly; fix the cause; re-review |
Never permanently delete campaigns, ad sets, ads, audiences or conversions. Pause or archive.
Record the before/after state of every rollback.

## 6. Reports
- Weekly (and on request): spend, results, CPL, pacing vs plan, breakdowns, flags raised and decisions taken,
  attribution setting, data date range and timezone.
- Every number from a pull file; cite the file.
- Creative comparisons inside one ad set are **directional**.
- After the run: write the campaign memory entry (what ran, setup, real results, flags, verdict, approver's
  words, one-line lesson).

## 7. Lead-state and sales-path reporting (2026-11-05 additive, owner-selected Hormozi review items) [ADD #1, #3, #4]
Sections 1 to 6 above are unchanged. §3 kill/pause rules keep their exact DRAFT wording and status; nothing here
pauses, edits or enables anything.
- **Daily check addition (while spending):** S0 Meta-reported, S1 contactable, S2 engaged, S3 qualified and S4
  customer counts, plus P2 contacted, P3 booked, P4 showed, P5 closed (or the confirmed route's stages), from the
  logs named in questionnaire I8 and M5. Stages with no data are written "no data", not zero.
- **Weekly report addition:** the same counts, and cost per stage where both numbers are real. All-in CAC only
  when S4 > 0, labelled incomplete if any cost is missing. Compare against questionnaire H12/H13 only if they
  were computed; otherwise say "economics unknown (H14 signoff on file)". Small samples stay labelled small.
- **Quality flag (recommend only, not automated):** if the launch wrote a quality flag (`07` §6 template), raise
  it to the approver the same day it trips. It never pauses anything and is separate from the §3 rules.
- The own-account lead definition stays **UNRESOLVED**; these counts do not choose it.
