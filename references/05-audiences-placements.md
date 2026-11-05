# 05. Audiences, exclusions, placements

Inputs come from the questionnaire (C, D, E, F). This file says how to set and verify them.
Meta mechanics cited from local research (2026-10-19, not re-verified today; `SOURCES.md`).

## 1. Pick the audience model first
| Model | Typical use | Targeting notes |
|---|---|---|
| B2B owner-operator | Selling to business owners (Domin8te own ads) | Owners are a small slice of the public. Cheapest leads pull toward the general public, so owner-intent signals and hard controls matter. Keep the audience big enough to deliver. |
| Consumer / diner | A café or restaurant promoting to locals | Local radius around the real address. Usually broad (no stacked interests). Check spend skew against the client's real customers. |
| Recruiting | Hiring ads | Employment special category: age, gender, postal-code and some interest targeting unavailable in the US and Canada (O42). See `11`. |

Don't mix models in one ad set.

## 2. Location
- [ ] Set from questionnaire C2/C3. Write the radius or city list and why.
- [ ] Exclusions from C4 applied (e.g. regions the copy's language doesn't fit).
- [ ] Location is a hard control in Meta (O13).
- [ ] Domin8te own account: Canada and US markets; never only one city; Quebec off while ads are English-only (`01`).

## 3. Age and gender
- Only from questionnaire D with evidence. No universal age rule.
- Domin8te-managed campaigns: no 65+ targeting and no heavy 65+ skew (agency rule, `01` §3).
- To **enforce** a range, use a hard control:
  - Advantage+ audience **off**, with age min/max set; or
  - Advantage+ audience on with "Further limit the reach of your ads", "Use as a suggestion" **unticked** (O13; UI wording volatile; O10 says this may switch Advantage+ off in Advantage+ leads campaigns).
- Read `age_min`, `age_max` and the Advantage+ audience state from the saved ad set before launch.
- Report spend by age daily either way.
- Unverified (non-official N2): minimum age control inside Advantage+ audience may cap at 25. Don't rely on it.

## 4. Interests, behaviours, job titles
- Only names chosen in questionnaire E **and** shown available in Ads Manager at build time.
- Record each name exactly, who checked, when. If one is unavailable or "combined": stop, tell the owner, and
  re-ask E. Never substitute a guessed name and never drop it silently.
- Prefer a few broad signals over many stacked narrow ones at small budgets.
- Advantage+ detailed targeting may expand interests beyond selections; it does not apply to location, age or
  gender (O14). Record the setting Ads Manager shows. Whether it can be turned off for Leads optimization:
  **unverified**.
- Domin8te own account owner-intent examples (Page admins, restaurant/food-service industry, small business
  owners) are **illustrative**; availability must be checked each build.

## 5. Custom audiences, lookalikes, exclusions
- Customer lists only with a recorded consent basis (CASL/PIPEDA in Canada; applicable US rules).
- Lookalikes from customers, not form submitters (O3). Advantage+ lookalike is on by default and can expand (O15).
- Domin8te own account: no lookalikes or retargeting until enough volume and consented lists exist.
- Exclusions to consider: existing leads/customers (if consented list exists), staff, the advertiser's own
  followers when acquiring new people. Optional.

## 6. Audience size
- Record Meta's estimated size at build. Small local budgets need enough room to deliver. [Practice: no fixed number]
- Before widening an audience because of high frequency, check where the repeats come from (placement vs
  audience). [Lesson] Oct 13 run: repeats came from Audience Network, not the audience.

## 7. Placements
- Set from questionnaire F3. Write which placements are on.
- **Domin8te own account: Facebook + Instagram only.** Audience Network, Messenger, Threads off. For clients
  this is a Domin8te recommended starting point (`CLIENT_AD_CHECKLIST.md` (a)) that the client must choose in F3.
- Meta recommends Advantage+ placements and reports lower costs from them (O18, O19). Restricting is a choice
  with a cost tradeoff; record the reason.
- Reels/Stories on only when a real 9:16 version of each ad exists. Feeds-only is a stopgap.
- Within the chosen platforms, don't cut a placement just because its own CPL is higher; judge the ad set total (O19).
- Higher-intent instant forms deliver only on mobile FB and IG Feeds (O2). Volatile.
- After saving: reopen the ad set and confirm the placement list. Check the placement spend breakdown daily.

## 8. Readback rows (copy into the build readback, `08`)
| Setting | Questionnaire value | Read from saved ad set | Match? |
|---|---|---|---|
| Locations / radius | | | |
| Exclusions | | | |
| age_min / age_max | | | |
| Advantage+ audience | | | |
| Gender | | | |
| Interests (each) | | | |
| Detailed targeting expansion | | | |
| Placements (each) | | | |
| Estimated audience size | | | n/a |
