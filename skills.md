# Poster Generator: WITNESS NYC–Inspired Design System

## Purpose

Build a generative poster app that creates exciting, distinct compositions from user content. Use Leanna Urena’s chosen WITNESS NYC poster as the visual seed. Translate its design logic into a flexible system rather than reproducing one fixed template with replacement words.

Use these instructions when planning, building, evaluating, or refining the generator. Treat this as a project design brief for the class assignment.

## Understand the seed

The reference uses oversized black condensed capitals on yellow paper, a narrow off-white border, heavy horizontal bars, and a strong vertical composition. “WIT” dominates the top, “NYC” sits smaller in the middle, and “NESS” is rotated 180 degrees below. The date is also upside down. A small white Nike mark appears near the bottom. One central vertical fold and two horizontal folds give the surface a physical, handled quality.

Preserve the boldness, scale contrast, structural rhythm, unexpected reading direction, and printed character. Do not require every output to use those exact words, the same line breaks, the same positions, yellow, or a brand logo.

## Visual principles

### Let typography be the image

- Build the composition primarily from letters, numbers, negative space, and solid bars.
- Use heavy, condensed uppercase sans-serif type as the dominant voice.
- Use Anton as the starting font. Leanna has chosen and supplied Anton, Oswald, Bebas Neue, and League Gothic. Offer these four as font options; account for their different widths and visual weights rather than treating them as identical.
- Use Anton Regular and Bebas Neue Regular at their supplied weights. Use the supplied Oswald variable font at weight 700 for headlines. Start League Gothic at its default width; only expose width changes supported by its font file. Do not simulate bold by adding strokes or distort letter proportions to force a fit.
- Use one family per poster by default. Create contrast through scale, spacing, and orientation instead of unrelated fonts.
- Avoid cursive type, decorative novelty lettering, and thin headline weights.

### Make hierarchy dramatic

- Give each composition a clear first, second, and third reading level.
- Make the headline or a meaningful part of it dominate. Keep location and supporting information clearly subordinate.
- Allow one word, one line, or a deliberate word fragment to become the main visual event.
- Keep essential event information readable even when the headline is experimental.

### Use a grid with room for surprise

- Begin with a portrait format close to the reference’s 5:7 proportions, while allowing other aspect ratios later.
- Align text and bars to a shared grid. Vary the grid between generations: horizontal bands, unequal columns, or an offset modular layout.
- Use intentional differences in density: pair crowded typographic areas with clear open space.
- Use a narrow border or consistent outer margin by default. Allow controlled edge crops for display lettering in more experimental compositions.
- Do not randomly scatter elements. Every shift should reinforce alignment, tension, or hierarchy.

### Use rotation deliberately

- Treat 180-degree rotation as a signature option, not a mandatory placement rule.
- Rotate a complete word, line, or group when an upside-down reading is intended. Do not mirror letters or manually reverse the spelling.
- Allow 90-degree side labels and upright compositions as additional variations.
- Keep at least one clear upright reading anchor in each composition.
- Avoid arbitrary small-angle tilts that weaken the reference’s strong horizontal and vertical structure.

### Make bars structural

- Use solid rectangular bars to divide, underline, frame, or counterbalance text.
- Vary their count, length, position, and thickness in relation to the type and grid.
- Allow a split bar with a narrow gap as a reference-inspired motif.
- Omit bars when the composition is stronger without them. Do not treat the reference’s exact arrangement as compulsory.

### Keep color simple and forceful

- Default to yellow paper, black ink, and a small off-white accent.
- Allow new high-contrast palettes, normally using one background color, one primary ink color, and at most one accent.
- Support light-on-dark designs as well as dark-on-light designs.
- Check the actual foreground/background contrast. Reject generated palettes that make required text difficult to distinguish.
- Keep decorative gradients, rainbow palettes, and unrelated effects out of the core visual language.

### Give the surface a physical feel

- Offer subtle grain, uneven ink, and folded-paper effects as optional finishing layers.
- Vary fold positions or omit folds; do not always divide the page into the same six panels.
- Keep texture secondary to the typography and preserve text legibility.
- Provide a clean mode with no texture.
- Reproduce folds with restrained light and shadow, not a glossy or three-dimensional mockup.

## Measurable starting rules

These are proposed rules for the generator, not verified measurements of the original poster. Test and refine them against rendered results. Keep the structure consistent while varying the composition.

### Canvas, grid, and spacing

- Start with an SVG canvas of **1000 × 1400 units**, a 5:7 portrait ratio. Scale the preview to the screen without changing the artwork proportions.
- Define a base spacing unit **u = canvas width / 100**. At the default size, u = 10.
- Use **4u outer margins** on each side: 40 units. The usable area is 920 × 1320 units.
- Divide the usable width into **six equal columns**, separated by **2u gutters**. Column width = (canvas width − 2 × margin − 5 × gutter) / 6. At the default size, each column is approximately 136.67 units.
- Build blocks by spanning columns: 6, 3+3, 2+4, or 4+2. Use the same column edges for type and bars. Do not snap those calculated edges to the spacing unit if doing so breaks alignment.
- Use gaps and padding of **1u, 2u, 3u, 4u, 6u, or 8u**. Keep at least 2u between separate text blocks and between text and a bar, measured from visible letter bounds.
- Default to left-aligned text within each block. A centered location label or rotated group is allowed when its position follows the grid.
- For stacked layouts, begin with content-band proportions of **40% / 20% / 40%**, **45% / 15% / 40%**, or **35% / 25% / 40%**. Apply these proportions to the available height after subtracting gaps and bars. Adjust to fit content; do not make the bands permanent templates.
- Optional border: an off-white frame **1u thick**, separate from the 4u text-safe margin. Essential information must stay inside that margin.

### Typography scale and fitting

Use this starting hierarchy at the 1000-unit canvas width:

| Role | Starting size | Allowed fitting range |
| --- | --- | --- |
| H1: main title or dominant title segment | 240 units (24u) | 160–400 units (16–40u) |
| H2: location or secondary label | 60 units (6u) | 40–100 units (4–10u) |
| Details: date and optional supporting copy | 30 units (3u) | 24–40 units (2.4–4u) |

- The starting size ratio is **8:2:1**. These roles describe reading order, not mandatory HTML heading tags inside the artwork.
- Aim for H1 to be at least **3× H2**, and H2 at least **1.5× details**, when all roles are present. Choose compatible values from the ranges rather than selecting each size independently.
- For a multi-line headline, start with baseline spacing of **0.9× the font size**; allow 0.85–1.05× after checking that visible letters and accents do not collide.
- Use **1.2× line spacing** for multi-line supporting text.
- Start headline letter spacing at **0em**, with a controlled range of **−0.02em to +0.02em**. Start smaller text at +0.02em and allow 0 to +0.06em.
- Wait until the selected font is loaded before measuring. Include accents, letter spacing, and rotation in the final bounds check.
- Try new line breaks and block proportions before reducing type size. If the content still cannot fit within these limits, choose a different composition or ask for shorter text.
- Preserve entered wording and punctuation. Uppercase styling may be used for the display title, but never silently rewrite the content.
- Cropping is off by default. When explicitly enabled, crop only display lettering; never crop location, dates, or required supporting text.

### Bars, palette, and texture

- Use **0–3 structural bars**, each **1–4u thick**. Their lengths should match one or more grid columns.
- A split bar may use a **1–2u gap**. Keep bars outside required text bounds.
- Starting palette: **yellow #F1DC45**, **black #111111**, and **off-white #F5F1E7**. These are chosen working colors, not sampled values from the reference.
- Limit each poster to one background, one main ink color, and at most one accent. Use the off-white mainly for the border or small graphic details.
- Start with clean artwork. Optional grain and fold overlays should remain subtle, initially **3–8% opacity**, and must not weaken text readability.
- Rotate text groups only **0°, 90°, 180°, or 270°**. Keep at least one essential information group upright.

### Variation without losing the rules

Keep the grid, fitting checks, and hierarchy as constraints. Vary column spans, band proportions, title breaks, dominant segment, orientation, and bars together. When settings are unlocked, each Generate action should change at least two of these structural choices; a color or texture change alone is insufficient. If repeated attempts cannot produce a valid new composition, explain which setting to unlock.

## Supplied font files

Use these exact filenames as project-relative paths once the user has placed them in the project’s `fonts/` folder:

| Font | File |
| --- | --- |
| Anton | `fonts/Anton-Regular.ttf` |
| Oswald | `fonts/Oswald-VariableFont_wght.ttf` |
| Bebas Neue | `fonts/BebasNeue-Regular.ttf` |
| League Gothic | `fonts/LeagueGothic-Regular-VariableFont_wdth.ttf` |

The four font files have been uploaded. Their placement in the local project and inclusion of license files have not been confirmed. Keep each font’s license alongside it, using separate subfolders or distinct license filenames so repeated `OFL.txt` files do not overwrite one another.

## Generative behavior

Make Generate produce a new composition, not merely a new color or tiny positional change.

1. Read the supplied headline, location, date, and optional supporting text. Identify their roles and measure their lengths.
2. Choose a composition family that can accommodate the content.
3. Select compatible grid proportions, line breaks, headline scale, spacing, alignment, orientation, bars, palette, and texture.
4. Measure the rendered typography using the loaded font. Fit content to its assigned areas.
5. Check hierarchy, legibility, overlaps, margins, and content completeness. Revise or regenerate failed candidates.
6. Compare with the previous result and avoid repeating the same composition when unlocked settings permit a meaningful change.
7. Preserve the chosen seed and settings so a successful result can be reproduced and exported.

Use constrained variation rather than changing every parameter independently. Coordinate choices: a large rotated word may need a quiet upright label and fewer bars; a dense headline may need larger margins and less texture.

### Starting composition families

- **Stacked impact:** use uneven horizontal bands, a dominant headline, a smaller information band, and an optional rotated lower section.
- **Offset columns:** place large type in unequal columns with a contrasting upright or rotated supporting block.
- **Single-word monument:** make one word dominate the page, using smaller information and one strong bar to balance it.
- **Split and turn:** break a headline into meaningful segments and change one segment’s orientation while preserving a decipherable reading order.
- **Rhythmic repetition:** repeat a user-supplied headline or keyword as a deliberate graphic pattern, with one dominant instance and a clear information area.

Treat these as starting strategies. Vary their internal proportions and arrangements; do not hard-code five frozen templates.

## Preserve and fit user content

- Preserve spelling, punctuation, accents, dates, and meaning. Never invent event information or silently discard words.
- Prefer word-boundary line breaks. Allow deliberate word splitting as an experimental option, but do not force every word into the original’s three-letter/four-letter split.
- Fit long text by changing line breaks, proportions, composition family, and size before clipping it.
- Never crop required dates, locations, or supporting information. Only crop display lettering intentionally, with a control to disable it.
- Handle short headlines and empty optional fields gracefully; redistribute space instead of leaving accidental gaps or placeholder labels.
- If content cannot fit legibly, explain the problem and request shorter text. Do not silently shrink it to unreadable size.
- Check font glyph support and provide a suitable fallback or a clear warning for unsupported characters.

## Proposed app controls

Follow Leanna’s interface plan: Title, Location, and Date fields on the left, followed by one shared Generate button; a large Poster Preview on the right with a Download SVG button beneath it. “Title” is the headline described in this file. On narrow screens, stack the controls above the preview. Place optional supporting text and detailed styling controls in an expandable advanced area.

Allow users to change:

- Headline, location, date, and optional supporting text.
- Palette, including the reference yellow-and-black preset.
- Layout choice or automatic layout selection.
- Typography scale and spacing within safe limits.
- Rotation, bars, border, texture, and display-letter cropping.
- Variation level: restrained, balanced, or experimental.
- Random seed, with a way to reproduce a previous result.

Allow users to lock settings they like while generating variations of the remaining settings. Respect locks; if they prevent meaningful variation, explain which control to unlock. Keep user-entered content unchanged when Generate is clicked.

Build the basic fields, Generate, preview, font selection, and SVG download first. Add advanced controls after the basic workflow works. Keep the screen simple and use clear labels.

## Output and implementation requirements

- Build real procedural layouts from editable text and shapes. Do not use an AI-generated flattened poster image as the generator’s output.
- Use SVG as the primary poster representation so the preview and exported artwork share the same composition.
- Keep headline text, supporting text, bars, background, and optional texture in separate logical groups.
- Export SVG with editable text and vector shapes. Include font requirements with the project; text editability depends on the font being available in the editing application.
- If outlined text export is added, label it clearly: outlines preserve appearance and editable letter shapes but are no longer editable as typed text.
- Keep any raster texture separate and optional. Do not flatten the whole poster to preserve a texture effect.
- Ensure export captures the current preview, seed, settings, and content without generating a different design.
- Keep font files and their open-source licenses organized with the project. Keep the source references below with the project; verify the matching license when organizing the downloaded files.
- Do not automatically reproduce the Nike mark on new posters. Offer an optional user-supplied logo or a small original graphic accent; the style must work without a logo.
- Follow the assignment’s later build requirement for one complete HTML page rather than disconnected code snippets. Keep the GitHub Pages deployment and editable export requirements in view.

## Evaluate the generator

Before calling a result successful, check:

- Does typography carry the design?
- Is there a clear first point of attention and readable supporting information?
- Does the layout feel deliberate, with coherent alignment and spacing?
- Does it retain the reference’s bold, graphic energy without copying its exact arrangement?
- Does Generate produce visibly different structures, not just cosmetic changes?
- Are all required words and numbers preserved?
- Are rotations correct, with no accidental mirroring?
- Are essential elements within the export boundaries and free from unintended overlap?
- Does the export match the preview, and can its text and shapes be edited in Illustrator?

During development, test a one-word headline, a long multiword headline, accented text, empty optional fields, and all rotation modes. Generate at least six results from the same content and look for real variation in scale, grouping, orientation, and use of space.

For the assignment’s later Müller-Brockmann Tonhalle stress test, use a supplied reference to identify limits in grid, hierarchy, and content handling. Document what breaks and revise the relevant rules. Do not claim this seed style can already reproduce every unrelated poster style.

## Font sources

- Anton: https://fonts.google.com/specimen/Anton
- Oswald: https://fonts.google.com/specimen/Oswald
- Bebas Neue: https://fonts.google.com/specimen/Bebas+Neue
- League Gothic: https://open-foundry.com/fonts/league-gothic

## Project status

Updated October 12, 2026. The reference poster, written analysis, design-rules draft, initial interface sketch, and handoff.md have been created. Leanna has chosen and uploaded all four font files listed above. This revision adds measurable starting rules and records the planned interface.

The assignment overview confirms one complete HTML page, SVG or PDF export with editability checked in Illustrator, a Müller-Brockmann Tonhalle stress test, and final submission with a GitHub Pages link. SVG is the planned first export format. The app has not yet been built or tested, and local font/license organization and GitHub uploads remain unconfirmed.

Next: use plain-language requirements to have Gemini prepare a build prompt, then provide that prompt, this file, the reference poster, and the interface sketch to request the first complete HTML page. During development, verify that exported text remains editable as text and shapes remain editable as vectors in Illustrator; the SVG extension alone does not establish editability. Record completed work and revised decisions in handoff.md.
