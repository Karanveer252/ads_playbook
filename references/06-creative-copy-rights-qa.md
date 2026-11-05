# 06. Creative, copy, link, UTM, form and rights QA

Run per ad. One row per ad in the QA table at the bottom. Meta specs cited from local research
(2026-10-19, not re-verified today).

## 1. Formats
- [ ] 4:5 feed version (1080x1350 typical) and 9:16 vertical version (1080x1920 typical). 1:1 optional for IG Feed (O37).
- [ ] Key text, logo and CTA inside safe zones on 9:16; keep top, bottom and sides clear; bottom 40% clear when there's a disclaimer (O38).
- [ ] If 9:16 is missing, Meta may apply automatic templates to Reels (O36). Either supply 9:16 or restrict placements.
- [ ] Video: container/codec and size within Meta's current specs (check the Meta specs page at build; volatile).
- [ ] Missing 4:5 for a vertical-only video = FAIL unless the approver accepts the feed crop in writing (lesson from `PRELAUNCH_2026-11-04.md` row 8).

## 2. Copy
- [ ] One offer per ad, matching the owner-approved offer exactly (questionnaire B1).
- [ ] Headline and CTA say what the offer is and who it's for. Avoid passive CTAs like "See details". Description filled.
- [ ] Every claim provable. No invented stats, reviews, testimonials or results.
- [ ] Scarcity or time claims ("only N spots", "ends Friday") true at launch and on the day they run.
- [ ] Domin8te-managed copy: claim check passes; numbers only from the proof file; no em dashes; no prices; no
      audit/report/PDF/checkup/score/grade framing; banned outreach phrases not used (`brand/lessons.md`).
- [ ] Special category words checked (hiring, housing, credit, politics); see `11`.
- [ ] Spelling, grammar, emoji use per brand rules.

## 3. Advantage+ creative and AI
- [ ] List every Advantage+ creative enhancement toggle for the ad and its state (O35, O36). Some are on by default, including generative ones.
- [ ] Generative enhancements (text variations, overlays, music, animation, expansions) **off** unless the owner approves. Domin8te: Ad Studio + Karan, plus the client for client ads.
- [ ] AI-generated imagery, video or voice: Meta AI label on. List which assets.

## 4. Links and UTMs
- [ ] Destination URL correct, HTTPS, loads on mobile data.
- [ ] UTMs present; `utm_content` = ad name (`04` §5).
- [ ] Display link (if used) matches the real domain.

## 5. Form
Website form:
- [ ] Works on mobile; success state shows; conversion event fires only on success.
- [ ] Privacy policy link visible; consent wording for follow-up.
Instant form:
- [ ] Form type recorded (More volume / Higher intent / Rich creative).
- [ ] Privacy policy URL (required) and a purpose notice (O1, O5).
- [ ] No prohibited questions: financial info, government IDs, health, criminal history, insurance, political/religious/race/sexual orientation/union, logins, child's date of birth, duplicates of prefill fields (O6). Domin8te: no revenue, income or finance questions at all.
- [ ] Multiple-choice qualifiers preferred; keep it short (O3).
- [ ] Thank-you screen sets a realistic follow-up promise that matches the named owner's response time.

## 6. Rights
| Asset | Type | Rights holder | Proof (licence, owner statement, date) | People shown? Consent? | AI? |
|---|---|---|---|---|---|
| | | | | | |

- Music: licensed for ads (e.g. Meta's sound collection or a licence covering paid ads). Organic-only licences don't cover ads. [Practice]
- Client photos/videos: owner confirms they took them or hold rights. Public images of a business are not automatically licensed.
- Logos and fonts: official files from the owner.

## 7. Per-ad QA table
| Ad name | 4:5 | 9:16 | Safe zones | Copy QA | Claims ok | Advantage+ toggles listed | AI label | UTM ok | Link ok | Rights ok | Reviewer |
|---|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | | |

## 8. Hook, call-out, proof, ad-page promise and CTA QA (2026-11-05 additive, owner-selected Hormozi review items) [ADD #5]
Sections 1 to 7 above are unchanged. This section is a **check only**. It does not write hooks, headlines or ad
copy, and it does not require new public hooks. It judges the approved copy against **approved evidence** only.
A FAIL goes back to the copy owner and the approver; the QA reviewer does not rewrite the ad.

Per ad:
- [ ] **Call-out.** The first line or first frame makes it clear who the ad is for, or names their problem, and
      matches the buyer model chosen in questionnaire C1.
- [ ] **First five seconds** (video) or first line plus image (static). The offer or the problem is clear without
      sound, inside the safe zones in §1.
- [ ] **Proof.** Every proof element (review, quote, photo, number, logo, case study) is on the approved proof
      list in questionnaire B7, with source, date and permission. If B7 says "none", the ad makes no proof
      claims. Never create, edit or round proof. Where several approved items exist, prefer the most recent.
- [ ] **Ad-page promise match.** The landing page headline or instant form intro states the same offer and
      conditions as the ad (B1, B3). No new promise appears on the page that the ad did not make, or the reverse.
- [ ] **CTA.** States the exact next action, and that action matches the sales path route in questionnaire M
      (for example, no "book a call" if the route has no call). Any reason to act now is true at launch (B3).
- [ ] Domin8te-managed rules in §2 still apply (claim check, proof file, no prices, no banned framings).

| Ad name | Call-out | First 5 s | Proof IDs (from B7) or "none" | Ad-page match | CTA = route (M) | Urgency true | Reviewer |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
