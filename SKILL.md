---
name: typography-discovery
description: Research, evaluate, preview, and implement distinctive typefaces for a new or existing website without defaulting to generic font choices. Use for website builds, UI redesigns, or typography reviews.
---

# Typography Discovery

## Purpose

Select typography deliberately instead of falling back automatically to familiar defaults. The goal is a distinctive, legible, brand-appropriate typographic system.

This skill supports controlled typography experiments on already completed projects. Preserve existing design and functionality unless the user explicitly authorizes broader changes.

## Non-negotiable rules

- Do not automatically choose Inter, Roboto, Arial, Geist, Manrope, Open Sans, Lato, Montserrat, or another familiar default merely for convenience.
- Do not choose unusual fonts just to be different. Choose for fit, legibility, and brand character.
- Google Fonts is one eligible source, not the default or exclusive catalog.
- Never claim to have searched a website, checked a license, downloaded a font, or tested browser rendering unless you actually did.
- A “free font” label does not prove commercial-use rights or SIL Open Font License (OFL) status.
- Verify the exact family/version license at the original source or in the distributed license file. Do not infer licensing from a directory listing.
- Prefer self-hosted WOFF2 files when practical and permitted. Preserve required copyright and license notices.
- Do not change framework, build system, package manager, component architecture, copy, layout, colors, spacing, or interactions in a typography-only task unless necessary and approved.
- Do not overwrite or delete existing font assets before the replacement has been reviewed and confirmed to work.

## Phase 1 — Inspect the project

Before editing:

1. Read repository instructions, README, package scripts, framework setup, and design-system files.
2. Find all font usage: CSS `font-family`, custom properties, `@font-face`, external imports and links, Tailwind/theme tokens, component-library typography settings, and existing font assets/license files.
3. Map the hierarchy: display/headings, body, navigation, UI labels, tables/data, and editorial elements.
4. Establish the intended brand, audience, content, language(s), and visual direction from project context.
5. If browser tooling is available, run representative pages at desktop and mobile sizes and establish a baseline. Note available build/test commands.
6. Report the current font stack and likely change scope before editing.

For a completed project, this is a controlled typography experiment, not permission for a redesign.

## Phase 2 — Define the brief

Describe the intended direction in 3–5 terms grounded in the brand and content (for example: editorial, warm, technical, rural, precise, playful, premium, utilitarian, experimental).

Evaluate:
- Brand personality and audience.
- Reading comfort for long text and small UI sizes.
- Display character at large sizes.
- Required language and glyph support, including German ä ö ü Ä Ö Ü ß, punctuation, and currency symbols.
- Available weights/styles and variable-font axes.
- Compatibility with the existing visual identity.
- Performance, font loading, fallback behavior, and layout shift.
- Whether one family with multiple weights is better than an arbitrary pairing.

Do not introduce a second family merely for the sake of pairing fonts.

## Phase 3 — Discover candidates

Search multiple sources when web access is available. These are discovery resources, not guarantees of licensing, provenance, or suitability.

### Independent foundries and curated directories
- UNCUT — https://uncut.wtf/
- Best Free Fonts — https://bestfreefonts.com/
- Velvetyne Type Foundry — https://velvetyne.fr/
- Collletttivo — https://www.collletttivo.it/
- Open Foundry — https://open-foundry.com/
- Use & Modify — https://usemodify.com/
- Fontshare — https://www.fontshare.com/
- Type.Fish Open Source — https://www.type.fish/typefaces/open-source/
- Type Barn — https://typebarn.com/
- Fonts by Fasu — https://fonts.fasu.dev/
- Font Squirrel — https://www.fontsquirrel.com/
- The League of Moveable Type — https://www.theleagueofmoveabletype.com/
- SIL Open Font License directory — https://openfontlicense.org/ofl-fonts/

### Real-world use and inspiration
- Fonts In Use — https://fontsinuse.com/
- Typewolf — https://www.typewolf.com/
- Freesources Typography — https://freesourc.es/Typography
- Design Resources for Developers — https://designresources.dev/fonts

### Technical delivery
- Fontsource — https://fontsource.org/
- Google Fonts — https://fonts.google.com/ (valid source, but do not default to familiar families)
- Google Webfonts Helper — https://gwfh.mranftl.com/fonts (check current availability)

Fontshare and other services may use their own licenses rather than OFL. Always inspect the original font's license. If a source is inaccessible, do not pretend it was searched; continue with accessible sources and state the limitation.

### Shortlist requirements

1. Build a shortlist of at least 5 plausible families when practical.
2. Include genuinely different directions, not five near-identical geometric sans-serifs.
3. Consider grotesque, humanist, serif, slab serif, display, condensed, mono, variable, and experimental faces where appropriate.
4. Record each candidate's family, designer/foundry if available, original source URL, category/character, styles and variable axes, glyph/language coverage, exact license and evidence, self-hosting suitability, strengths, risks, and fit for the project.
5. Never fabricate font names, metadata, availability, licensing, or test results.

If web access is unavailable, inspect local assets and use known candidates only where licensing can be verified from local files or reliable project documentation. Mark unverified facts clearly.

## Phase 4 — Compare before committing

For a meaningful change, present 3 distinct typographic directions before implementing, unless the user explicitly asks you to choose and proceed.

For each direction provide:
- Heading/display family and body/UI family, if a second is useful.
- Rationale tied to the project.
- Source and license status (verified or unverified).
- Risks and compromises.
- A concise description of how the existing design's character would change.

Create a specimen using actual project copy, not alphabet-only samples. Include a heading, subheading, long and short paragraphs, navigation, buttons, numbers/prices, punctuation, German characters, multiple weights/sizes, and desktop/mobile widths.

Prefer an isolated specimen page or temporary branch over immediately changing every page. If feasible, compare candidates side by side in the actual browser. Otherwise create a static HTML/CSS specimen and state the limitation.

For an existing project, wait for approval before changing production styles unless the user explicitly authorized autonomous implementation. If end-to-end implementation is requested, choose the strongest candidate and document why.

## Phase 5 — Implement safely

1. Obtain files from the original source or a trusted package that preserves licensing information.
2. Verify the exact license and retain required notices in a suitable location, following the license terms.
3. Prefer WOFF2 where available and appropriate. Avoid untrusted mirrors.
4. Self-host where practical and permitted; do not add an external font request without a reason.
5. Declare `@font-face` with correct `font-weight`, `font-style`, and `font-display` behavior.
6. For variable fonts, specify only the weight range actually supported by the file.
7. Define robust fallback stacks. Do not treat fallback as a substitute for verifying the chosen font loads.
8. Update central design tokens instead of scattering family names across components.
9. Limit changes to the authorized typography scope. Preserve layout, copy, interactions, responsive behavior, and existing brand elements.
10. Check text wrapping, headings, navigation, buttons, cards, forms, long copy, and mobile overflow. Font metrics can change layout.
11. Run relevant build, lint, and test commands when available.
12. If browser tooling is available, verify the selected font really renders and check the console/network for failed font requests or decoding errors.

Do not subset fonts unless all required languages and glyphs remain covered. Confirm that the license permits the intended use and redistribution.

## Phase 6 — Report

Summarize:
- Chosen families and rationale.
- Original source and exact license status, distinguishing verified from unverified facts.
- Font file and license-notice locations.
- Files/tokens changed.
- Tests and browser checks actually performed.
- Remaining issues and trade-offs.

Never claim a visual browser check if only static code inspection was performed.

## Final checklist

- [ ] Selection is deliberate and tied to the existing brand.
- [ ] Multiple sources considered where available.
- [ ] Exact license checked.
- [ ] Required glyphs, including German characters, render.
- [ ] Weight ranges match the actual font files.
- [ ] Local loading works or remote loading is justified.
- [ ] Required license notices are preserved.
- [ ] Layout and responsive behavior remain intact.
- [ ] Build/tests and browser rendering checked where tools permit.
- [ ] Changes stay within the authorized scope.
