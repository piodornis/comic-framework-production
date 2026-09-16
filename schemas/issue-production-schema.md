# Issue production planning — v0.1 draft

Contract: `comic-production-standard-v0.1-draft`. These are normative rules for this draft only. Markdown records are human-reviewable; no machine validator is provided yet.

## Configuration and precedence

Resolve format from the issue's chosen profile/version plus explicit issue overrides, otherwise the project profile/version plus project overrides. An issue profile selection replaces the project format as a whole; never combine dimensions silently. Store the effective trim, bleed and safe-area values in the issue record, with their source. Printer-confirmed values become explicit versioned overrides; a discrepancy is reported before adoption.

For panels, resolve explicit page override, then issue default, then project default. Defaults are targets, not a hard capacity. Record the effective integer panel count for every story-bearing page. Storyboard differences require reconciliation with Story, never automatic splitting or deletion of panels. A deliberate override needs a reason and upstream reference; numbers outside a configured preferred range require review, not automatic rejection. Pure ad, cover, editorial and blank pages have zero story panels. A single-page splash has one panel. For a shared double-page splash, the non-owning side may have zero local panels only with an explicit reference to the shared panel; see [Publication structure](publication-structure.md). Panel count alone does not prove readable layout.

## Required issue fields

- Stable issue ID, draft contract, plan revision and review state.
- Profile ID/version or custom format; effective dimensions in mm; reading direction.
- Binding and page-count multiple (positive integer, configured for this product).
- `total_pages`, `cover_pages`, `interior_pages`; all integers, total positive.
- Positive `default_panels_per_story_page`; optional preferred minimum/maximum.
- Sources: script/storyboard paths and revisions, relevant Design configuration/revisions; unresolved inputs explicitly OPEN.
- Complete physical page map; ad reservations; exceptions and review findings.
- Printer confirmation state and source; export requirements can remain OPEN during planning.

## Counting

A page is one printed side, not a sheet or spread. `total_pages = cover_pages + interior_pages`. All cover sides, blanks, ads and editorial pages count. Require `total_pages % page_count_multiple = 0`. The supplied saddle-stitch planning example uses four cover sides and a multiple of four; this is not a universal binding rule. For other bindings/digital editions choose explicit printer/product constraints rather than assuming the example applies.

## Configurable extent and planning before Story pagination

`total_pages` is an issue choice, not a fixed 32-page default. A saddle-stitch planning profile with four cover sides and a multiple of four can represent 24 pages (4 cover + 20 interior), 32 pages (4 + 28), or other compatible totals. Confirm actual printer limits separately. Distinguish total pages from interior pages explicitly in intake: “24 interior pages plus 4 cover sides” is a 28-page product.

For example, 24 total = 4 covers + 16 story + 2 full interior ads + 2 editorial pages. Cover ads remain included in the four covers. Editorial pages are optional project choices; removing them changes the available Story budget. A format profile never determines the issue extent.

When the upstream source is prose without accepted Story page IDs, Production may allocate provisional budget IDs and link each to source paragraphs at a recorded revision. Mark them as proposals and keep accepted Story-page coverage OPEN. They are not Story pages or a substitute for a storyboard. Source paragraph coverage can be checked independently. Story owns acceptance/adaptation of the proposed distribution, dialogue and staging; Production must not edit the published prose to make its budget fit.

Each physical slot is present exactly once and has one type: `cover`, `story`, `ad`, `mixed`, `editorial`, `blank`. The sum of type counts equals total pages. Mixed pages count once as physical pages and once as story-bearing pages; track fractional ad area separately, never subtract it as another whole page. Cover ads remain cover pages and are counted through the ad reservation table.

## Physical page map

Required columns: stable slot ID, reading-order position (1..total), cover role or interior index, type, story page ID/reference (or none), effective panels, override reason/reference (or none), ad slot IDs (or none), spread ID (or none).

For four cover sides, reading order is C1 front outside, C2 front inside, I001..I(N), C3 back inside, C4 back outside. Reading-order position is distinct from optional printed folio and from Story page number. Cover roles are unique. Preserve stable IDs when inserting advertising; update positions without renaming Story references. Every expected Story page must be mapped exactly once, unless an explicit approved split/spread mapping records all related slots.

For left-to-right bound reading with C1 at position 1, a facing spread starts at an even position and ends at the next odd position. Right-to-left products require an explicit pairing convention. Spreads consume two physical pages and require an explicit panel allocation per side; a cross-gutter panel has one owning side/ID and a reference on the other side, so it is counted once. Do not place an ad within a protected narrative spread or between a declared page-turn setup/payoff without an explicit Story revision decision.

## Advertising

Each reservation records ID, physical slot ID, full/partial area, rectangle in trim-relative mm (`x`, `y`, `width`, `height`), creative asset/reference or OPEN, asset state (reserved/supplied), placement constraints, and content acceptance reference or OPEN. A reservation is not an approved or print-ready asset.

Rectangles have positive dimensions and lie inside trim. Full-page art may additionally extend through the configured bleed. Separate ad rectangles may not overlap. On mixed pages, specify non-overlapping story and ad rectangles; sum of rectangle areas must not exceed trim area, and text remains within safe area. Geometric checks do not replace visual review. Ads may be reserved on C2/C3/C4 explicitly; C1 requires an explicit editorial decision. Do not assume all cover sides are available for ads.

## Publication functions

Use [Publication structure](publication-structure.md) for U1–U4 aliases, cover elements, imprint/preview allocation, house versus third-party ads, editorial options and splash/credits handling. These options do not prescribe 32 pages or override an explicit issue budget. Existing cover IDs C1–C4 remain stable.

## Changes and authority

Changing format, page count, ads or panel allocation requires recalculating the budget and reviewing affected Story references, facing spreads, page turns, lettering space and downstream assets. Do not compress the story to accommodate advertising silently. Record unresolved capacity conflicts and proposed remedies in the issue plan.

Planning review states: `DRAFT`, `IN_REVIEW`, `ACCEPTED`, `SUPERSEDED`. Acceptance records decision source, scope, revision and date and requires creator authorization. Arithmetic review does not accept a plan. A changed accepted plan becomes a new DRAFT revision; prior acceptance remains historical. These states apply only to planning, not rendered assets, canon, Design approval or press readiness.
