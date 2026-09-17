# Future layout import expectations

Status: specification for a pilot implementation, not an existing script or validated API integration.

## Inputs and validation

Require a named source revision, a selected native template, known styles, explicit units and a physical-slot-to-document-page map. Cover files may be separate: record document identity and page identity rather than assuming physical reading position is the application page number. Check unique text/placement IDs, source references, existing assets, speaker references, required styles and adopted geometry before production import.

Optional CSV templates use UTF-8 and standard comma-separated quoting. Use a CSV parser, not string splitting. Coordinates are millimetres from the top-left trim corner of each page, not the spread. Convert explicitly to the application's units/origin. Empty/OPEN fields indicate missing information, not literal content to import. A preliminary probe may omit geometry; a position-driven import requires complete valid rectangles and an explicit crop/fitting policy.

## Behavior

- Begin with a readable dry-run report and a working copy or saved revision.
- Use stable object labels/IDs to distinguish managed objects from manual work.
- Separate first placement from text-only update; repeated imports must not duplicate objects.
- Preserve manually adjusted positions, balloon outlines and tails during text updates.
- Detect changed local wording and report conflicts before overwriting.
- Report unknown pages, missing links/fonts/styles and text overflow rather than silently substituting, skipping or shrinking.
- Make partial failure visible and recoverable; record which objects changed and preserve the pre-import version.
- Do not equate a successful import with PDF readiness or trigger release/ordering automatically.

## Verification cases once implemented

Test initial placement, repeat import without duplication, source wording update with preserved geometry, local wording conflict, missing asset/style, unresolved page map, text overflow, CSV punctuation/newlines and recovery after a failed operation. Visually inspect both the native document and its exported proof. These checks are deferred until a real importer exists.
