---
name: ad-launch-playbook
description: >-
  When launching or pre-launching Meta (Facebook/Instagram) ads for Domin8te
  own account or any client: run the mandatory questionnaire, pass/fail
  checklist, build/readback/go-no-go, then monitor with kill/rollback rules.
---

# Ad launch playbook (Meta: Facebook + Instagram)

A reusable recipe for getting a Meta lead campaign from "idea" to "spending safely", then watching it.
It is a **docs-only playbook**. It does not authorize any live Meta change. Every create, edit, pause,
budget or targeting change needs a named human approver (for Domin8te: Karan) to approve that exact change.

Three layers of rules. Keep them apart:

| Layer | Applies to | File |
|---|---|---|
| Universal defaults | Any launch, any advertiser | `references/00-universal-defaults.md` |
| Domin8te own-account policy | `act_1700335297732498` only (plus a few Domin8te agency-wide rules, marked) | `references/01-account-specific-domin8te-own.md` |
| Client settings | One client launch | The filled questionnaire for that launch (`references/02-prelaunch-questionnaire.md`) |

Own-account defaults (ages 28 to 60 hard, Advantage+ audience off, FB+IG only, the DRAFT CPL rules) are
**not** carried over to clients automatically. Client settings come from questionnaire answers with evidence.

## Hard stops (check before step 1)

- Never read, change or launch anything in `act_1858408461981983`.
- No live writes from this skill. `cads-launch` and `cads-optimize` run in `--draft` only; any apply needs a
  separate, explicit human approval of the exact mutation plan.
- No secrets, tokens or credential paths in any launch file.
- No invented numbers. Unproven items are labelled **DRAFT**, **untested** or **no data**.
- Same-day lead response is **not automated**. Validate the intake path and the named owner by hand (step 9).

## Steps

1. **Scope the launch.** Name the advertiser, the ad account ID and the decision owner. If the account is
   `act_1700335297732498`, load `references/01-account-specific-domin8te-own.md`. If it is a client account,
   confirm in writing that Domin8te has access through the client's Business Manager (`references/00-universal-defaults.md` §1).
2. **Run the mandatory questionnaire.** Fill every question in `references/02-prelaunch-questionnaire.md`
   (examples are illustrative, not defaults). Any **CRITICAL** question unanswered, "unsure", or without the
   evidence it asks for = **BLOCKED**. Stop and ask. Do not fill gaps with guesses or own-account defaults.
3. **Check special categories and privacy.** Use `references/11-special-categories-privacy.md`. A hiring,
   housing, credit/financial or political ad changes what targeting is allowed: decide this before building.
4. **Verify tracking.** Pixel, test Lead event, CAPI and dedup state, attribution setting:
   `references/04-tracking-pixel-capi.md`. A verified Lead event from a real test submission is the hard gate.
5. **Plan audience and placements.** Location, radius, exclusions, age (with evidence), interests (verified
   available), placements: `references/05-audiences-placements.md`.
6. **QA creative, copy, links and rights.** Formats, safe zones, Advantage+ creative toggles, AI label,
   UTMs, form, asset rights: `references/06-creative-copy-rights-qa.md`.
7. **Set budget and pacing.** Currency, daily cap, billing, red lines: `references/07-billing-budget-pacing.md`.
8. **Draft the build, then read it back.** Name objects, write the mutation plan, build PAUSED only after
   approval, then re-read every setting from the saved ad set (not the summary screen):
   `references/08-naming-build-readback.md`.
9. **Validate lead handling.** Test lead reaches the named inbox or CRM; owner and response time are written
   down; nobody assumes an auto-responder exists: `references/10-lead-handling.md`.
10. **Fill the pass/fail sheet.** `references/03-prelaunch-passfail-checklist.md`. Save it with the launch as
    `PRELAUNCH_<YYYY-MM-DD>.md`.
11. **Go / no-go gate** (below). Only a human approver turns anything on.
12. **Monitor, report, roll back.** Daily checks, red flags, kill rules (recommend only), rollback:
    `references/09-monitoring-kill-rollback.md`.

### Step additions (2026-11-05 additive, owner-selected Hormozi review items)
Steps 1 to 12 above are unchanged. These run inside them:
- **2a. Offer strength and customer economics** (right after step 2, before building). Fill questionnaire B6 to
  B11 and H8 to H14 in `references/02-prelaunch-questionnaire.md`. Economics use **gross profit after
  fulfillment**, not revenue. Unknown economics are allowed only with a **named human risk signoff** (H14).
- **6a. Hook and proof QA.** Run `references/06-creative-copy-rights-qa.md` §8 on approved copy and approved
  evidence only. This QA does not write hooks or ad copy.
- **9a. Lead states and sales path.** Define lead states S0 to S4 and the qualifying sequence (questionnaire
  I7 to I10). Fill the sales path (questionnaire M: opt-in → contact → book → show → close, named owner per
  stage, alternate routes and privacy/consent confirmed explicitly). See `references/10-lead-handling.md` §6, §7.

## Go / no-go gate

**GO** only when all of these are true. Any one false = **NO-GO**.

- [ ] Questionnaire complete: zero CRITICAL gaps, evidence attached where asked.
- [ ] Pass/fail sheet: every row PASS or N/A with a reason. Zero FAIL.
- [ ] Correct account, read back from the build. `act_1858408461981983` untouched.
- [ ] Lead event verified with a real test submission (date, time, who).
- [ ] Settings read back from the saved ad set match the questionnaire (age, geo, placements, Advantage+ states, objective, budget).
- [ ] Lead intake tested by hand; named owner and response time written down.
- [ ] Budget, currency and billing confirmed by the client (client launches) or Karan (own account).
- [ ] Monitoring owner and first check time set; kill/rollback rules written for this launch.
- [ ] The approver saw the filled sheet and said yes for **this exact launch**, with date and time (CT for Domin8te).

**Gate additions (2026-11-05 additive, owner-selected Hormozi review items).** Also required for GO:
- [ ] Customer economics written (questionnaire H8 to H13, gross profit after fulfillment, sourced) **or** marked unknown with a named human risk signoff (H14). No price used as profit. Own-account CA$40 is not used as client economics.
- [ ] Offer strength answered (B6 to B10; B11 if a lead magnet). Proof and any guarantee come from approved, written sources only.
- [ ] Lead states S0 to S4 defined, with logging and evidence (I7 to I10).
- [ ] Sales path complete (questionnaire M): named owner at each stage; N/A stages and privacy/consent confirmed explicitly in writing.
- [ ] Hook/proof QA (`06` §8) PASS for every ad, using approved evidence only.
- [ ] Pass/fail rows 30 to 36 (`03`, additive table) PASS or N/A with a reason.

Record the decision at the bottom of the pass/fail sheet: `GO` or `NO-GO`, approver, timestamp, reasons.

## After launch

- Don't edit in the first days unless a red flag shows wasted spend; batch any edits (edits can restart learning).
- Every pause, budget or targeting change is a recommendation until the approver says yes.
- Log what changed, when, and why. Write the result and lesson into the campaign memory file.

## Where things live

- Package file list: `INVENTORY.md`. Source citations and unverified labels: `references/SOURCES.md`.
- Review status and open blockers: `QA_REVIEW.md`.
