# Optional production pilot templates

These templates support the [lettering/print pilot](../../guides/lettering-and-print-pilot.md). They are experimental, opt-in working forms, not new required fields of `comic-production-standard-v0.1-draft`. No native layout or executable importer is included. Copy only the forms needed into the project's declared Production area and record deviations there.

Possible locations are project-local `production/references/previous-comic/` and issue-local `lettering/`, `artwork/`, `layout/`, `exports/review/`, `exports/print/` and `reviews/`. Keep existing paths when practical. Store reusable conventions in the project entry point and exact printer parameters in an issue-specific print specification. Decide large-file storage before importing heavy binaries; this template does not enable Git LFS.

## Forms

- [Example intake](reference-intake.md): original package, application/version, links/fonts, reference PDF and limited reuse scope.
- [Lettering CSV](lettering.csv): one row per text object, derived from Story.
- [Asset CSV](assets.csv): one row per placement, with asset revision/provenance.
- [Change CSV](changes.csv): text corrections and synchronization evidence.
- [Print specification](print-spec.md): printer-confirmed parameters and evidence.
- [Output review](output-review.md): checks and release for an exact output revision.
- [Print checklist](print-checklist.md): separate editorial, technical and delivery checks.

## CSV conventions

UTF-8, comma delimiter, header row. Quote fields containing commas, newlines or quotes; double embedded quotes. Files intentionally contain headers only. No story text or approved assets are implied.

`text_id` is stable and unique. Story page/panel IDs reuse upstream IDs; physical slots refer to the issue plan, not printed folios. For non-panel editorial text, page/panel fields may be empty with an explicit source. `reading_order` is a positive number unique within the physical page. `kind` can be narration, dialogue, thought, system, sfx or editorial. `speaker_id` is the existing character ID, or empty for narrator/editorial text; uncertain speakers remain open. `text` preserves exact wording. `source_ref` and `source_revision` identify authority; `text_status` and `approval_ref` record scope/evidence. Example local text states DRAFT/REVIEW/APPROVED are not Design states or a new universal lifecycle.

Optional `x_mm,y_mm,width_mm,height_mm` refer to the top-left trim corner of the single page. All four must be numeric and dimensions positive before position-driven import. Check bounds against the intended usage; never assume off-page text is acceptable. `paragraph_style`/`object_style` refer to actual template styles. `tail_target` is intent; final curve geometry stays in layout. Unknown values are not importable defaults.

`placement_id` distinguishes repeated uses of one `asset_id`; `file_path` is repo-relative or uses a documented external-asset reference convention. `sha256` identifies the exact bytes. `source_ref`, `status` and `approval_ref` describe provenance and demonstrated Design scope. `effective_ppi` is assessed after placement against printer requirements, not inferred solely from a file's DPI metadata.

`changes.csv` records old/new text and synchronization. Local status values may be OPEN/ACCEPTED/REJECTED/APPLIED; APPLIED means the editable Story/adaptation record, lettering list and native layout agree, with revision evidence. Published originals are preserved. A text-state label never grants print release.

The templates require an explicitly documented mapping from physical slot to native document/page before automated import. They do not yet define a complete executable layout exchange format.
