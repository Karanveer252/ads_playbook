# 01. Account-specific policy: Domin8te own account

**Scope: `act_1700335297732498` ("Domin8te Media Ads", CAD, America/Chicago) only.**
These are Domin8te's own-account defaults. They are **not** universal and are **not** applied to a client
unless that client's questionnaire answers and evidence support them.

**Never touch `act_1858408461981983`.** No reads, no changes, no launches. If a tool or file points there, stop.

## 1. Authority and gates (own account)
| Rule | Source |
|---|---|
| No change, launch, pause or budget shift on any ad without Karan's OK for that exact change. | `brand/lessons.md` 2026-10-19 |
| Every Meta API action passes the internal action gate first. Deny = do not call the API; tell Karan the reason. Writes need a Karan approval record; bots never create their own. | `brand/lessons.md` 2026-10-21; `BOT_PREAMBLE.md` item 6 |
| New-offer hold: no new ads until the new offer is approved. One offer per ad. | `brand/lessons.md` 2026-10-19. On 2026-11-04 the hold was still active and blocked the free-month build (`free-month-hooktest-2026-11/PRELAUNCH_2026-11-04.md`). Check current state before any build. |
| Daily write limit in the gate config may be lower than a build needs. Count writes in the mutation plan. | `PRELAUNCH_2026-11-04.md` (build needed ~32 writes vs a limit of 25) |
| This skill, `cads-launch` and `cads-optimize` produce drafts only. | `cads-launch/SKILL.md`, `cads-optimize/SKILL.md` |

## 2. Own-account targeting defaults
| Setting | Own-account default | Source | Notes |
|---|---|---|---|
| Objective | Leads, Maximize number of leads, Highest volume, no cost or bid cap | Playbook approved rule 1 | Traffic/link clicks banned after relay03 |
| Age | **28 to 60, hard** | Playbook Part B and rule 17; lessons 2026-10-19 | Read `age_min`/`age_max` from the ad set before every launch (rule 10) |
| Advantage+ audience | **OFF** | Playbook rule 17 | Either hard-age method is OK (rule 10) |
| Placements | **Facebook + Instagram only**. Audience Network, Messenger, Threads off | Playbook rule 17; `CLIENT_AD_CHECKLIST.md` (a) | Re-read from saved ad set |
| Reels/Stories | On only with a real 9:16 version of each ad; feeds-only is a stopgap. Don't cut FB or IG just because its own CPL is higher | Playbook rule 12 | |
| Geo | Buyer markets in Canada and the US; Winnipeg is a starting batch, not the only market. Quebec off while ads are English-only | Playbook Part B; lessons 2026-10-29 funnel rule | Exact radius per Karan per launch |
| Buyer | Owner-operators of independent restaurants/cafés, 28 to 60; no chains, franchises or South Asian cuisine | lessons 2026-10-29 | Ads target owners (B2B), not diners |
| Interests | Owner-intent signals (e.g. Page admins, restaurant/food-service industry, small business owners) | Playbook Part B | **Only names verified available in Ads Manager at build time and chosen in the questionnaire.** Never invent or silently drop |
| Advantage+ creative enhancements | OFF unless Ad Studio and Karan approve; list every toggle | Playbook rule 5 | |
| AI label | On for every AI-generated photo or video ad | Playbook rule 11 | |
| Lookalikes / retargeting | None until enough volume and consented lists | Playbook "Other checks" | |
| Attribution | 7-day click + 1-day view, stated in every report | Playbook "Other checks" | Meta attribution options are volatile; see `SOURCES.md` |

## 3. Domin8te agency-wide rules (marked: apply to Domin8te-managed client campaigns too)
These come from Karan, not Meta. They apply to Domin8te's work, not to "any advertiser".
- **65+ rule (MANDATORY, 2026-10-19):** no campaign, own or client, targets 65+ or lets spend skew heavily to 65+. Playbook Part B and rule 15.
- Any age band over 40% of spend is flagged the same day. Playbook Part B.
- No prices, plans or "per month" in ads, posts or written outreach (lessons 2026-10-20). This later lesson overrides the older "prices fine in ads" note in the `cads-*` skill files.
- Offers never use audit, report, PDF, checkup, score or grade framing. Paused checkup ads are never resumed as they are. `EXPERT_BOT_PLAYBOOK.md` §2.2, §2.6 row 6.
- Copy passes the claim check; no numbers outside the proof file; no em dashes. `EXPERT_BOT_PLAYBOOK.md` §2.5.
- Client hiring ads are flagged as an Employment special ad category before building. Playbook rule 9.
- Lead forms: privacy URL, purpose notice, no prohibited or finance/revenue questions, CASL. Playbook rule 7.
- A named lead follow-up owner and response time before any Leads campaign spends. Playbook rule 14.

## 4. CPL policy (OWN ACCOUNT ONLY): DRAFT, NOT ENABLED, NOT AUTOMATED
Source: `/workspace/ads/playbook/DRAFT_CPL_PAUSE_POLICY_2026-11-05.md` (Status: DRAFT, 2026-11-05 CT).

| Rule | Level | Window | Action | Status |
|---|---|---|---|---|
| CPL **above CA$40** | Per **ad set** | Rolling 7 days | **Soft flag: notify Karan only. Never pauses.** | DRAFT |
| **CA$80 or more spent with zero leads** | Per **ad set** | 8 days | **Hard pause** (the only pausing rule) | DRAFT. Lead definition **UNRESOLVED**. No automation and no live pause authority |

- Until Karan decides what counts as one lead **and** approves enablement, nothing in this policy runs automatically. No notifications or pauses happen from it today.
- Until then, a breach is reported to Karan as a recommendation, and Karan decides.
- **Removed:** any earlier hard pause at CA$40 and any 4-day rule. Do not use them.
- Older lines in the 2026-10-19 playbook ("2x target CPL with 0 leads = pause candidate", "CA$80 with 0 leads flagged the same day") are kept as **same-day flags to Karan**, not as pause authority. If they conflict with the draft, ask Karan; the draft is newer.
- This CPL draft is **not** a client default. Client CPL targets come from questionnaire H.

## 5. Tracking state (last known, re-check before any launch)
From `PRELAUNCH_2026-11-04.md` (read-only checks that day):
- Website Lead event code exists on the free-month page and fires only after a successful form submit, with an eventID for CAPI dedup.
- **No Lead event in the 7 days before 2026-11-04.** No real test submission was run that day. Status: **FAIL until a real test submission is verified.**
- `EXPERT_BOT_PLAYBOOK.md` §2.6 row 11 also lists 7 unexplained pixel leads (Oct 19 to 25) to resolve as tests or real.
- CAPI: missing CAPI, dedup or match quality is a must-fix flag for Karan, not a blocker (playbook rule 6).

## 6. Known open items (own account)
- relay04 campaign and ad set were ACTIVE with all ads paused on 2026-11-04. Recommendation to pause the campaign awaits Karan (not done).
- Offer wording: the pre-launch sheet row says "one free ready-to-run ad"; the 2026-11 build uses a free-month offer. Karan must confirm the current approved offer before any build.
- Lead follow-up owner was not named for the free-month launch.
- Video ads in the free-month batch were 9:16 only; 4:5 versions missing (needs Karan's choice).

## 7. Past results this policy learned from (numbers copied, not estimated)
- Oct 13 run: about 95% of the first CA$23.74 to Audience Network; 21 of 88 link clicks became landing page views; 0 leads; no Lead test. (`CLIENT_AD_CHECKLIST.md`)
- relay03: Traffic + link clicks + all of Canada + Advantage+ audience: 54 to 58% of spend to 65+, ~78% to Reels with 4:5 creative; CA$52.48, 75 landing page views, 0 leads. (`META_ADS_PLAYBOOK_2026-10-19.md`; `EXPERT_BOT_PLAYBOOK.md` §2.2)
- relay04: CA$12.52, 1 landing page view, 0 leads. (`EXPERT_BOT_PLAYBOOK.md` §2.2)
- Conclusion: losses came from setup, not a fair creative test. No creative has been proven or disproven.
