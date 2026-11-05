# 11. Special ad categories, regulated content, privacy, consent

**Not legal advice.** Meta category names and restrictions change; each item below is from local research
dated 2026-10-19 or general knowledge and is marked **unverified today** unless stated. Check Meta's current
pages (`SOURCES.md` O42, O43) at build time.

## 1. Special ad categories (decide before building)
| Ad mentions | Category (Meta name may differ today) | Effect (US and Canada) | Status |
|---|---|---|---|
| Jobs, hiring, "we're hiring" | Employment | Age, gender, postal-code targeting unavailable; lookalikes and some interests limited; city radius expanded (O42) | From local research O42; re-verify |
| Rentals, home sales, housing | Housing | Similar targeting limits | Unverified today |
| Loans, credit, financial products | Credit / financial products and services | Similar targeting limits | Unverified today; category name has changed over time |
| Social issues, elections, politics | Social issues, elections or politics | Authorization and "Paid for by" disclaimer required | Unverified today |

Rules:
- Restaurant/café promotions are normally not a special category (O42). A restaurant **hiring** ad is.
- If a category applies, own-account or client age/gender rules can't be applied. Re-answer questionnaire D.
- Domin8te: flag any client hiring ad to Karan before building (playbook rule 9).

## 2. Regulated content to check (Meta Advertising Standards, O43)
- Alcohol: local age and location restrictions apply; check the Advertising Standards alcohol section and local law. (Relevant for bars/restaurants promoting drinks.) Unverified today.
- Health or weight claims about food: avoid; they trigger policy review.
- Before/after, personal attributes ("Are you struggling…?") wording can be rejected. Review copy.

## 3. Lead form privacy (from O1, O5, O6)
- Privacy policy URL required on instant forms.
- A reasonably prominent notice of why data is collected; contact people only for that purpose.
- No prohibited questions (list in `06` §5). Domin8te: no revenue/income/finance questions at all.

## 4. Consent and messaging law (Canada and US)
| Topic | What to record | Notes |
|---|---|---|
| CASL (Canada) | Consent basis (express or implied) for any commercial email/SMS follow-up; sender ID and unsubscribe | Domin8te is in Winnipeg; CASL applies (`cads-*` Domin8te notes) |
| PIPEDA (Canada) | Purpose, retention, access to personal data | Provincial laws may add duties (e.g. Quebec); confirm with counsel. Unverified |
| US email | CAN-SPAM basics: accurate sender, opt-out | Unverified today |
| US SMS/calls | TCPA consent for texts/calls | Unverified today; get counsel for SMS follow-up |
| Customer lists | Consent basis before uploading for custom audiences | Hashing per Meta docs |

## 5. Data handling for this package
- Don't store lead personal data, customer lists, raw exports, tokens or credentials in launch files.
- Store counts, dates and file references, not the data itself.
- Follow the advertiser's retention and deletion rules (`cads-setup` data-lifecycle contract).
