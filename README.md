# ad-launch-playbook-skill

A **docs-only** agent skill for launching Meta (Facebook + Instagram) lead ads safely: a mandatory
pre-launch questionnaire, a pass/fail checklist, a build/readback/go-no-go gate, and monitoring with
kill and rollback rules.

It contains no code, no credentials and no automation. It does **not** authorize any live Meta change.
Every launch, pause, budget or targeting change still needs a named human approver's yes for that exact change.

## How to use
1. Load `SKILL.md` as an agent skill (YAML frontmatter + recipe), or read it as a human runbook.
2. For each launch, fill `references/02-prelaunch-questionnaire.md`. Any CRITICAL gap blocks the launch.
3. Work through steps 3 to 9 in `SKILL.md` using the matching `references/` files.
4. Fill `references/03-prelaunch-passfail-checklist.md`, get the approver's GO, then monitor with
   `references/09-monitoring-kill-rollback.md`.

## Universal vs account-specific
| What | Where | Applies to |
|---|---|---|
| Universal defaults | `references/00-universal-defaults.md` and files 02 to 11 | Any advertiser |
| Domin8te own-account policy | `references/01-account-specific-domin8te-own.md` | `act_1700335297732498` only, plus marked Domin8te agency-wide rules |
| Client settings | A filled questionnaire per launch | That client only |

Own-account defaults (ages 28 to 60 hard, Advantage+ audience off, FB + IG only, the DRAFT CPL rules) are
examples of account policy. They are not applied to clients without questionnaire evidence.

## Status of key items (2026-11-05)
- **CPL policy (own account only): DRAFT, not enabled, not automated.** CPL > CA$40 rolling 7 days per ad set =
  soft notify only; CA$80+ with zero leads over 8 days per ad set = hard pause (draft; lead definition
  unresolved; no live authority).
- **Same-day lead response: not automated.** The playbook requires manual validation of the intake path and a
  named owner.
- Meta claims come from local research dated 2026-10-19 and were not re-verified this turn; see `references/SOURCES.md`.

## Publishing note
- Proposed repo name: `Karanveer252/ad-launch-playbook-skill`, **private** by default.
- Not created, not pushed. No git repo exists in this folder. Publishing needs Karan's approval.
- Before publishing, read `QA_REVIEW.md` (publish blockers) and decide whether the own-account file and the local
  path citations should stay in a shared copy. `_work/` holds build-time files and should not be published.

## Files
See `INVENTORY.md`.

## 2026-11-05 additive update (owner-selected Hormozi review items)
Five additions, all additive (no existing line removed or reordered). Details and line ranges: `CHANGELOG.md`.
1. Customer economics: gross profit after fulfillment, allowable CAC/CPL, or unknown with a named human risk signoff (questionnaire H8 to H14).
2. Offer strength: dream outcome, proof, time delay, effort, guarantee, lead-magnet check (questionnaire B6 to B11).
3. Qualified-lead tracking: lead states S0 to S4 and a qualifying sequence (questionnaire I7 to I10; `10` §6).
4. Sales path: opt-in → contact → book → show → close with a named owner per stage (questionnaire M; `10` §7).
5. Hook/proof checks: call-out, first five seconds, approved proof, ad-page match, CTA (`06` §8).

Kill rules, DRAFT status and authority safeguards are unchanged. Still docs only; nothing published.
