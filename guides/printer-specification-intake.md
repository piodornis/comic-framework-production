# Printer specification and legacy-layout intake

Optional pilot guidance, 2026-09-17. This does not expand the required v0.1 planning contract or establish a universal printer preset.

## Evidence and scope

For each researched parameter, record value/unit, source URL or file, retrieval date, relevant country shop, product/binding/paper scope and confirmation state. Distinguish:

- provider-published information applicable to the stated scope;
- project proposals and mathematically derived values;
- unresolved values or contradictory sources;
- requirements confirmed for the exact selected order/configuration.

These are evidence labels, not canon, Design or planning lifecycle states. A website statement is not proof of an order-specific agreement. Do not mark a whole specification confirmed because some individual values are supported.

Use the exact product/configuration datasheet or written order-specific clarification as the primary technical source. General product pages and FAQs provide preliminary evidence. Another product, country shop, prior order or third-party mirror cannot silently establish requirements for the current job. If applicable official sources conflict, record both, explain their scopes and leave the disputed parameter unresolved pending clarification; do not choose the most convenient number.

## Project-owned printer records

Store provider research, configuration evidence, actual datasheets and export presets inside the comic project, with the effective issue specification linking them. Keep historical requirements for the old example separate from newly researched requirements for the next comic. Do not rewrite a reusable format profile merely because one printer asks for different bleed.

Before final output, confirm the exact product, closed trim size, binding, total versus interior/cover counts, stock, color configuration and quantity. Then resolve per-edge bleed/gutter treatment, safe area, PDF version, color profile/output intent, ink limits, marks, page order and cover-file arrangement. A proposed special size or paper combination is not verified availability until supported by the chosen configuration.

Changing a format assumption is an explicit versioned project/issue override. Compare old and proposed values, record the source and decision, and reconcile plan, native layout and output checks before release. Research alone must not silently alter accepted layouts or Story pagination.

## Native document versus reference PDF

Record the exact files/revisions or checksums and compare independently:

- native/exchange-file page count, each page's actual dimensions and bleed values;
- PDF page count and each page's TrimBox, BleedBox and MediaBox coordinates/dimensions;
- whether boxes are explicitly present, inherited or merely supplied as reader fallbacks;
- embedded output-intent identity and declared PDF/X metadata, separately from validation results;
- fonts and linked assets, separating recorded metadata from current availability checks.

Compute rectangle width as right minus left and height as top minus bottom; do not interpret an upper-right coordinate as a page dimension. A matching filename does not prove matching revisions or geometry. An exchange format's DOM/version metadata is not proof of the currently installed application version. Recorded font status is not a live font check. A PDF/X metadata string alone is not evidence of PDF/X conformance.

If dimensions or bleed differ, preserve both originals and report the mismatch before deriving a production template. Determine whether differing revisions, intentional cropping, export settings or another cause explain it; do not infer the cause or “repair” files without evidence. Rendered appearance supplements these checks but cannot prove technical conformance.

## Resolution and geometry

Evaluate raster resolution at the final placed size. Changing only a DPI tag does not add detail. Keep vector text/balloons distinct from raster artwork. Convert pixel requirements from the chosen physical dimensions explicitly and label the result as a calculation.

Trim plus opposing bleed values defines a bleed rectangle, not necessarily the entire PDF MediaBox when marks/margins exist. Configure native page trim and bleed separately. Keep a project's generous lettering inset unless explicitly changed; a printer's minimum safety distance is not automatically a typography target.

## Next step

Record missing evidence and a concrete next action. A first researched specification can be delivered with OPEN values, but no final preset, validated PDF, release or order is implied. Use the [print specification template](../templates/production-pilot/print-spec.md) and [reference intake](../templates/production-pilot/reference-intake.md).
