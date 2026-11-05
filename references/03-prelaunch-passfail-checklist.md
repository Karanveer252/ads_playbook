# 03. Pre-launch pass/fail checklist

Generalized from `EXPERT_BOT_PLAYBOOK.md` §2.6 (Domin8te pre-launch check) and `CLIENT_AD_CHECKLIST.md`.
Any **FAIL** = no launch. **N/A** needs a one-line reason. Settings are read from the **saved ad set**, not
the summary or review screen.

Rows marked **[OWN POLICY]** apply only to Domin8te's own account (`act_1700335297732498`). For client
launches, they are **[OPTIONAL]** and only apply if the client's questionnaire chose them.

Who does what (Domin8te roles, adapt for other teams): builder fills it; a second person verifies settings by
reading the ad set; an independent reviewer confirms; the approver signs off.

## Sheet

```
Campaign:                     Ad account:                 Date (TZ):
Questionnaire file:           Questionnaire status: READY FOR CHECKLIST (must be)
```

| # | Area | Check | Pass means | Status | Evidence |
|---|---|---|---|---|---|
| 1 | Account | Correct account | Ad account ID matches questionnaire A1. `act_1858408461981983` not touched. | | |
| 2 | Account | Access and ownership | Operator role confirmed; client owns assets (client launches). | | |
| 3 | Gate | Approval to build | Approver OK for the build recorded. **[OWN POLICY]** new-offer hold lifted; internal gate allows the action; approval record exists from Karan's main bot. | | |
| 4 | Objective | Objective / goal | Matches questionnaire G. Lead campaigns: Leads objective, real conversion event; not Traffic or link clicks. **[OWN POLICY]** Maximize number of leads, Highest volume, no cap. | | |
| 5 | Placements | Placement list | Matches questionnaire F3, re-read from saved ad set. **[OWN POLICY]** FB + IG only; Audience Network, Messenger, Threads off. | | |
| 6 | Audience | Geo | Locations, radius, exclusions match questionnaire C. | | |
| 7 | Audience | Age | Matches questionnaire D (with evidence) or unrestricted by choice. Read `age_min`/`age_max` and Advantage+ audience state. Domin8te-managed: no 65+ targeting. **[OWN POLICY]** 28 to 60 hard, Advantage+ audience off. | | |
| 8 | Audience | Interests | Matches questionnaire E. Each interest shown available at build (name, date). None invented or dropped. Expansion setting recorded. | | |
| 9 | Audience | Size | Estimated audience size recorded from Ads Manager. | | |
| 10 | Special category | Category | Questionnaire L1 answered; category declared if needed; targeting adjusted. | | |
| 11 | Offer | Offer wording | Matches the owner-approved offer (B1). One offer per ad. Claims true at launch. Domin8te: no prices; no audit/report/PDF/checkup/score/grade; no "free trial"; no done-for-you. **[OWN POLICY]** exact current Karan-approved offer wording. | | |
| 12 | Copy | Copy QA | Spelling, CTA names the offer and audience. Domin8te: claim check passes, no em dashes, locked lines verbatim. | | |
| 13 | Creative | Formats | Every ad has 4:5 and 9:16 inside safe zones. | | |
| 14 | Creative | Creative review | Reviewer PASS. Domin8te: creative scorecard verdict SHIP and Independent Reviewer PASS. | | |
| 15 | Creative | AI settings | Every Advantage+ creative toggle listed with state; generative ones off unless approved. AI label on for AI assets. | | |
| 16 | Rights | Asset rights | Every asset in questionnaire J1 has a rights holder and consent where needed. | | |
| 17 | Links | Destination + UTMs | Every link opens the right page on mobile with UTMs intact; `utm_content` = ad name. | | |
| 18 | Tracking | Lead event | Real test submission produced the Lead event in Events Manager (or a lead in the leads center): date, time, who. **Hard gate.** | | |
| 19 | Tracking | CAPI / dedup | CAPI state and dedup noted. Missing = flagged to approver (approver decides if blocking). | | |
| 20 | Tracking | Old events | Unexplained past events resolved as test or real. **[OWN POLICY]** the 7 unexplained pixel leads from Oct 19 to 25. | | |
| 21 | Form | Lead form compliance | Privacy URL, purpose notice, no prohibited/finance questions, CASL where relevant. | | |
| 22 | Landing | Page | Loads fast on mobile data; form works; thank-you state shows. | | |
| 23 | Leads | Intake + owner | Test lead arrived where the named owner sees it. Owner and response time written. No claim of automated response. | | |
| 24 | Budget | Currency + amount | Account currency confirmed; budget matches questionnaire H; payment method works. | | |
| 25 | Budget | Structure | Small budgets: one ad set, 3 to 5 ads, no split (unless approver chose otherwise in writing). | | |
| 26 | Budget | Red lines | Kill/flag thresholds written for this launch. **[OWN POLICY]** DRAFT CPL policy (CA$40 rolling 7d soft notify; CA$80+ with zero leads over 8 days = hard pause, draft only, not automated). | | |
| 27 | Monitoring | Owner + schedule | Monitoring owner and first check time set; red-flag list attached. Note: no routine runs unless separately approved and scheduled. | | |
| 28 | Build | Readback | Every object built PAUSED and read back; readback table attached (`08`). | | |
| 29 | Approver | Final yes | Approver saw this filled sheet and said yes for this exact launch, with date and time. | | |

### Additional rows (2026-11-05 additive, owner-selected Hormozi review items)
Rows 1 to 29 above are unchanged. These rows are part of the same sheet; any FAIL = no launch.

| # | Area | Check | Pass means | Status | Evidence |
|---|---|---|---|---|---|
| 30 | Economics [ADD #1] | Customer economics | Questionnaire H8 to H13 answered with sources, using gross profit after fulfillment (not revenue or price); **or** each unknown item covered by an H14 named human risk signoff (name, role, date/time). Own-account CA$40 not used as a client figure. | | |
| 31 | Offer [ADD #2] | Offer strength | B6 to B10 answered (B11 if a lead magnet is used). Proof listed in B7 has source, date and permission; "none" is acceptable. Any guarantee has the owner's written confirmation. Nothing invented. | | |
| 32 | Leads [ADD #3] | Lead states | S0 to S4 defined for this launch (I7); logging, logger and evidence named (I8); qualifying sequence written with no finance or prohibited questions (I9); counted state recorded (I10). | | |
| 33 | Sales path [ADD #4] | Owners per stage | Questionnaire M filled: route stated; named owner and backup for every stage that applies; every N/A stage confirmed in writing by the client (Karan, own account). | | |
| 34 | Sales path [ADD #4] | Privacy / consent | M4 confirmed explicitly by the client (Karan, own account): channels consented, consent basis, storage, access, retention. | | |
| 35 | Creative [ADD #5] | Hook / proof QA | `06` §8 table PASS for every ad: call-out, first five seconds, proof from B7 only, ad-page promise match, CTA matches the route in M. QA used approved copy only. | | |
| 36 | Reporting [ADD #3, #4] | Stage reporting | Report template has fields for S0 to S4 and P1 to P5 counts, owner of the report, and log sources (M5). | | |

Decision block addition (fill with the Decision block below):
```
Economics status: KNOWN (sources attached) | UNKNOWN with risk signoff (name, role, date/time)
Offer-strength notes shown to approver: yes | no
Sales path route: standard | alternate (confirmed by, date)
```

## Decision
```
Result: GO | NO-GO
FAIL rows:
N/A rows and reasons:
Approver:                 Timestamp (TZ):
Approval channel / message reference:
```
