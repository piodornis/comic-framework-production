# Issue 001 — Production plan

Contract: comic-production-standard-v0.1-draft
Revision: 1
State: DRAFT
Acceptance: OPEN

## Configuration

- Format/profile version and effective dimensions: OPEN (resolve project defaults)
- Reading direction, binding and page multiple: OPEN
- Total pages / cover pages / interior pages: OPEN (e.g. 24 / 4 / 20 or 32 / 4 / 28; covers included in total)
- Interior allocation: Story / full ads / mixed / editorial / blank: OPEN; no double counting of cover ads
- Default panels and preferred range: OPEN
- Printer confirmation and export specification: OPEN

## Upstream references

- Script path/revision and expected Story page IDs: OPEN
- If source is unpaginated prose: provisional budget IDs and source paragraph/revision map; accepted Story-page coverage remains OPEN
- Storyboard path/revision, protected spreads and page turns: OPEN
- Design configuration/revisions: OPEN

## Physical page map

Create one row per printed side, including covers and blanks.

| Slot ID | Position | Cover role/interior index | Type | Story reference | Panels | Override reason/reference | Ad IDs | Spread ID |
|---|---|---|---|---|---|---|---|---|

## Cover and editorial content

| Alias / slot | Function | Content/assets or OPEN | Acceptance |
|---|---|---|---|
| U1 / C1 | Front cover | Artwork, series logo, issue number, price, barcode, artist credits: OPEN | OPEN |
| U2 / C2 | Imprint or ad | OPEN; do not double-book a full-page ad | OPEN |
| U3 / C3 | Ad, merchandise or Next Issue | OPEN; choose editorial versus house ad purpose | OPEN |
| U4 / C4 | Full-page ad candidate | Advertiser/creative: OPEN | OPEN |

- Imprint location/content: OPEN.
- Opening: multi-panel, single splash or double-page splash: OPEN; title/creative-team credit placement: OPEN.
- Interior editorial slots and functions (editorial, Lettercol, highlights, credits): OPEN; allocate actual pages before including them in totals.
- If a double-page splash: both physical slots, spread/shared panel ID and owning side: OPEN.

## Advertising reservations

| Ad ID | Slot ID | Full/partial | Rectangle x/y/w/h mm | Creative reference | Asset state | Advertising kind | Constraints | Acceptance |
|---|---|---|---|---|---|---|---|---|

Advertising kind: house / third_party / OPEN.

For mixed pages add story rectangles and check non-overlap.

## Review

Budget, coverage, panels, geometry, page turns, upstream revisions: OPEN.
Record findings and affected slots; acceptance remains separate from review completion.

## Optional layout pilot links

If adopted, record the representative page/spread scope, text/asset source revisions, physical-slot-to-native-document-page mapping, lettering and correction records, printer specification and output review locations. Otherwise leave this section unused. A pilot's preparation or completion does not change this plan's acceptance state or grant print release.
