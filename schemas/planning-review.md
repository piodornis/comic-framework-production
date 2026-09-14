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

Negative cases to check during implementation: 31 pages with a multiple of four; duplicate/missing position; unmapped Story page; ad on a protected spread; zero panels on a story page; mixed area overlap; conflicting profile dimensions. Future automation must report these rather than silently repair content.
