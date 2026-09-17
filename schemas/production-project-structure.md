# Production project structure — v0.1 draft

Read `project.md`, `design-project.md` and `production-project.md` for broad planning work; for focused revisions inspect the relevant issue plan and linked current sources.

```text
comic-project/
├── project.md
├── design-project.md
├── production-project.md
├── issues/issue-001/                  # Story-owned script and storyboard
└── production/issues/issue-001/
    └── production-plan.md            # physical allocation and ad reservations
```

`production-project.md` owns production defaults and issue-plan links. Each plan owns its issue overrides and physical page map. Profile definitions remain reusable; store the selected version and effective dimensions with the project so future profile revisions cannot silently alter an issue. Document alternate paths in the entry point.

Normative rendering-asset directories, export manifests and large-file storage remain deferred. Projects may opt into the [lettering/print pilot](../guides/lettering-and-print-pilot.md) and [experimental templates](../templates/production-pilot/README.md), documenting local reference, lettering, artwork, layout, export and review paths in their entry point. These optional paths do not change the required planning structure. Do not treat a plan or prepared folders as a rendered or print-ready comic. No migration of existing Story or Design records is required.
