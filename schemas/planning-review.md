# Planning review

Report each check as PASS, FAIL or OPEN with evidence. A plan can be useful with OPEN printer or creative inputs; it must not be called print-ready.

1. Effective profile values are internally consistent; metric/inch variants are not mixed.
2. Total = cover + interior, chosen page multiple holds, and every physical position occurs exactly once.
3. Cover roles/interior indices and stable IDs are unique; type counts sum to total.
4. Story references have complete coverage without unexplained duplicates or omissions.
5. Panel inheritance is resolved; every exception is explained; non-story pages have zero story panels.
6. Every ad reservation resolves to a page; every page's ad ID resolves back to its reservation. Asset and acceptance gaps remain explicit.
7. Ad/story rectangles fit without overlap; safe area, lettering space and reading order receive visual review.
8. Protected spreads and page-turn intent survive ad insertion and page remapping.
9. Upstream revisions and plan acceptance scope are recorded; accepted source changes cause an impact review.

Negative cases to check during implementation: 31 pages with a multiple of four; duplicate/missing position; unmapped Story page; ad on a protected spread; zero panels on a story page without a valid shared-panel reference; mixed area overlap; conflicting profile dimensions. Future automation must report these rather than silently repair content.

10. Cover aliases U1–U4 resolve to C1–C4 without duplicate pages. Cover elements and imprint placement are resolved or OPEN; prices, barcodes and credits are not invented.
11. Full-page ads do not compete with imprint/preview content on the same slot. Shared uses have explicit non-overlapping geometry; house/third-party classification may remain OPEN.
12. Splash/credits stay inside the existing page budget. A double-page splash consumes two facing pages but one unique shared panel, with an explicit reference on its zero-local-panel side. An unexplained zero-panel story page still fails.
13. Editorial functions and ad totals distinguish interior from cover allocation; supplied page ranges are reconciled to one actual total.

## Boundary to output review

Planning PASS or ACCEPTED does not approve the final text, artwork, lettering or print file. Projects performing a layout pilot can use the separate [print checklist](../templates/production-pilot/print-checklist.md) and [output review](../templates/production-pilot/output-review.md). These optional forms do not extend the plan-state lifecycle.
