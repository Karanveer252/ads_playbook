# 04. Tracking: Pixel, Conversions API, dedup, test events, attribution

Meta claims below come from `/workspace/ads/playbook/META_LEAD_ADS_RESEARCH_2026-10-19.md` (official pages read
2026-10-19 through a reader proxy). **Not re-verified on 2026-11-05.** Event names, UI labels and attribution
windows change often; confirm in Events Manager before relying on them. URLs in `SOURCES.md`.

## 1. Hard gate (universal)
A launch is NO-GO until a **real test submission** through the real form produces:
- Website conversion location: a **Lead** event (or the chosen conversion event) visible in Events Manager for
  the right Pixel/dataset, with the time noted.
- Instant form: a test lead visible in the leads center / connected CRM.

Record: date, time, timezone, who submitted, which URL/form, what Events Manager showed.
Tag the test lead so it is excluded from results (questionnaire I2).

> Warning: on Domin8te's site, a test submit sends a real email to the inbox and fires a real Lead.
> There is no dry-run mode on the form handler (`/workspace/leads/item7-same-day-lead-response-2026-11-05/RESULT.md`, gap 4).
> Tell the inbox owner before testing.

## 2. Pixel checklist
- [ ] Pixel/dataset ID belongs to the advertiser's own Business Manager.
- [ ] Base code on every funnel page (landing, form, thank-you state). PageView seen in Events Manager.
- [ ] Conversion event fires **only on success** (after the form submit is accepted), not on button click or page load.
- [ ] Event parameters are sensible and current (e.g. no stale category names from an old offer). Minor, not blocking.
- [ ] Recent event history checked: when did the conversion event last fire? A conversion event with no recent history may make delivery slow; note it. [Meta warning behavior: unverified]
- [ ] Unexplained past conversion events resolved as tests or real before reading results.
- [ ] Optional: a form-start event and a thank-you URL event so drop-off is visible (playbook "Tracking").

## 3. Conversions API and deduplication
- Meta recommends running CAPI **alongside** the Pixel (O32).
- Dedup: browser and server events share the same `event_name` and `event_id`. Check Events Manager shows
  both sources and that duplicates are being deduplicated.
- Event match quality (EMQ) is scored from recent activity; email and click ID (fbc) are listed as high-priority
  parameters (O33). Send only with lawful consent, hashed per Meta developer docs.
- **Policy:** missing CAPI, dedup or EMQ is a **must-fix flag** for the approver, not an automatic blocker
  (Domin8te playbook rule 6). Write the state in the pass/fail sheet row 19.
- CAPI for CRM / qualified-lead optimization needs much higher lead volume than small test budgets produce (O30).
  Do not plan around it for small tests.

## 4. Test events
- Use Events Manager **Test events** where available to watch the event arrive live. [UI name volatile]
- After the test, confirm the event also appears in the normal event history (not just the test view).
- Remove or tag test data per questionnaire I2.

## 5. UTMs
- Every ad: `utm_source=meta&utm_medium=paid&utm_campaign=<campaign name>&utm_content=<ad name>`.
  (Pattern from `PRELAUNCH_2026-11-04.md`; adjust to the advertiser's analytics convention.)
- Ad names in Meta match `utm_content` exactly.
- Click each link once before launch; confirm the page opens with tags intact on mobile.
- If the page passes UTMs into hidden form fields or a booking tool, confirm they arrive with the test lead.

## 6. Attribution
- Choose one attribution setting per launch and write it in every report. Domin8te own account uses
  **7-day click + 1-day view** (playbook).
- Results across ad sets with different settings are not comparable (O25).
- Per local research: 7-day view and 28-day view windows were removed from the Ads Insights API on
  2026-01-12, and click-through counts link clicks only (O25, O28, O29). **Volatile; re-check.**
  API pulls asking for removed windows return blanks.

## 7. Own-account status (last known)
See `01-account-specific-domin8te-own.md` §5. On 2026-11-04 the Lead code existed with an eventID for dedup,
but no Lead event had fired in 7 days and no real test was run. Row 18 = **FAIL** until a test passes.
