# MOR Biased Signaling Atlas

Interactive bilingual research atlas for the study *Mapping μ-Opioid Receptor Biased Signaling: An Integrated Bibliometric, Assay-Level, and Scaffold-Based Analysis*.

Authors: Bo Chen, Yizhou Liu, Chengyi Wang, Tao Chen, Xiao Wang. The First Hospital of Jiaxing.

## Current evidence release

The 2026-10-15 source bundle contains 257 included publications, 375 compound records, 408 assay records and 142 excluded publications. Of these compounds, 373 enter the 28-family scaffold classification. The 202 publication–family pairs correspond to 151 distinct substantive publications.

Literature search cutoff: 2026-08-25. Clinical evidence cutoff: 2026-10-03. Clinical status is the supplied S5 snapshot, not a live regulatory feed.

## Explore

- Chinese: `index.html`; English: `en.html`.
- Compare 28 families by compound count, linked publications, or scaffold diversity and research activity.
- Select a heatmap cell to open its family/year literature subset.
- Search compounds, publications, assay records, 22 advanced clinical records, or exclusions.
- Open records for source workbook, sheet and row, original fields, associated papers and evidence URLs.
- Export the complete filtered subset to UTF-8 CSV. Values beginning with spreadsheet formula characters are escaped for safe spreadsheet import.
- Language links retain the active search filters. A query URL can reproduce a filtered view.

## Source reconciliation

Data come from the five supplied supplement workbooks S1–S5. `evidence-data.js` preserves original fields alongside normalized display fields and provenance. `search-history.txt` retains the supplied search log.

The 28-family classification replaces the previous 29-family version. BMS-986122 and BMS-986187 are allosteric modulators excluded from direct-agonist scaffold comparisons. Old family IDs must not be joined to this release.

Family publication totals and annual heatmap cells count unique article–family links in S3, matched to S4 by article number, UT and year. Six family summary counts differ from those validated links. Original summary values remain available in the dataset. Two bias-summary cells and one legacy allosteric audit mapping also conflict with the current record-level classification; normalized values use the current detailed records. Nine discrepancies are retained in `MOR_EVIDENCE.issues`.

The scatter x-axis preserves the supplied S5 scaffold-diversity metric; y is log10(verified linked publications + 1). Bubble area scales with compound count. The highest stage of a family does not describe every compound, and conventional drug maturity is distinct from bias-led development.

## Running and publishing

This is a dependency-free static website. Serve this directory with any static HTTP server, for example `python -m http.server 8766`, or publish the repository root through GitHub Pages. Both language editions share `app.js`, `styles.css`, `interactions.css`, and the same evidence dataset.

No accounts, tracking scripts, or third-party frontend libraries are used. Source publications and clinical evidence open through explicit links.

## Interpretation

Dataset membership does not establish signaling bias. Bias depends on reference agonist, cellular context, assay platform and analytical model. Reported EC50/Emax values retain their original units and are not ranked across assay systems. This atlas is for research exploration, not individual treatment decisions.
