# Clay Landing Pages

Personalized landing pages for prospects who requested a Clay demo. Each page is a single
standalone `.html` file, with messaging tailored to the prospect's role and sent before or
around the demo call.

## Status

| Prospect | Title | Company | Status |
|---|---|---|---|
| Sarah Mitchell | VP of Revenue Operations | Retool | Built (v1, v2, v3) |
| Marcus Chen | Head of Growth | Linear | Page in `deploy-marcus/` |
| Emily Rodriguez | Director of Sales Development | Loom | Not started |
| James Okonkwo | GTM Engineer | Webflow | Not started |
| Rachel Goldstein | VP of Sales | Airtable | Not started |

## What's here

- `sarah-mitchell-retool-v3.html`, `-v2.html`, `.html`: Sarah's page, newest to oldest.
- `deploy/sarah.html` and `deploy-marcus/marcus.html`: smaller versions of the pages without embedded fonts, each with a `vercel.json` that asks search engines not to index them.
- `landing-page-prospects.csv`: the five prospects.
- `clay_icp.txt`: ideal customer profile, pain points, and per-role messaging angles.
- `clay_value_prop.txt`: older value-prop notes. Some numbers are out of date.
- `clay-brand-book.md` / `.html`: brand system reconstructed from clay.com (not official).
- `clay-tone-of-voice.md`: voice guide with sourced examples.
- `CLAUDE.md`: working rules and decisions for building the pages with Claude Code.

## How the pages are built

- **Role-based personalization** from the ICP doc, not per-company research.
- **One goal per page:** confirm the demo. The reader already said yes, so the page reassures and primes rather than re-sells.
- **Clay leads the branding.** The prospect's accent color appears in a small "Prepared for [Company]" chip, taken from their live site.
- **Verified by rendering:** finished pages are screenshotted in headless Chrome and checked by eye.

## Before sending a page

- Replace the placeholder booking link `#confirm-demo` with the real scheduling link.
- **Fonts:** pages use Schibsted Grotesk, loaded free from Google Fonts. Clay's own face, Roobert, is not included because only trial files exist.
