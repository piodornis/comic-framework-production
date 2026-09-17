# comic-framework-production

Reusable comic issue planning, followed by future asset production, assembly, lettering and export. Project-specific content stays in the comic project repository.

## Current scope

This initial foundation defines **comic-production-standard-v0.1-draft** for format selection, page budgets, per-page panel planning and advertising reservations. It is an experimental planning contract, not a released v1 or a working renderer/exporter. No Skills are implemented or installed yet.

Compatible upstream inputs: `comic-project-standard-v1` and `comic-design-standard-v1`. Production owns physical allocation; Story owns narrative pacing, panel intent and text; Design owns approved visual identity.

## Repository structure

- `schemas/` — normative draft planning rules, project structure and review checks
- `format-profiles/` — reusable dimensional starting points, subject to printer confirmation
- `templates/comic-project-production/` — project entry point and issue planning template
- `examples/` — generic worked issue, without project canon
- `skills/` — implementation roadmap, no executable Skills yet

See [Publication structure](schemas/publication-structure.md) for U1–U4 cover functions, imprint, splash/credits, advertising categories and editorial options.

## Start here

1. Read [planning rules](schemas/issue-production-schema.md).
2. Select a [format profile](format-profiles/README.md) or define a custom one.
3. Add the [production entry point](templates/comic-project-production/production-project.md) to your comic project.
4. Copy the issue template and allocate covers, story, ads and other pages before scripting against the remaining story budget.
5. Link story pages to physical slots, record panel overrides and review page-turn impacts with Story.
6. Follow the [review checklist](schemas/planning-review.md). Try the [32-page example](examples/issue-32-pages.md).

The total page count is configurable. The examples cover [24 pages](examples/issue-24-pages.md) and [32 pages](examples/issue-32-pages.md); these include four cover sides. Neither is a fixed framework default. Other totals are allowed when the chosen binding/page-multiple constraints hold.

Working defaults are proposals, not creator approval or printer specifications. No automatic commit, push, publication or installation. Git is the primary history; preserve upstream sources and unrelated work.

## Optional lettering and print pilot — 2026-09-17

[Lettering and print pilot](guides/lettering-and-print-pilot.md) connects Story wording, Design inputs, layout corrections and print review. [Pilot templates](templates/production-pilot/README.md) provide intake, lettering, assets, changes, print specifications and review forms. [Import expectations](guides/import-expectations.md) describe future implementation checks.

These are opt-in experimental guidance and blank forms, separate from the normative v0.1 planning contract. No new required project fields, universal final-asset status model, native InDesign template, executable importer or verified PDF export are introduced. The layout application and printer settings remain project choices.
