# 08. Naming, build, readback, approval, go/no-go

## 1. Naming
Pattern (adapt per advertiser; keep it consistent and URL-safe):
- Campaign: `<offer-or-test>-<YYYY-MM>` e.g. `free-month-hooktest-2026-11` (own-account example from `PRELAUNCH_2026-11-04.md`)
- Ad set: `<prefix>_<concept>` e.g. `fm_friend`
- Ad: `<prefix>_<concept>_<variant>` e.g. `fm_friend_flex`
- `utm_content` = ad name, exactly.
Rules: lowercase, hyphens/underscores only, no spaces, no client personal data in names.

## 2. Mutation plan (draft, before any write)
Write this before building. `cads-launch --draft` produces the same shape.
| Field | Content |
|---|---|
| Account | ID, confirmed against questionnaire A1 |
| Objects | Every campaign, ad set, creative, ad, upload to be created, with names |
| Settings | Objective, conversion event, goal, bid strategy, budget, schedule, geo, age, Advantage+ states, interests, placements, creative toggles |
| Status | All created **PAUSED** |
| Write count | Total API writes (uploads + objects). Check against any daily write limit. |
| Learning impact | Which existing objects (if any) change and whether learning restarts |
| Blast radius | What else in the account could be affected |
| Rollback | How to undo each step (pause, archive; never delete) |
| Owner / approver | Names |
| Approval | Exact plan approved by: name, timestamp |

Known tool gaps (Domin8te, 2026-11-04): the connected Meta tools could not set FB+IG-only placements,
upload video, or build multi-asset creatives directly; raw API calls were needed. Check current tool
capability before promising a build (`PRELAUNCH_2026-11-04.md`). Dynamic creative allows one ad per ad set,
which forces one ad set per concept; weigh that against the "don't split budget" rule.

## 3. Build
1. Confirm the approval for the exact plan exists (own account: internal gate allows it).
2. Build everything PAUSED.
3. Record every created object ID in the plan.
4. Stop on the first error; don't improvise a workaround that changes the plan without re-approval.

## 4. Readback (from the saved objects, not the summary screen)
| Object | Field | Planned | Read back | Match |
|---|---|---|---|---|
| Campaign | objective | | | |
| Campaign | status | PAUSED | | |
| Campaign | special ad category | | | |
| Ad set | optimization goal / event | | | |
| Ad set | bid strategy | | | |
| Ad set | daily or lifetime budget + currency | | | |
| Ad set | start / end | | | |
| Ad set | geo + radius + exclusions | | | |
| Ad set | age_min / age_max | | | |
| Ad set | Advantage+ audience state | | | |
| Ad set | interests / expansion | | | |
| Ad set | placements (each) | | | |
| Ad set | attribution setting | | | |
| Ad | creative IDs (4:5, 9:16) | | | |
| Ad | Advantage+ creative toggles (each) | | | |
| Ad | AI label | | | |
| Ad | URL + UTMs | | | |
| Ad | status | PAUSED | | |
| Ad | review status (approved / in review / rejected) | | | |

Any mismatch = fix (with approval) and read back again.

## 5. Go / no-go
- Fill `03-prelaunch-passfail-checklist.md`. Attach the questionnaire, mutation plan, readback and QA tables.
- Approver reviews and writes GO or NO-GO with timestamp.
- Activation is a separate approved change. Note the activation time; the first monitoring check is scheduled from it.

## 6. Where to save
- `<campaign folder>/QUESTIONNAIRE_<date>.md`, `PRELAUNCH_<date>.md`, `PLAN_<date>.md`, `READBACK_<date>.md`.
- Link the launch from the campaign memory file (Domin8te: `knowledge/ads/ADS_MEMORY.md`).
