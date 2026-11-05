# 00. Universal defaults (any Meta launch, any advertiser)

These apply to every launch run with this skill, own account or client. They do **not** include
Domin8te's own-account targeting choices (ages, Advantage+ state, placements, CPL rules). Those are in
`01-account-specific-domin8te-own.md` and are never copied to a client without questionnaire evidence.

Labels used: **[Meta doc]** = from an official Meta page as summarized in local research dated 2026-10-19,
not re-verified on 2026-11-05 (see `SOURCES.md`). **[Lesson]** = learned from a Domin8te run. **[Practice]** =
working practice, not a Meta rule, no controlled data.

## 1. Account access and permissions
| # | Default | Why |
|---|---|---|
| 1.1 | Confirm the exact ad account ID in writing before any work. Write it at the top of every launch file. | Wrong-account launches can't be undone cleanly. |
| 1.2 | Client accounts: the client owns the ad account, Page, Instagram account, Pixel/dataset and payment method. Domin8te gets partner access through the client's Business Manager. | Client keeps ownership; access can be revoked cleanly. [Practice] |
| 1.3 | Use the lowest access level that does the job. Read-only for audits and monitoring. | Least privilege. |
| 1.4 | Record who holds admin, who can approve spend, and who gets billing alerts. Store names and roles, never passwords or tokens. | |
| 1.5 | Any account on a "do not touch" list is excluded from every read and write. | |

## 2. Objective and optimization
| # | Default | Source |
|---|---|---|
| 2.1 | Lead campaigns use the **Leads** objective, optimizing for the real conversion event (website Lead or instant form lead). | [Meta doc] objective → conversion location → performance goal (O34) |
| 2.2 | Do not optimize for link clicks or landing page views when a working conversion event exists. | [Lesson] relay03: Traffic/link clicks, CA$52.48, 0 leads |
| 2.3 | Small budgets: **Maximize number of leads** + **Highest volume** bid strategy, no cost cap or bid cap. | [Meta doc] goal-based bidding works best with 50 to 100+ weekly conversions (O24) |
| 2.4 | "Learning limited" is expected at small budgets. It is not a reason to edit on its own. | [Meta doc] O20, O21 |
| 2.5 | Qualified-lead or value optimization only after CRM Conversions API and the volume Meta asks for exist. | [Meta doc] O7, O30. Treat as volatile. |

## 3. Structure
- Small budgets: one campaign, one ad set, 3 to 5 ads. Don't split budget across ad sets unless the budget can feed each one. [Meta doc] O20 (avoid high ad volumes); [Practice] the 3 to 5 count.
- Test one variable at a time (creative OR copy OR audience OR form). Label in-ad-set comparisons **directional**; Meta's A/B test tool is the only method Meta treats as reliable. [Meta doc] O41.
- Batch edits. Targeting, creative, optimization event, a new ad, bid strategy, a 7+ day pause, or a large budget change can restart learning. [Meta doc] O22.

## 4. Targeting (universal part only)
- Location, radius and exclusions come from the advertiser's real service or delivery area (questionnaire C).
- **Age, gender and interests are never assumed.** Each needs a questionnaire answer and evidence (questionnaire D, E).
- If an age range must be enforced, it has to be a **hard control**, and it must be read back from the saved ad set. Meta treats age ranges inside Advantage+ audience as suggestions (O13). Two ways to make it hard: turn Advantage+ audience off, or use "Further limit the reach of your ads" with "Use as a suggestion" unticked. [Meta doc] O13; UI wording volatile.
- Interests must be confirmed available in Ads Manager at build time. Removed interests can stop delivery. [non-official] N3, N5 to N7.
- Check the estimated audience size before launch. Too narrow at a small budget means slow, expensive delivery. [Practice]

## 5. Placements
- Placements are a **questionnaire choice** (C, F). Write down which are on and why.
- After saving, re-read the placement list from the ad set. Check the placement spend breakdown daily. Meta can add placements through defaults and some edits. [Lesson] Oct 13 run: ~95% of the first CA$23.74 went to Audience Network.
- Only run a placement you have native creative for (e.g. 9:16 for Reels/Stories). [Meta doc] O36, O37.

## 6. Creative and copy
- Every ad has a feed version (4:5) and a vertical version (9:16) inside safe zones. 1:1 optional. [Meta doc] O37, O38.
- Headline and CTA say what the offer is and who it's for. [Meta doc] O3.
- List every Advantage+ creative enhancement and its state before go-live. Generative enhancements off unless the advertiser approves. [Meta doc] O35, O36.
- Only claims the advertiser can prove. No invented stats, reviews or results.
- Asset rights confirmed for every image, video, music track, voice and logo.

## 7. Tracking
- Hard gate: a real test submission produces a Lead event in Events Manager (or a real test lead in the instant-form leads center).
- Conversions API with deduplication (shared event_id) is recommended. If missing, flag it to the approver as must-fix; whether it blocks is the approver's call. [Meta doc] O32, O33.
- UTMs on every ad, with `utm_content` = ad name.
- Attribution setting written in every report. Don't compare results across different settings. [Meta doc] O25.

## 8. Budget, billing, pacing
- Confirm account currency before entering a budget.
- Daily cap from the approved monthly test budget (monthly / 30). Meta can spend above the daily budget on a given day. [Practice; Meta-side daily overspend behavior: verify current Meta wording]
- Working payment method confirmed before launch.

## 9. Approvals and change control
- Nothing goes live, pauses, or changes budget or targeting without the named approver's yes for that exact change.
- Build PAUSED. Read back. Then the approver turns it on (or approves the exact activation).
- Log every change: date, time, timezone, what, who approved.
- No permanent deletion. Pause or archive instead.

## 10. Lead handling
- A named person owns follow-up, with a written response time, before any spend.
- Test that a lead actually lands where that person will see it.
- Run ads during hours someone can respond, or say so in the form's follow-up promise. [Meta doc] O4.
- Do not assume an automated responder exists. See `10-lead-handling.md`.

## 11. Monitoring
- Daily check while spending. Report only real pulled numbers. Call small samples small.
- Kill and rollback rules are written per launch before spend; they are **recommendations** to the approver unless an approved automation exists (none does in this package).

## 12. Additions (2026-11-05 additive, owner-selected Hormozi review items)
Sections 1 to 11 above are unchanged. These pointers add to them:
- **Customer economics [ADD #1] (adds to §8).** Every launch records gross profit after fulfillment per new
  customer, sales-path rates, allowable CAC and allowable CPL (questionnaire H8 to H13), or marks them unknown
  with a named human risk signoff (H14). Revenue or price is never used as profit. [Practice]
- **Offer strength [ADD #2].** Value questions (dream outcome, proof, time delay, effort, guarantee) and a
  lead-magnet check are answered before building (questionnaire B6 to B11). No invented proof; no automatic
  guarantee. [Practice]
- **Lead states [ADD #3] (adds to §10).** Meta-reported, contactable, engaged, qualified and customer counts are
  kept apart (questionnaire I7 to I10; `10` §6). [Practice]
- **Sales path [ADD #4] (adds to §10).** Opt-in → contact → book → show → close with a named owner at each stage,
  or a confirmed alternate route; privacy/consent confirmed explicitly (questionnaire M; `10` §7). [Practice]
- **Hook and proof checks [ADD #5] (adds to §6).** Call-out, first five seconds, proof from approved evidence,
  ad-page promise match and CTA are checked per ad (`06` §8). The check does not write copy. [Practice]
