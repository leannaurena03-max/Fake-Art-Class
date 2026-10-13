# Poster Generator — Project Handoff

**Student:** Leanna Urena  
**Class:** A.I. for Designers  
**Last updated:** October 12, 2026  
**Current stage:** Session 1 — research, design rules, and interface planning

## Project goal

Create a poster generator inspired by my chosen WITNESS NYC poster. It should make new, visually different posters using the original poster’s bold typography, strong contrast, structured spacing, and unexpected rotation. Each generation should offer a new composition while keeping the text I entered.

Use `skills.md` for the design rules. Use this file to understand the project’s progress, decisions, and next steps.

## Reference and visual direction

The reference file is `hort-nke-lebron-witness-campaign.jpg`.

My analysis describes large, heavy black sans-serif letters on a yellow background. “WIT” is at the top, a smaller “NYC” is in the middle, and “NESS” is upside down below. Black bars divide the layout. The open space around the smaller text balances the large lettering, and the border and creases give it a printed-paper feeling.

The qualities I want to carry into the generator are boldness, energy, dramatic size differences, and typography acting as the main image. New posters do not need to repeat the exact WITNESS layout or include the Nike logo.

## What is done

- Chosen the WITNESS NYC reference poster.
- Written a personal analysis of its type, hierarchy, layout, color, spacing, and texture.
- Created a `skills.md` draft for a generative design system. The latest supplied copy is named `skills(2).md`.
- Identified Anton as the first font candidate, with Oswald Bold, Bebas Neue, and League Gothic as alternatives.
- Drawn and revised an initial interface sketch with content fields, a poster preview, and a download control.

The latest sketch image could not be visually checked in the last review. Confirm that it has one shared Generate button before treating that revision as final.

## Interface plan

Keep the first version simple:

- **Left side:** Title, Location, and Date fields, followed by one Generate button for the whole poster.
- **Right side:** A large Poster Preview with a Download button underneath.
- **Generate:** Keep the entered text and produce a new composition using the design rules.
- **Download:** Save the poster currently shown in the preview.

The interface can say “Title”; this is the “headline” described in `skills.md`. More detailed controls for color, rotation, bars, and texture can come later.

## Decisions and open items

- Start with a portrait poster and yellow-and-black styling, while allowing other high-contrast palettes later.
- Use heavy condensed type, clear hierarchy, structural bars, and controlled rotation.
- Anton is a candidate, not a confirmed or downloaded font. Compare it with the reference before making the final choice.
- The design rules still need specific grid, spacing, and type-size measurements. Earlier suggestions of a six-column grid, 4% margins, a 1% spacing unit, and an 8:2:1 type-size ratio are proposals to test, not measured facts about the reference.
- The current `skills.md` proposes SVG artwork and editable export. These features have not been built or tested.
- References in `skills.md` to a later Tonhalle test, a single HTML page, and GitHub Pages requirements need to be checked against the later assignment instructions.

## Files and organization

| File | Status |
| --- | --- |
| `hort-nke-lebron-witness-campaign.jpg` | Reference supplied |
| `quick poster descrip..txt` | Written analysis supplied |
| `skills(2).md` | Latest supplied design-rules draft; intended project filename is `skills.md` |
| `handoff.md` | This progress record |
| `app-sketch.png` | Suggested filename for the final sketch; saving under this name is not confirmed |
| `fonts/` | Planned folder for the selected font and its license |

The local class-folder structure and GitHub uploads have not been confirmed. Do not assume those steps are complete.

## Next steps

1. Confirm that the sketch has one Generate button and save it as `app-sketch.png` in the class folder.
2. Compare Anton with the reference, choose a font, and save the font files and license in `fonts/`.
3. Finalize measurable grid, spacing, and hierarchy rules in `skills.md`.
4. Organize the reference, analysis, sketch, fonts, and both Markdown files. Confirm that the reference poster is uploaded to GitHub as required.
5. When the class reaches the building stage, use these materials to build and test the first generator.

## Instructions for the next AI session

Read this file, the current `skills.md`, the reference poster, and the sketch before continuing. Explain one manageable step at a time in simple language. Keep the generator flexible enough to create new compositions. Update this handoff as work is completed, and distinguish planned features from working features.

No working generator, verified export, or published generator site has been confirmed yet.
