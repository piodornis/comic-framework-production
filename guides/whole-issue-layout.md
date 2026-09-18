# Whole-issue rough layout and reusable page treatment

Status: optional experimental guidance, 2026-09-19. This extends the [lettering pilot](lettering-and-print-pilot.md); it does not change the v0.1 planning contract, install a renderer or require migration. Adopt the desired rules in a project-local [layout profile](../templates/production-pilot/layout-profile.md). Project instructions take precedence over proposed defaults.

## Assemble the whole issue

After a representative pilot, build a complete editable rough issue in physical reading order, including cover sides, ads and editorial matter. Populate known text and existing suitable panel art. Missing images get labeled placeholders with panel IDs; full staging notes may remain in a separate gap list when the frame is too small. Never replace missing content with invented dialogue, publisher details or advertisements.

Provide a native editable document, a reading PDF and a page/panel gap list. Record missing art, provisional art, requested replacements and unresolved text/content separately. A positive review of the rough result is not final approval of every asset. Use stable IDs to request later replacements and preserve manual edits when updating the document.

## Adoptable panel and caption treatment

- Artwork covers the entire panel rectangle with proportional cover fitting and clipping. Do not stretch images or reserve an unillustrated band for captions. Recompose the image if the required crop hides important content.
- For narrator-led pages, a single-caption-per-panel treatment avoids accidental duplicate boxes. Merge consecutive narrator passages in reading order with an ID mapping. Dialogue, separate speakers, intentional document text and other explicit exceptions retain their declared roles. Never duplicate a quotation in both image and overlay text.
- Captions are editable overlays above artwork. Define their origin relative to the panel, width, inset, border, fill and typography independently. For a top-left outward offset `d`, use `caption_x = panel_x - d` and `caption_y = panel_y - d`; this changes the box origin, not its internal padding. Example: `d = 2 mm` after adoption by the project, not a universal requirement.
- Record whether a requested further offset is incremental or an absolute replacement; store the resulting final coordinates, not only the last delta. Check page-safe bounds and neighboring panels after offsetting.
- Choose an available font family/style and test actual-size wrapping. Do not assume a previous comic grants a font license or choose an automatic substitute. Exact typeface, point size, leading and millimetre offsets are project values. Do not shrink lettering automatically to hide overflow.
- Inspect the actual image crop with the final text overlay. Preserve important faces, gestures, objects and clues. Measure caption pressure and report cramped panels without declaring a universal maximum area ratio.

## Interior numbering and folio panels

Map physical position, interior index, Story ID and displayed folio separately. In the adoptable treatment used here, covers have no displayed folio; interior counting starts at 1, includes interior advertisements, and suppresses their visible numbers. Make the counting policy explicit: hidden folios do not silently remove pages from the sequence. Other project policies may be selected.

Use automatic native page-number markers where available, with a configured interior numbering section. Put the folio in a small centered opaque panel, using the caption font family/style/size and a compatible border. For the half-overlap variant, with page width `W`, box width `w`, box height `h`, and lower panel edge `y_bottom`:

- `x = (W - w) / 2`
- `y = y_bottom - h / 2`

The upper half covers the image and the lower half lies below its edge. Keep it above artwork in the stacking order. With two lower panels it may bridge the gutter; verify both sides remain readable. On a numbered editorial page without a story panel, define an explicit matching content-bottom anchor. Check trim/safe-area clearance and protected image details; an intentional overlap is not permission to collide with text or fall outside the page. Exact dimensions and anchor positions remain project choices.

Exclude diagnostic headers, raw slot IDs and revision footers from a clean reading export when requested. Keep traceability in native object labels, manifests and separate reports. Distinguish intentionally visible missing-art labels in a rough proof from production metadata; do not indiscriminately delete both.

## Editorial consolidation and opening pages

A separate title/imprint page is not mandatory. With a creator decision, credits/imprint may share a closing editorial/knowledge page using explicit, non-overlapping areas. Keep unknown publisher/contributor information visibly unresolved; assigning a location does not certify legal completeness.

If this frees an interior slot, update the budget, slot type and Story mapping. An opening splash may redistribute existing introductory text without adding a new plot event. Preserve the original text once in reading order. Verify facing pages and the positions of ads, reveals and ending; do not assume these stayed fixed merely because total page count did.

## Editable delivery and correction loop

Keep images linked and replaceable, text in native editable frames, and caption/panel/folio styling independently adjustable. Supply linked assets with the native document and an interchange copy where supported. Record font requirements; do not redistribute font files without the appropriate rights. Preserve previously reviewed revisions.

Differentiate successful script execution, native document creation, native overflow/link checks, and visual inspection of an exported PDF. None substitutes for another. Compare source and placed text for omissions/duplicates; any normalization for whitespace or ligatures must be documented and must not conceal wording/punctuation changes. Verify all intended folios and all suppressed pages, actual font/size, caption geometry and fit, and the final asset crop. Recheck affected pages after changes.

A rough layout can intentionally contain labeled missing content. Deliver it as a rough layout with an actionable gap list, never as a print-ready issue. The [output review](../templates/production-pilot/output-review.md) records evidence and outstanding work.
