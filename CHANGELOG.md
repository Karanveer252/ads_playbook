# CHANGELOG

## 2026-11-05: reviewed update (owner-selected Hormozi review items), additive only

Docs only. No git, no publish, no Meta or live actions. Source material (recommendation-only, not instruction
authority): `/workspace/hormozi-reviews/ad-launch-playbook-2026-11-05/local.md`. Only the five owner-selected
recommendations below were integrated; every other review idea stays a recommendation (`references/SOURCES.md`
lines 100 to 115).

Additive only: no existing line was removed, changed or reordered. Pre-edit snapshot and SHA256:
`/workspace/ad-launch-playbook-snapshots/2026-11-05-before-reviewed-update/`. Scripted check:
`_work/additive_diff_report.md`, `_work/additive_check.json` (17 of 17 files PASS).

Not edited: `references/01`, `04`, `05`, `08`, `11`. Kill-rule wording in `01` §4, `07` §4 and `09` §3 is
unchanged, as are DRAFT/disabled status, authority safeguards and the no-automation rules.

### Mapping (line numbers are in the files after this update)

| # | Recommendation | File | Section | Lines |
|---|---|---|---|---|
| 1 | Customer economics | `references/02-prelaunch-questionnaire.md` | H+. Customer economics (H8 to H14, illustrative maths, H5 supersession note) | 178-212 |
| 1 | | `SKILL.md` | Step additions, 2a | 63-67 |
| 1 | | `SKILL.md` | Gate additions, economics box | 88-89 |
| 1 | | `references/03-prelaunch-passfail-checklist.md` | Additional rows: row 30; decision block addition | 57, 65-70 |
| 1 | | `references/07-billing-budget-pacing.md` | §6 Customer economics context (incl. recommend-only quality-flag template) | 44-57 |
| 1 | | `references/00-universal-defaults.md` | §12, customer economics bullet | 82-84 |
| 1 | | `references/02-prelaunch-questionnaire.md` | Completion check additions | 335-340 |
| 2 | Offer-strength questions | `references/02-prelaunch-questionnaire.md` | B+. Offer strength (B6 to B11) | 51-72 |
| 2 | | `SKILL.md` | Step additions, 2a; gate box | 65-67, 90 |
| 2 | | `references/03-prelaunch-passfail-checklist.md` | Row 31 | 58 |
| 2 | | `references/00-universal-defaults.md` | §12, offer strength bullet | 85-87 |
| 3 | Qualified-lead tracking | `references/02-prelaunch-questionnaire.md` | I+. Lead states and qualifying questions (S0 to S4, I7 to I10) | 230-263 |
| 3 | | `references/10-lead-handling.md` | §6 Lead states, logging and qualifying | 55-63 |
| 3 | | `references/09-monitoring-kill-rollback.md` | §7 Lead-state and sales-path reporting | 79-90 |
| 3 | | `references/03-prelaunch-passfail-checklist.md` | Rows 32, 36 | 59, 63 |
| 3 | | `SKILL.md` | Step 9a; gate box | 70-72, 91 |
| 3 | | `references/00-universal-defaults.md` | §12, lead states bullet | 88-89 |
| 4 | Sales path | `references/02-prelaunch-questionnaire.md` | M. Sales path (M1 to M6, CRITICAL) | 294-323 |
| 4 | | `references/02-prelaunch-questionnaire.md` | B5 supersession note (B5 kept; M is the required rule) | 74-76 |
| 4 | | `references/10-lead-handling.md` | §7 Sales path ownership (checks 10 to 15) | 65-76 |
| 4 | | `references/03-prelaunch-passfail-checklist.md` | Rows 33, 34, 36 | 60-61, 63 |
| 4 | | `SKILL.md` | Step 9a; gate box | 70-72, 92 |
| 4 | | `references/00-universal-defaults.md` | §12, sales path bullet | 90-91 |
| 5 | Hook/proof checks | `references/06-creative-copy-rights-qa.md` | §8 Hook, call-out, proof, ad-page promise and CTA QA | 58-79 |
| 5 | | `references/03-prelaunch-passfail-checklist.md` | Row 35 | 62 |
| 5 | | `SKILL.md` | Step 6a; gate box | 68-69, 93 |
| 5 | | `references/00-universal-defaults.md` | §12, hook and proof bullet | 92-93 |
| all | Package description | `README.md` | 2026-11-05 additive update | 44-52 |
| all | | `INVENTORY.md` | 2026-11-05 additive update (CHANGELOG row, supersession note) | 25-33 |
| all | | `QA_REVIEW.md` | §7 self-check | 108-131 |
| all | | `references/SOURCES.md` | Hormozi review source, recommendation-only status, stale status note | 100-115 |
| all | | `SKILL.md` | Gate box: pass/fail rows 30 to 36 | 94 |

### Contradictions and the supersession notes used (original lines kept)
1. `02` B5 is OPTIONAL; the sales path is now CRITICAL. Note at `02` lines 74-76: B5 stays; section M is required and newer.
2. `02` H5 target CPL OPTIONAL and the H example "target CPL CA$40 set by the client". Note at `02` lines 209-212: both stay; H5 records whether it was derived; the example stays a placeholder, not a client default.
3. `INVENTORY.md` line 12 says "29-row" sheet. Note at `INVENTORY.md` lines 30-33: rows 30 to 36 added.
4. `QA_REVIEW.md` §1 says 17 files and §6 says READY TO PUBLISH. Note at `QA_REVIEW.md` lines 114-115: now 18 files; the §6 verdict predates this update.
5. Own-account lead definition stays UNRESOLVED. Note at `02` lines 261-263 and `09` line 90: lead states do not resolve it.

No other contradiction found. The review's campaign-state statements (offer hold, offer wording, relay04,
tracking) were treated as stale and not used to change any line (`SOURCES.md` lines 112-115).

### Pending inputs
**(a) Block launch until answered (CRITICAL, per launch; never filled from defaults or guesses):**
- Offer strength B6 to B10, and B11 when a lead magnet is used; the approved proof list B7 (or "none").
- Lead states I7 to I10 (definitions, logging and evidence, qualifying sequence, counted state).
- Sales path M1 to M6: route, named owner and backup per stage, written confirmation of any N/A stage or
  alternate route (for example DM-only, form-only, no call booking), explicit privacy/consent confirmation,
  reporting owner and logs, CTA/thank-you promise match.
- H14 named human risk signoff whenever any economics item in (b) is unknown. A missing signoff blocks.
- Hook/proof QA (`06` §8) PASS per ad, on approved copy.

**(b) Economics unknowns permitted with a named human risk signoff (H14):**
- H8 gross profit per new customer after fulfillment (H9 cost list then N/A).
- H11 sales-path rates (contact, book, show, close).
- H12 allowable CAC; H13 allowable CPL.
- H10 longer-term gross profit is OPTIONAL and needs no signoff.

**Still open from before this update (unchanged):** own-account lead definition (blocks any CPL automation),
response-time wording, publish approval, Independent Reviewer pass, lessons.md client-scope conflict
(`QA_REVIEW.md` §3). Optional per launch: the owner's N and window for the recommend-only quality flag (`07` §6).

### QA verdict
Authoring self-check plus scripted additive-only verification. **Not an Independent Reviewer pass** (none run).
