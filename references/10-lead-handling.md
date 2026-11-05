# 10. Lead handling

## Status: same-day lead response is NOT automated
Evidence: `/workspace/leads/item7-same-day-lead-response-2026-11-05/RESULT.md` (2026-11-05). Verdict:
**NOT DONE as automated end-to-end.** The same-day rule exists as training, brief, form copy and a KPI only.
No live trigger exists; nothing fires on a new lead. Only a synthetic, never-sent draft was produced.

Do not claim, imply or plan around an auto-responder, auto-notification or same-day bot reply. What this
playbook requires instead: **validate the intake path and the named human owner by hand before spend.**

## 1. Before spend: intake and ownership validation
| # | Check | Pass means |
|---|---|---|
| 1 | Intake path written | Where a lead goes: e.g. website form → email inbox; instant form → leads center / CRM integration |
| 2 | Test lead arrived | A tagged test submission arrived at that destination (date, time, who saw it) |
| 3 | Access confirmed | The named owner can open that inbox/leads center/CRM today |
| 4 | Owner named | One person owns follow-up (plus a backup) |
| 5 | Response time written | One wording, agreed by the owner, matching the form's promise |
| 6 | Hours | After-hours and weekend handling written; consider ad scheduling to hours someone can respond (O4) |
| 7 | Approval path | Who approves replies (Domin8te: Karan approves every send) |
| 8 | Logging | Where each lead and reply are logged by hand |
| 9 | Consent | Contact only for the stated purpose; CASL consent basis for email/SMS (`11`) |

Any FAIL = pass/fail sheet row 23 FAIL = NO-GO.

## 2. Domin8te own-account intake (known state, 2026-11-05)
From the RESULT.md file and its evidence:
- Website form handler emails the Domin8te inbox only. It also writes consent and CAPI logs.
- It does **not** write the lead log or pipeline file, and does **not** notify any bot.
- There is no mailbox connector for the inbox; the pipeline bot's email is off.
- No DM conversation tools exist in the current publishing integration.
- No dry-run mode: a public test submit sends a real email and a real Lead event.
- After-hours/weekend SLA is not coded.
- Two response-time wordings exist: "same business day" (Pipeline Manager profile) and "within 1 business day"
  (form success text, Community Engagement). **Pick one per launch and make the form match.**
- Every reply is a draft that Karan approves; no prices in writing.

So for an own-account launch: the owner checks the inbox by hand, drafts the reply, Karan approves, the reply is
sent, and the lead is logged by hand.

## 3. Client launches
- The client usually owns follow-up. Name the person and the response time in questionnaire I5.
- Confirm the client can see instant-form leads (leads center access or CRM integration) with a test lead.
- If Domin8te forwards leads, write who forwards, how and how fast. No automation assumed.

## 4. Lead definition and counting
- Use the definition in questionnaire I1. Exclude tagged tests, duplicates and spam (I2).
- Reconcile weekly: Meta lead count vs leads actually received.
- Own account: the lead definition for the DRAFT CPL policy is **unresolved** (`01` §4).

## 5. What would be needed for real automation (not in scope; not built)
From RESULT.md gaps: an intake → notification path, a mailbox connector, DM tools, a dry-run mode on the form
handler, lead log/pipeline wiring, and coded after-hours rules. Listed for planning only.

## 6. Lead states, logging and qualifying (2026-11-05 additive, owner-selected Hormozi review items) [ADD #3]
Sections 1 to 5 above are unchanged. Lead definitions come from questionnaire I7 to I10.
- Keep five counts apart: **S0 Meta-reported**, **S1 contactable**, **S2 engaged**, **S3 qualified**, **S4 customer**.
- Each state has one logger and one evidence source (pull file, inbox/CRM record, reply or call log, invoice/POS).
  Log by hand unless an approved integration exists (none is built; §5).
- Qualifying questions follow the order in questionnaire I (contact and consent, role/authority, fit, need,
  timing). Short form at a cold start; the rest at first contact. No revenue, income, finance or prohibited questions.
- Weekly reconcile (§4) adds: S0 vs S1 vs S2 vs S3 vs S4, with the reason for each drop where known.
- No response-time SLA is added. The owner's written I5 wording stays the only response-time promise.

## 7. Sales path ownership (2026-11-05 additive, owner-selected Hormozi review items) [ADD #4]
| # | Check | Pass means |
|---|---|---|
| 10 | Route written | Questionnaire M1: standard opt-in → contact → book → show → close, or the confirmed alternate route |
| 11 | Owner per stage | A named owner and backup for every stage that applies (M2) |
| 12 | N/A stages confirmed | Every stage marked N/A by route has the client's (Karan's, own account) written confirmation with date (M3). Never assume a client books calls |
| 13 | Privacy / consent | M4 confirmed explicitly: consented channels, consent basis, storage, access, retention |
| 14 | Reporting | Stage counts, reporter and log sources set (M5) |
| 15 | Promise match | CTA and thank-you message promise the same next step as the route (M6) |

Any FAIL here = pass/fail sheet rows 33 or 34 FAIL = NO-GO. For client launches the client usually owns P2 to P5
(§3); write the named people, not "the client".
