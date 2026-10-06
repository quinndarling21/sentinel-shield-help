# Sentinel Shield Help Center

Static help center served by GitHub Pages from `main` at
https://quinndarling21.github.io/sentinel-shield-help/

## Publish a scam alert

1. Copy `alerts/_template.html` to `alerts/<brand>-<scam-in-a-few-words>.html` (lowercase, hyphens).
2. Replace every `{{PLACEHOLDER}}`:
   - `{{TITLE}}`: `Scam alert: <what it is>` (for example `Scam alert: fake MetroPass unpaid toll text`)
   - `{{DATE}}`: publish date, `Mon D, YYYY`
   - `{{SUMMARY}}`: one or two plain sentences
   - `{{WHAT_IT_LOOKS_LIKE}}`: what the message says and where it shows up
   - `{{IMAGE_FILE}}` / `{{IMAGE_ALT}}` / `{{IMAGE_CAPTION}}`: a **redacted** screenshot saved in `alerts/img/` (never an unredacted one)
   - `{{SPOT_n}}`: how to spot it (add or remove `<li>` items as needed)
   - `{{PAID_n}}`: what to do if you already paid
   - `{{BLOCKED_SENTENCE}}`: what a customer sees now that Sentinel Shield blocks the link
3. Remove the `<meta name="robots" content="noindex">` line the template carries.
4. Add a list item at the top of the list between `<!-- ALERTS:START -->` and `<!-- ALERTS:END -->` in `alerts/index.html`.
5. Add the same item at the top of `<!-- LATEST:START -->` in `index.html` and keep only the 3 newest there.
6. Commit to `main`. Pages redeploys in about a minute; check the live URL returns 200.

Style: plain language, short sentences, no jargon. Existing alerts in `alerts/` are good examples.
