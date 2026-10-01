# Clay Landing Pages

Last updated 2026-09-29.

## Goal

I'm an AE at Clay.com. Five prospects requested a demo. Build one personalized landing page per
prospect, with messaging tailored to their role, to send before or around the demo call.

**Status: 1 of 5 built (Sarah Mitchell, v2). Do not build the other four until I say so.**

| Name | Title | Company | Status |
|---|---|---|---|
| Sarah Mitchell | VP of Revenue Operations | Retool | v2 done |
| Marcus Chen | Head of Growth | Linear | on hold |
| Emily Rodriguez | Director of Sales Development | Loom | on hold |
| James Okonkwo | GTM Engineer | Webflow | on hold |
| Rachel Goldstein | VP of Sales | Airtable | on hold |

## Working rules

- **Audit before install.** For any skill, plugin, or external download: read it, report the
  audit findings, and wait for my approval before installing anything into the project or a
  skills folder.
- **Don't build ahead.** Only build for the prospect I name.
- **Verify by rendering.** Screenshot finished pages with headless Chrome and look at them.
- **Keep large encoded assets out of context.** Embed fonts and images with a Bash/Python
  find-and-replace on placeholder tokens, not by pasting base64.

## Files

`Build Along Resources/` (Day 1):
- `landing-page-prospects.csv`: the five prospects.
- `clay_icp.txt`: ICP, pain points, per-role messaging angles. Prospect titles map onto its
  decision-maker list, which is what makes role-based personalization work.
- `clay_value_prop.txt`: **stale.** Its "5,000+ customers", "$3.1B valuation" and "150 providers"
  are outdated. Use the current numbers below.
- `sarah-mitchell-retool-v2.html`: **current page** (~1.3MB, self-contained).
- `sarah-mitchell-retool.html`: v1, superseded. Kept for comparison.

`Day 2 Build Along Resources/`:
- `clay-brand-book.md` / `.html`: brand system reconstructed from clay.com (not official), tagged
  CONFIRMED / OBSERVED / HYPOTHESIS.
- `clay-tone-of-voice.md`: voice guide from a 12-page scrape of clay.com, with sourced examples.
- `clay assets.zip` (110MB): logos, Roobert trial fonts, homepage videos, founder photos.

## Decisions made

- **Personalization:** role-based from the ICP doc, not per-company research.
- **CTA:** confirm the demo. Use the tone guide's line "Confirm my demo time".
- **Content:** minimal. No logo wall, stats grid, or video slot.
- **Format:** plain standalone `.html`, not a published Artifact.
- **Booking link:** placeholder `#confirm-demo`. Replace with the real scheduling link before sending.

## Brand and voice rules

- **Colors (confirmed from clay.com CSS):** oat neutrals `#fefdfb` (bg), `#f3f2ed`, `#eee9df`,
  `#dad4c8` (borders); ink `#1b1a18`. One accent family per section, never a rainbow in one
  block. Blueberry `#395afa` for data, Lime for resolved or highlighted rows, Lemon
  (`#fcbe11`/`#fae188`) for eyebrows and badges.
- **Type:** Roobert (variable, 300-900) with Roobert Mono for data labels. Medium weights
  (500-575). Headings at line-height 1.0 with tight negative tracking. Fallback: Schibsted Grotesk.
- **Components:** 12px button radius, flat colors, no box-shadows, background-color-only hover
  transitions (`0.3s cubic-bezier(0.075, 0.82, 0.165, 1)`), large-radius tinted cards.
- **Co-branding:** Clay leads, with the Clay mark first. The partner's accent goes in the page
  (a small "Prepared for [Company]" chip), never in either logo.
- **Partner colors** must come from the partner's real live site, never guessed or reused.
  Retool: `#151515`, cream `#e9ebdf`, accent `#e8765e`. The old indigo `#3C3C8C` is stale.
- **Never invent facts** about the prospect. Pages are non-public previews, one prospect each.
- **Voice:** builder-confident, specific (name + number + mechanism), quietly playful. Second
  person, present tense, verb-first CTAs, 8-16 words per marketing sentence, bold proof
  names and numbers. No exclamation marks. No "revolutionary", "cutting-edge", "best-in-class",
  or "leverage". **Never name a competitor** (use "Provider 1/2/3").
- **Tone for these pages:** the reader already said yes to a demo. Reassure and prime, don't re-sell.

**Current proof points (July 2026):** 500,000+ GTM teams, $5B valuation, 200+ data providers,
140M monthly Claygent runs, 4.9 stars on G2.

## Sarah's page (v2)

Headline built around CRM trust and staleness (from the ICP pain points). Centerpiece is a mock
waterfall-enrichment table, with the Blueberry accent and a Lime "resolved" pill. Footer uses
the tone guide's line "Inspired by our customers. Built with love." Clay logo is
`Full Mark/Dark/Clay_Logo_Tertiary_Blk.png` from the zip; fonts and logo are base64-embedded.

## Open items

1. **Design sign-off:** I haven't confirmed v2's direction. Confirm before templating it four more times.
2. **Real booking link** to replace `#confirm-demo`.
3. **Font licensing:** the embedded Roobert files are trial fonts, fine for internal previews
   only. Before anything goes external, license Roobert or switch to Schibsted Grotesk
   (already the fallback, so it's a one-line change).
4. **Per-prospect work for the other four:** pick pain points from the ICP doc for each role
   (Marcus and Rachel: Head of Growth / Primary Buyer; Emily: SDR Manager; James: GTM Engineer)
   and pull each company's accent from its live site.
5. **`frontend-design` skill:** audited and installed at `.claude/skills/frontend-design/`
   (Apache 2.0, prose-only guidance, no scripts). Not loaded in the 2026-09-29 session, so restart
   Claude Code, then check `/skills`. When using it, the brand book and tone guide win over its
   defaults. Its warnings about cream and terracotta don't apply to Clay's oat palette.
