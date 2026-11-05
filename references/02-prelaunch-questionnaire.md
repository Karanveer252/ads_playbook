# 02. Pre-launch questionnaire (MANDATORY before every launch)

Fill this for **every** launch: own account and every client, new campaigns and relaunches.
Save the filled copy with the launch as `QUESTIONNAIRE_<campaign>_<YYYY-MM-DD>.md`.

## How blocking works
- **[CRITICAL]** questions block launch. If a CRITICAL answer is blank, "unsure", "use the usual", or lacks
  the evidence asked for, the launch status is **BLOCKED**. Stop, ask the owner, and do not build.
- **[OPTIONAL]** questions improve the launch. A blank optional answer is written as "not set" and the
  universal default (`00-universal-defaults.md`) applies.
- Never fill a CRITICAL gap with a guess, with Domin8te own-account defaults, or with "what worked last time".
- Every example below is **ILLUSTRATIVE ONLY**. It shows the shape of a good answer. It is not a default,
  not a recommendation for this advertiser, and not data.

## Answer record header
```
Advertiser:                     Ad account ID:
Filled by:                      Date/time (TZ):
Answers confirmed by (owner):   Confirmation method (call / email / chat, with date):
Status: BLOCKED | READY FOR CHECKLIST
CRITICAL gaps (list):
```

---

## A. Business / client scope
> Illustrative: "Single-location independent café, owner-operated, one Page and one Instagram account, ad
> account owned by the café, Domin8te has partner access."

| # | Question | Level |
|---|---|---|
| A1 | Legal/trading name of the advertiser and the exact Meta ad account ID? | CRITICAL |
| A2 | Is this Domin8te's own account (`act_1700335297732498`) or a client account? (If the ID is `act_1858408461981983`: STOP, do not continue.) | CRITICAL |
| A3 | Who owns the ad account, Page, Instagram account, Pixel/dataset and payment method? | CRITICAL |
| A4 | What access does the operator have (role, via which Business Manager)? Confirmed in Business Settings? | CRITICAL |
| A5 | Who is the decision owner who approves launch, spend and changes? | CRITICAL |
| A6 | Any existing campaigns, ad sets or ads in this account that must not be touched or may conflict? | OPTIONAL |

## B. Offer
> Illustrative: "Weekday lunch set menu, available Mon to Fri 11 to 2, dine-in only, runs until end of
> month." (Example only. For Domin8te own ads, the offer must match the current Karan-approved offer.)

| # | Question | Level |
|---|---|---|
| B1 | What exactly is offered, in one sentence the advertiser approves? One offer per ad. | CRITICAL |
| B2 | Is the offer approved by the owner for this launch, with date? (Own account: is the new-offer hold lifted?) | CRITICAL |
| B3 | Conditions, limits, end date, scarcity claims. Are all of them true at launch and provable? | CRITICAL |
| B4 | Any words or framings the advertiser bans? (Domin8te: no prices in ads; no audit/report/PDF/checkup framing.) | CRITICAL |
| B5 | What happens right after someone responds (booking, call, visit, DM)? | OPTIONAL |

### B+. Offer strength (2026-11-05 additive, owner-selected Hormozi review items) [ADD #2]
B1 to B5 above are unchanged. These questions check whether the approved offer is worth paying to advertise.
Answer in the buyer's words where possible. "None" is a valid, honest answer for proof (B7) and guarantee (B10).
Never invent proof, results or a guarantee to fill a box. Nothing here adds a guarantee automatically.

> Illustrative only (not defaults, not claims, not data). Diner shape: "Dream outcome: a quick, filling lunch
> near work. Proof: 4 owner-approved Google reviews dated <date>. Time delay: served in about 10 minutes (owner's
> statement). Effort: walk in, no booking. Guarantee: none." B2B owner shape: "Dream outcome: more tables filled
> on slow nights. Proof: one approved case study with the client's written permission, dated <date>. Guarantee:
> none offered."

| # | Question | Level |
|---|---|---|
| B6 | **Dream outcome.** What result does the buyer want, in their words? Who said it (source, date)? | CRITICAL |
| B7 | **Proof / perceived likelihood.** List every approved proof asset (review, case study, photo, testimonial, number) with source, date and written permission to use it in ads. If none exists, write "none"; the ads then carry no proof claims. | CRITICAL |
| B8 | **Time delay.** How long until the buyer gets the result or first sign of it? Only what the advertiser can stand behind. | CRITICAL |
| B9 | **Effort / sacrifice.** What does the buyer have to do, give or risk to get it? | CRITICAL |
| B10 | **Guarantee / risk reversal.** None / conditional / unconditional / other. If any: the exact terms, and the owner's written confirmation they can honor it, with date. Never added by the builder or by a bot. | CRITICAL |
| B11 | **Lead-magnet check** (only if the offer is a free or low-cost item to get the opt-in). Is it a complete solution to one narrow problem? What next problem does it reveal that the core offer solves? (Domin8te: never audit, report, PDF, checkup, score or grade framing; B4 still applies.) | CRITICAL if a lead magnet is used; else N/A |

If B6 to B10 cannot be answered, the status is **BLOCKED** like any other CRITICAL gap. A weak answer is not a
block by itself; it is written down and shown to the approver at go/no-go.

**Supersession note (2026-11-05):** B5 ("What happens right after someone responds") stays above as written and
stays OPTIONAL as a free-text note. The sales path it describes is now **required** through section **M** below
(CRITICAL). Where B5 and M differ, M is the newer rule.

## C. Buyer vs consumer, location, radius, exclusions
Pick one. Each choice changes targeting, copy and lead handling.
- **(a) B2B owner-operator ad**: the reader is a business owner (e.g. Domin8te selling marketing to restaurant owners).
- **(b) Consumer / diner ad**: the reader is a customer of the business (e.g. a café promoting lunch to locals).
- **(c) Recruiting ad**: the reader is a job seeker. **Employment special ad category**; see `11-special-categories-privacy.md`.
- **(d) Other** (describe).

> Illustrative (b): "Diners within 8 km of the café address, exclude the neighbouring city across the river
> because they don't deliver there." Illustrative (a): "Owners in named Canadian and US metro areas, English
> only, Quebec excluded while copy is English-only."

| # | Question | Level |
|---|---|---|
| C1 | Which of (a) / (b) / (c) / (d)? | CRITICAL |
| C2 | Where can the advertiser actually serve? Address or cities/regions, and countries. | CRITICAL |
| C3 | Radius (for local), or list of cities/regions (for multi-market). Why that size? | CRITICAL |
| C4 | Location exclusions and why (areas not served, wrong language, competitor-only areas). | OPTIONAL |
| C5 | Location type wanted: people living in / recently in the area. (Meta option names are volatile; confirm in Ads Manager.) | OPTIONAL |
| C6 | Languages of the ads and of the people targeted. | OPTIONAL |

## D. Demographics and age (evidence required)
**No universal age rule exists.** An age range is set only when the owner gives one **and** says what it is
based on. Domin8te own account uses 28 to 60 hard (see `01`); that is not a client default.
Domin8te-managed campaigns also never target 65+ or allow heavy 65+ skew (agency rule, `01` §3).

> Illustrative evidence: "POS loyalty data: most members aged 25 to 54", "Instagram Insights follower age
> breakdown screenshot dated <date>", "the owner sells only to licensed business owners". "I think young
> people" is **not** evidence.

| # | Question | Level |
|---|---|---|
| D1 | Should age be restricted? Choose: (i) no restriction beyond Meta/legal minimums and Domin8te agency rules, (ii) a specific range. | CRITICAL |
| D2 | If (ii): the range, and the evidence (source, date, who provided it). No evidence = choose (i) or BLOCKED. | CRITICAL if D1 = (ii) |
| D3 | Must the range be **hard** (Advantage+ audience off, or "Further limit" with suggestion unticked) or may Meta treat it as a suggestion? | CRITICAL if D1 = (ii) |
| D4 | Gender restriction? Only with evidence and a lawful, non-discriminatory reason. Default: all genders. | OPTIONAL |
| D5 | Is this a special ad category (hiring, housing, credit/financial, social/political)? If yes, age/gender may be locked. | CRITICAL |

## E. Interests, job titles, broad targeting rationale
Owner-intent interests are **recommended** for B2B owner ads, but only by explicit choice, and only names
verified as available in Ads Manager at build time. Never invent interest names. Never silently drop one.

Pick one:
- **(a) Broad** (location + age only). Rationale required (e.g. small local area, consumer offer).
- **(b) Interests / behaviours** listed below, each verified available.
- **(c) Job titles / employers** (availability varies by region; verify).
- **(d) Custom audiences** (customer list or site visitors) with consent evidence.

> Illustrative (b), B2B: "Restaurant-industry interest and Page-admin behaviour, both checked available in
> Ads Manager on <date> by <name>." Illustrative (a), diner: "Broad. 8 km radius is already small; stacking
> interests would starve delivery."

| # | Question | Level |
|---|---|---|
| E1 | Which of (a) / (b) / (c) / (d), and why? | CRITICAL |
| E2 | If (b) or (c): exact names as shown in Ads Manager, who checked availability, and when. Any marked unavailable or combined? | CRITICAL if E1 = (b)/(c) |
| E3 | Allowed to let Meta expand interests (Advantage+ detailed targeting)? Record the setting actually shown. | OPTIONAL |
| E4 | If (d): list source, consent basis (CASL/PIPEDA in Canada; applicable US rules), upload owner. | CRITICAL if E1 = (d) |
| E5 | Estimated audience size shown at build (copy the number Meta shows, with date). | OPTIONAL (recorded at build) |

## F. Mandatory vs optional controls
For each control, mark MANDATORY (must be enforced and read back) or OPTIONAL (Meta may optimize).
> Illustrative: "Placements FB+IG only = MANDATORY; age = OPTIONAL suggestion; Reels = on only if 9:16 exists."

| Control | MANDATORY / OPTIONAL / N/A | Level |
|---|---|---|
| F1 Locations and exclusions | | CRITICAL |
| F2 Age range | | CRITICAL |
| F3 Placements (list: FB Feed, IG Feed, Reels, Stories, Audience Network, Messenger, Threads, WhatsApp) | | CRITICAL |
| F4 Advantage+ audience on/off | | CRITICAL |
| F5 Advantage+ creative enhancements (each toggle) | | CRITICAL |
| F6 AI-generated content label | | CRITICAL if any AI asset |
| F7 Ad schedule (business hours) | | OPTIONAL |
| F8 Language | | OPTIONAL |

## G. Objective and conversion
> Illustrative: "Leads objective, website conversion location, Lead event fired on the thank-you state of
> the booking form." Or: "Leads objective, instant form, Higher intent type."

| # | Question | Level |
|---|---|---|
| G1 | Business result wanted (leads, bookings, calls, messages, store visits, sales)? | CRITICAL |
| G2 | Campaign objective and conversion location (website, instant form, website + instant form, calls, messages). | CRITICAL |
| G3 | Exact optimization event and where it fires. Verified by a real test submission? (date/time/who) | CRITICAL |
| G4 | Instant form type if used (More volume / Higher intent / Rich creative; names volatile). | CRITICAL if instant form |
| G5 | Performance goal and bid strategy. Default: Maximize number of leads, Highest volume, no cap. | OPTIONAL |

## H. Budget and currency
> Illustrative: "CA$150 for the month, ad account currency CAD, client pays Meta directly by card, target
> CPL CA$40 set by the client." (Numbers are placeholders, not advice.)

| # | Question | Level |
|---|---|---|
| H1 | Ad account currency (read from the account, not assumed). | CRITICAL |
| H2 | Approved total budget and period, in that currency. | CRITICAL |
| H3 | Daily cap (default: monthly / 30) or lifetime budget with dates. | CRITICAL |
| H4 | Who pays Meta, and is the payment method working? | CRITICAL |
| H5 | Target cost per lead (or per result), set by the owner. "Unknown" is allowed; then monitoring uses spend-with-zero-leads flags only. | OPTIONAL |
| H6 | Kill/pause thresholds the owner wants recommended. (Own account: DRAFT CPL policy in `01` §4. Clients: written here.) | CRITICAL |
| H7 | Start date/time and end date/time (timezone). | CRITICAL |

### H+. Customer economics (2026-11-05 additive, owner-selected Hormozi review items) [ADD #1]
H1 to H7 above are unchanged. These questions say what a customer is worth to **this** advertiser, so a lead
cost can be judged against something real.

Rules:
- Use **gross profit after fulfillment costs**: what the business keeps from a new customer after the direct
  cost of delivering what was sold (food and labour for a restaurant; delivery or service time for an agency).
  **Revenue, price or plan fee is not gross profit.** Never enter a price as the profit figure.
- Every number needs a source (who gave it, date, how it was worked out). No invented figures, no figures
  borrowed from another client, no Domin8te own-account numbers.
- **"Unknown" is allowed** for H8 to H13, but only with a **named human risk signoff** in H14. An agent or bot
  cannot sign H14.
- The own-account CA$40 CPL watch level (`01` §4) is **not** a derived allowable CPL and is **not** a client
  rule. Do not copy it here.

| # | Question | Level |
|---|---|---|
| H8 | Gross profit per new customer after fulfillment costs, first 30 days (or the first purchase/visit), in the account currency. Source and method. Or "unknown". | CRITICAL (answer or "unknown" + H14) |
| H9 | Which fulfillment costs were subtracted (list them)? | CRITICAL if H8 is a number |
| H10 | Longer-term gross profit per customer (repeat visits or renewals), if the owner knows it, with source. Diner ads: average gross profit per guest or visit and the repeat-visit assumption, from the owner. | OPTIONAL |
| H11 | Known or estimated rates along the sales path (section M): lead to contact, contact to book, book to show, show to close (or the route's own stages). Source for each, or "unknown". | CRITICAL (answer or "unknown" + H14) |
| H12 | Allowable cost to acquire one customer (allowable CAC), chosen by the owner, and the rule used to choose it. Or "not computed". | CRITICAL (answer or "not computed" + H14) |
| H13 | Allowable cost per lead = allowable CAC x expected lead-to-customer rate. Or "not computed". | CRITICAL (answer or "not computed" + H14) |
| H14 | **Risk signoff for unknown economics.** If any of H8, H11, H12, H13 is unknown or not computed: name, role, date/time (TZ), channel, and this statement: "I accept launching with these economics unknown. Monitoring will use the written thresholds in H5/H6 and spend-with-zero-leads flags only. No CPL figure in this file is a business case." | CRITICAL if any of H8/H11/H12/H13 is unknown |

> **ILLUSTRATIVE / UNTESTED / NOT DOMIN8TE DATA.** The arithmetic shape only. Made-up inputs: gross profit after
> fulfillment of CA$300 per new customer; an owner-chosen rule of thumb of 3 to 1 (gross profit to acquisition
> cost; a rule of thumb from the source review, not a Domin8te rule) gives an allowable CAC of CA$100; if 1 lead
> in 5 became a customer, allowable CPL would be CA$100 x 0.2 = CA$20. Every input here is invented for the
> example. Do not copy any of these numbers into a launch.

**Supersession note (2026-11-05):** H5 (target CPL OPTIONAL, "unknown" allowed) stays as written. When H5 is set,
record next to it whether it was derived from H12/H13 or set without economics (then H14 applies). The H
illustrative line above ("target CPL CA$40 set by the client") stays a placeholder, not advice and not a
client default.

## I. Lead definition and attribution
> Illustrative: "A lead = a form submit with a valid phone or email and a name; duplicates within 7 days
> count once; test submissions are tagged and excluded."

| # | Question | Level |
|---|---|---|
| I1 | What counts as one lead? (Meta event? Inbox arrival? Qualified only?) | CRITICAL |
| I2 | How are tests, duplicates and spam excluded from lead counts? | CRITICAL |
| I3 | Attribution setting to report (e.g. 7-day click + 1-day view). Same setting across compared ad sets. | CRITICAL |
| I4 | Where do leads land (inbox, CRM, leads center)? Who has access? Tested? | CRITICAL |
| I5 | Named follow-up owner and response time (e.g. "same business day", "within 1 business day"). | CRITICAL |
| I6 | After-hours and weekend handling. | OPTIONAL |

Note for own account: the lead definition for the DRAFT CPL policy is **unresolved** (`01` §4). Until Karan
decides, I1 answers for own launches are recorded, but the CPL rules stay non-automated.

### I+. Lead states and qualifying questions (2026-11-05 additive, owner-selected Hormozi review items) [ADD #3]
I1 to I6 above are unchanged. Count leads in separate states. Each state has its own definition, its own
evidence and one person who logs it. A later state is always a subset of the earlier one.

| State | Meaning (write the exact definition for this launch) | Evidence source (example) |
|---|---|---|
| S0 Meta-reported | What Ads Manager or Events Manager counts as a result | Ads Manager export / pull file with date range and attribution setting |
| S1 Contactable | Arrived at the intake destination with working contact details; tests, duplicates and spam removed (I2) | Inbox / leads center / CRM record |
| S2 Engaged | Contactable **and** has shown interest in what is sold (replied, answered a question, asked to book) | Reply or call log entry |
| S3 Qualified | Engaged **and** meets the written criteria from the qualifying questions below | Logged answers |
| S4 Customer | Bought, booked a paid service, or visited and paid, per the owner's definition | Invoice, POS or signed order (counts only, no personal data in launch files) |

| # | Question | Level |
|---|---|---|
| I7 | Definition of S0 to S4 for this launch, in one line each. | CRITICAL |
| I8 | For each state: where it is logged, who logs it, and what evidence backs it. | CRITICAL |
| I9 | Qualifying questions, in order, and where each is asked (on the form, or at first contact). | CRITICAL |
| I10 | Which state the launch's thresholds and reports count as "a lead". (Own account: still **UNRESOLVED**; see note.) | CRITICAL |

Qualifying question sequence (reasonable order; the exact wording is **untested** and set per launch):
1. Contact and consent: is the contact detail real, and did they agree to be contacted for this purpose (`11`)?
2. Role / authority: are they the person who decides? (B2B owner ads: "Are you the owner?")
3. Fit: are they inside what the advertiser serves (business type, location in C2)?
4. Need: what do they want help with, in their words?
5. Timing / readiness: when do they want it?

- Keep the form short at a cold start; get working flow first, then add qualifying friction. Ask the rest at
  first contact.
- **No revenue, income or finance questions**, and none of the prohibited questions in `06` §5.
- No response-time or follow-up SLA is added here. Response time stays the owner's written answer in I5.

**Note (2026-11-05):** these states do **not** resolve the own-account lead definition for the DRAFT CPL policy
(`01` §4). That stays UNRESOLVED until Karan decides. I10 records the choice per launch; it does not enable
anything.

## J. Assets and rights
> Illustrative: "Photos shot by the owner on their phone (owner holds rights); logo file from owner; music
> from Meta's licensed library for ads; no customer faces without consent."

| # | Question | Level |
|---|---|---|
| J1 | List every asset (image, video, music, voice, logo, font, review quote) and who holds the rights. | CRITICAL |
| J2 | Consent for any identifiable person in the assets. | CRITICAL if people shown |
| J3 | Any AI-generated imagery, video or voice? Which assets? | CRITICAL |
| J4 | Feed (4:5) and vertical (9:16) versions exist for each ad? | CRITICAL |
| J5 | Landing page URL or form; privacy policy URL. | CRITICAL |
| J6 | Brand rules (colours, banned words, logo use). | OPTIONAL |

## K. Approvals
| # | Question | Level |
|---|---|---|
| K1 | Who approves copy and creative? | CRITICAL |
| K2 | Who approves budget and go-live? (Own account: Karan. Client: client owner **and** Karan.) | CRITICAL |
| K3 | Who may approve pauses and changes after launch, and how fast can they respond? | CRITICAL |
| K4 | Channel and format for approvals (written, with timestamp). | CRITICAL |

## L. Special categories, privacy and consent
| # | Question | Level |
|---|---|---|
| L1 | Does the ad mention jobs/hiring, housing, credit/loans/financial products, or social issues/elections/politics? | CRITICAL |
| L2 | Is personal data collected? Privacy URL, purpose notice, consent wording ready? | CRITICAL |
| L3 | Will leads get email/SMS follow-up? CASL (Canada) express or implied consent basis recorded. | CRITICAL if email/SMS |
| L4 | Any prohibited form questions (finance, health, IDs, etc.)? Must be none. | CRITICAL |

## M. Sales path (2026-11-05 additive, owner-selected Hormozi review items) [ADD #4]
Mandatory for every launch. The path is **opt-in → contact → book → show → close**, with a **named owner at
every stage**. Do not assume every client books calls. If the route is different (for example DM-only,
form-only, walk-in, phone order, no call booking), write the route's real stages and mark the stages that do not
apply as **N/A by route**. An N/A stage needs the client's (or Karan's, own account) **explicit written
confirmation**, with date.

> Illustrative only. Café diner route: "Opt-in = instant form for a lunch offer. Contact = owner texts a
> confirmation within the hours in I5 (consent recorded). Book = N/A by route (walk-in), confirmed by the owner
> in email on <date>. Show = guest visits; front-of-house logs the offer redemption. Close = paid bill."

| Stage | What it means for this launch | Named owner (+ backup) | Channel | Where logged | Reporting field |
|---|---|---|---|---|---|
| P1 Opt-in | | | | | Opt-ins (S0 and S1 counts) |
| P2 Contact | | | | | Contacted |
| P3 Book | | | | | Booked |
| P4 Show | | | | | Showed |
| P5 Close | | | | | Closed (S4) |

| # | Question | Level |
|---|---|---|
| M1 | The route for this launch: standard (opt-in → contact → book → show → close) or an alternate route. If alternate, its stages. | CRITICAL |
| M2 | A named owner (and backup) for every stage that applies. | CRITICAL |
| M3 | Written confirmation for every stage marked N/A by route (who, date, channel). | CRITICAL if any stage is N/A |
| M4 | **Privacy and consent for the path**, confirmed explicitly by the client (or Karan, own account): which contact channels the lead agreed to (email, SMS, call, DM), the CASL / applicable US consent basis, where lead data is stored, who can see it, how long it is kept (`11`). | CRITICAL |
| M5 | Reporting: who reports the stage counts, how often, and from which logs. Counts only; no personal data in launch files. | CRITICAL |
| M6 | What the ad's CTA and the form's thank-you message promise as the next step, and that it matches M1. | CRITICAL |

No response-time target is invented here; I5 holds the owner's written wording. Replies still follow the
approval path in `10` (Domin8te: Karan approves every send).

---

## Completion check
- [ ] Every CRITICAL question answered with the evidence asked for.
- [ ] No answer copied from own-account defaults without the owner choosing it.
- [ ] Interest names (if any) verified available, with name and date.
- [ ] Age range (if any) has evidence.
- [ ] Owner confirmation recorded (method and date).
- [ ] Status set: **READY FOR CHECKLIST** or **BLOCKED** (with the list of gaps).

### Completion check additions (2026-11-05 additive, owner-selected Hormozi review items) [ADD #1 to #5]
- [ ] Offer strength B6 to B10 answered (B11 if a lead magnet is used); proof and guarantee only from approved, written sources.
- [ ] Customer economics H8 to H13 answered with sources, **or** marked unknown / not computed with an H14 named human risk signoff. No price entered as profit.
- [ ] Lead states S0 to S4 defined (I7), logging and evidence named (I8), qualifying sequence written (I9), counted state chosen (I10).
- [ ] Sales path section M filled: route, named owner per stage, N/A stages confirmed in writing, privacy/consent confirmed explicitly, reporting set.
- [ ] Approved proof list (B7) handed to the creative QA in `06` §8.
