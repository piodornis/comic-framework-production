# Issue 001 — Production plan

Contract: comic-production-standard-v0.1-draft
Revision: 1
State: DRAFT
Acceptance: OPEN

## Configuration

- Format/profile version and effective dimensions: OPEN (resolve project defaults)
- Reading direction, binding and page multiple: OPEN
- Total pages / cover pages / interior pages: OPEN
- Default panels and preferred range: OPEN
- Printer confirmation and export specification: OPEN

## Upstream references

- Script path/revision and expected Story page IDs: OPEN
- Storyboard path/revision, protected spreads and page turns: OPEN
- Design configuration/revisions: OPEN

## Physical page map

Create one row per printed side, including covers and blanks.

| Slot ID | Position | Cover role/interior index | Type | Story reference | Panels | Override reason/reference | Ad IDs | Spread ID |
|---|---|---|---|---|---|---|---|---|

## Advertising reservations

| Ad ID | Slot ID | Full/partial | Rectangle x/y/w/h mm | Creative reference | Asset state | Constraints | Acceptance |
|---|---|---|---|---|---|---|---|

For mixed pages add story rectangles and check non-overlap.

## Review

Budget, coverage, panels, geometry, page turns, upstream revisions: OPEN.
Record findings and affected slots; acceptance remains separate from review completion.
