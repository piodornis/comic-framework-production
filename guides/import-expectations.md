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

## Additional native-layout verification from rough-issue work

- Preserve the live editable document when producing a new revision; reconcile local changes before rebuilding from older exported data. Use a working copy rather than overwriting the reviewed source.
- Treat script encoding and data encoding explicitly. Verify non-ASCII text, quotation marks and symbols in the exported result, not only the source file. An ASCII-escaped script or correctly declared Unicode script may be used as supported by the application.
- When replacing text, replace the complete intended story/text object, including overset content. Some frame-range operations can leave an old tail behind; test long-to-short replacement and inspect the result.
- Apply proportional cover/clipping and separate editable overlays according to the adopted profile. Updates must preserve approved manual geometry unless the requested change targets it.
- Check automatic folios against interior numbering, cover/ad exclusions, font size, centering and overlap geometry. Remove diagnostic headers by stable labels, not by deleting arbitrary text with a similar word.
- Do not infer native-file success from a script file existing. Verify saved native/interchange outputs, normal asset links, available fonts, no unintended overset and an independently rendered proof.

These are implementation checks, not claims of an included executable importer. API details remain application/version-specific.
