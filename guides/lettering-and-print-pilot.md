# Lettering and print pilot

Status: optional experimental guidance, 2026-09-17. The implemented contract `comic-production-standard-v0.1-draft` remains limited to planning. This guide and the pilot templates are not an executable renderer, importer, native layout template or PDF export implementation. Existing planning projects need no migration.

## Ownership

Story owns exact wording, speaker identity, narrative order and adaptation decisions. Design owns visual identity, reference roles and visual approval. Production owns physical slots, final typography, balloon geometry, assembly and export settings. The creator or explicitly authorized project workflow releases a specific delivery revision. Plan acceptance does not approve text, art or a PDF.

Upstream guidance: `comic-framework-story/schemas/lettering-handoff.md` and `comic-framework-design/schemas/production-handoff.md`. Record the source paths and revisions used by the project. The production lettering list is a derived snapshot, not an independent script.

## Pilot sequence

1. Choose a layout application and record its version. When available, preserve an existing comic package, reference PDF and prior print settings, then inspect a working copy.
2. Reconcile Story pages/panels with the physical page map. Plan text area and reading flow before finished artwork; include facing pages and ad interruptions.
3. Select a representative spread and a text-dense page. Keep this a proposal until adopted by the project; do not impose fixed page counts or dimensions.
4. Prepare exact text units from the named Story revision, stable IDs, speakers and acceptance evidence. Record unknowns rather than manufacturing text or IDs that pretend to exist upstream.
5. Produce/place artwork with the agreed lettering separation, protected visual details, provenance and design scope.
6. Assemble linked images, editable text and editable balloons/caption forms. Test typography and reading flow at actual page size.
7. Reconcile wording corrections with Story, update the derived list and layout, then review a new PDF revision. Preserve published originals and document separate adaptations.
8. Confirm current printer specifications, run appropriate technical checks and inspect the exported PDF. Record release for that exact file, not for a similarly named earlier proof.

## Image and text separation

When adopting separate lettering, artwork excludes added dialogue, narrator boxes and balloons but reserves their space. Story-relevant signs, interfaces and intentionally integrated SFX are explicit exceptions with an exact source and a plan for corrections. Never remove meaningful in-world text just to satisfy a generic text-free rule.

## Corrections and revisions

Keep text IDs stable through placement changes; record splits/merges. Distinguish normal line wrapping and geometry changes from wording changes. Log old/new text, reason, source revision and decision, then reconcile the authoritative editable Story/adaptation record, derived list and layout. Report local layout text edits before reimport. Do not overwrite published scripts or automatically shrink text to hide overflow.

A changed source triggers an impact review. New artwork or cropping can require Design/Story review; changed text or export settings invalidate the affected prior checks. Preserve reviewed delivery files and track exact revisions/checksums. Routine authorized edits do not require an additional generic approval gate.

## Tool-specific implementation

InDesign is one suitable project implementation, not a framework dependency. A project may use linked artwork, separate balloon/text layers, paragraph/object styles and nonprinting guides. Native template and scripting compatibility must be verified with its actual application/version and example files. Store trim dimensions as the page size and bleed separately; a trim-plus-bleed extent is not the document trim size.

Build automation only after the pilot establishes a usable template. [Import expectations](import-expectations.md) describe behaviors to verify before relying on an importer. No script is supplied by this increment.

## Completion evidence

The pilot succeeds when the source can be edited, text is readable at actual size, ordering and speaker attribution are clear, a correction survives synchronization, and the exported PDF has been independently checked against the selected specification. Empty folders, header-only CSVs and unchecked checklists are preparation, not completion.

Use [pilot templates](../templates/production-pilot/README.md) only when relevant. Universal final-asset status enums and a stable machine interchange schema remain deferred pending evidence from actual use.
