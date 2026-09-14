# Format profiles

Starting points transcribed from the supplied `comics_aufbau_anforderungen.txt`, not independently verified printer specifications. Two variants prevent rounded metric dimensions and exact inch conversion from being silently mixed.

| Profile (version 0.1) | Trim mm | Bleed each edge mm | File extent mm | Centered safe area mm |
|---|---|---|---|---|
| us-modern-metric | 170 × 260 | 3 | 176 × 266 | 150 × 240 |
| us-modern-inch | 168.275 × 260.35 | 3 | 174.275 × 266.35 | 148.275 × 240.35 |

The metric profile reproduces the supplied metric dimensions. The inch profile converts 6.625 × 10.25 inches using 25.4 mm/inch and deliberately retains a 10 mm safe inset; its safe area is derived, not quoted from the attachment. Do not label either variant printer-confirmed.

Custom profiles record ID, version, source, trim width/height, bleed per edge, safe insets per edge and confirmation state. All dimensions are mm; trim must be positive, bleed/insets non-negative, and remaining safe width/height positive. File extent equals trim plus opposing bleed values. Safe extent equals trim minus opposing safe insets. Profile selection does not fix page count or panel count.

The attachment also suggests CMYK with printer-agreed profile, 300 dpi for color, 600–1200 dpi for lineart, and sequential single-page PDF/X-3 or PDF/X-4 delivery. Keep these as intake notes until the chosen printer confirms profile, resolution, PDF variant, binding, page multiple and whether covers require a separate file. The attachment's approximate 64-page binding transition is not enforced as a universal rule. Export/preflight implementation is deferred.
