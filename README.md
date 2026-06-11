# Geotech Report Analyser — AS 2870

A self-contained, **fully client-side** browser tool that reads a geotechnical report PDF and extracts
the key parameters a building surveyor / engineer needs into an **editable summary**, then exports a
branded "Comps" summary PDF.

**🔒 Private:** the PDF is read entirely in your browser via pdf.js — **nothing is uploaded** anywhere.
No server, no API key.

## Run it
Open `index.html` in any browser. Keep `logo.js` alongside it for the PDF header. (pdf.js and jsPDF
load from CDN the first time, then cache.)

## Use it
**Drag &amp; drop** a geotechnical report PDF onto the drop zone (or click to choose). It extracts and
presents, each editable with the source snippet and a ✓found / ⚠not-found marker:

- **Classification &amp; reactivity** — AS 2870 site class (A/S/M/M-D/H1/H2/E/P), characteristic surface
  movement ys, soil reactivity, climate zone.
- **Footings &amp; bearing** — recommended footing system (raft/waffle/strip/pad/pier/pile), founding
  depth, allowable bearing pressure, founding material.
- **Soil profile &amp; groundwater** — strata summary, fill, groundwater.
- **Investigation &amp; durability** — boreholes / test pits / CPTs, concrete exposure classification.
- **Report metadata** — reference, date, geotechnical consultant, client, site address.

Plus **hazard &amp; condition flags** scanned across the text: reactive/expansive, fill, acid-sulfate,
salinity, slope/landslip, contamination, asbestos, soft/compressible soils, rock/rippability,
settlement.

A collapsible **full extracted text + search** lets you check anything the parser didn't surface.

## Important
This is a **pattern-based extraction aid, not a substitute for reading the report**. Geotechnical
reports vary widely in wording and layout, so some items may be missed or mis-read — **verify every
field against the original report, which governs**. Site classification, footing design, bearing
capacity and durability are to be taken from the report and AS 2870 / AS 3600 by the responsible
practitioner. Scanned / image-only PDFs have no selectable text and will need OCR first.
