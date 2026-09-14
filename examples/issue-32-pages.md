# Generic 32-page planning example

Contract: comic-production-standard-v0.1-draft; revision: 1; state: DRAFT; acceptance: OPEN.
This is an illustrative allocation, not an accepted story or a production-ready issue.

Format: us-modern-metric v0.1; trim 170 × 260 mm; bleed 3 mm each edge; file extent 176 × 266 mm; safe inset 10 mm each edge (150 × 240 mm). Printer confirmation: OPEN.
Reading: left-to-right. Binding: saddle stitch. Page multiple: 4.
Total: 32; covers: 4; interiors: 28. Interior allocation: 26 story + 2 ad pages. Cover allocation: 1 front cover + 3 advertising cover sides. Ads therefore occupy 5 sides, but cover ads are not subtracted from interiors again.
Default panels: 5; preferred range: 3–6. Explicit Story-page overrides: S001 = 1, S008 = 7. Total story panels: 128 (24 × 5 + 1 + 7).
Upstream: S001–S026 are illustrative expected story IDs; actual script, storyboard and Design references/revisions: OPEN. Protected spreads/page turns: OPEN, must be checked with a real storyboard.

| Slot ID | Position | Cover role/interior index | Type | Story reference | Panels | Override reason/reference | Ad IDs | Spread ID |
|---|---|---|---|---|---|---|---|---|
| C1 | 1 | C1 | cover | none | 0 | none | none | none |
| C2 | 2 | C2 | cover | none | 0 | none | AD-C2 | none |
| I001 | 3 | 1 | story | S001 | 1 | Opening splash; illustrative S001 intent | none | none |
| I002 | 4 | 2 | story | S002 | 5 | none | none | none |
| I003 | 5 | 3 | story | S003 | 5 | none | none | none |
| I004 | 6 | 4 | story | S004 | 5 | none | none | none |
| I005 | 7 | 5 | story | S005 | 5 | none | none | none |
| I006 | 8 | 6 | story | S006 | 5 | none | none | none |
| I007 | 9 | 7 | story | S007 | 5 | none | none | none |
| I008 | 10 | 8 | story | S008 | 7 | Fast action sequence; illustrative S008 intent; review outside preferred range | none | none |
| I009 | 11 | 9 | story | S009 | 5 | none | none | none |
| I010 | 12 | 10 | ad | none | 0 | none | AD-I010 | none |
| I011 | 13 | 11 | story | S010 | 5 | none | none | none |
| I012 | 14 | 12 | story | S011 | 5 | none | none | none |
| I013 | 15 | 13 | story | S012 | 5 | none | none | none |
| I014 | 16 | 14 | story | S013 | 5 | none | none | none |
| I015 | 17 | 15 | story | S014 | 5 | none | none | none |
| I016 | 18 | 16 | story | S015 | 5 | none | none | none |
| I017 | 19 | 17 | story | S016 | 5 | none | none | none |
| I018 | 20 | 18 | story | S017 | 5 | none | none | none |
| I019 | 21 | 19 | story | S018 | 5 | none | none | none |
| I020 | 22 | 20 | story | S019 | 5 | none | none | none |
| I021 | 23 | 21 | ad | none | 0 | none | AD-I021 | none |
| I022 | 24 | 22 | story | S020 | 5 | none | none | none |
| I023 | 25 | 23 | story | S021 | 5 | none | none | none |
| I024 | 26 | 24 | story | S022 | 5 | none | none | none |
| I025 | 27 | 25 | story | S023 | 5 | none | none | none |
| I026 | 28 | 26 | story | S024 | 5 | none | none | none |
| I027 | 29 | 27 | story | S025 | 5 | none | none | none |
| I028 | 30 | 28 | story | S026 | 5 | none | none | none |
| C3 | 31 | C3 | cover | none | 0 | none | AD-C3 | none |
| C4 | 32 | C4 | cover | none | 0 | none | AD-C4 | none |

## Advertising reservations

| Ad ID | Slot ID | Full/partial | Rectangle x/y/w/h mm | Creative reference | Asset state | Constraints | Acceptance |
|---|---|---|---|---|---|---|---|
| AD-C2 | C2 | full | 0/0/170/260 | OPEN | reserved | inside front cover | OPEN |
| AD-I010 | I010 | full | 0/0/170/260 | OPEN | reserved | between S009 and S010; Story review OPEN | OPEN |
| AD-I021 | I021 | full | 0/0/170/260 | OPEN | reserved | between S019 and S020; Story review OPEN | OPEN |
| AD-C3 | C3 | full | 0/0/170/260 | OPEN | reserved | inside back cover | OPEN |
| AD-C4 | C4 | full | 0/0/170/260 | OPEN | reserved | back outside cover | OPEN |

## Mixed-page alternative (not included in the map above)

Convert I010 from ad to mixed only after agreeing additional Story allocation. Keep its ad ID with partial rectangle 0/200/170/60 mm; allocate story rectangle 0/0/170/190 mm, leaving a 10 mm gap. Record a new Story reference and an explicit panel target justified by the remaining space. Recalculate coverage and panel totals. Story text stays within the page safe area and the story rectangle; ad text also respects the safe inset. The page still counts once, not 1.23 pages.

## Review

Arithmetic/coverage within the illustrative map: PASS. Profile geometry: PASS as a supplied planning assumption. Actual narrative fit, lettering, printer confirmation, Design inputs, creative assets and acceptance: OPEN.
