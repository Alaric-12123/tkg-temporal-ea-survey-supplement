# Supplementary materials validation report

> **Expanded edition (23 October 2026).** The tables now cover all 43 core methods. The sections below the expansion note describe the original 35-method edition and its review; the section *Expansion to 43 methods* at the end records what was added and how it was checked.

**Date:** 23 October 2026  
**Scope:** the requested 35-method cohort and selected mechanism–experiment records; no manuscript modification, new literature search, new experiment or public release.

## Version and scope decision

The current manuscript is the modular KAIS manuscript in the latest R2 handover, with verification updates through 23 October 2026. It contains 43 core methods and a separately indexed DynEA workshop version. The requested 35-method cohort is defined by the core entries in `master_temporal_methods_matrix_H2.csv`. This export retains that cohort, uses current corrections, and explicitly identifies the eight later core additions as outside scope. It does not present the 35 records as exhaustive latest-manuscript coverage.

The source hierarchy is documented in README. Scientific content was reconciled from retained records, not reconstructed from model memory. Existing bibliographic keys were preserved. The public source mapping has **253 associations** covering every S1 method, detailed operation and S2 experiment record.

## Record counts and verification states

| S1 verification state | Rows |
|---|---:|
| Full-text evidence retained; selected operation-level trace | 6 |
| Full-text evidence retained; method-level summary | 29 |
| Total methods | 35 |

The operation worksheet has **51 records across six methods**: L1 9, L2 14, L3 16, L4 11 and auxiliary Context 1. Thus there are 50 temporal-operation records, one auxiliary dependency and 35 distinct methods in the main table. DynEA workshop is excluded from all these counts.

| S2 verification state | Rows |
|---|---:|
| Retained full-text result; protocol boundaries preserved | 33 |
| Retained full-text result; source inconsistency flagged | 5 |
| Retained qualitative evidence; numerical values not extracted | 6 |
| Total experimental records | 44 |

S2 covers **31 methods**, with **38 numeric records** (37 paired contrasts and one single-condition observation) and **six qualitative records**, including the ITEA record whose numerical aggregation is withheld. Experiment classes are Whole-pipeline Performance 7, Temporal Component Contribution 33 and Temporal Capability Validation 4. These labels do not override the row-specific limitations.

## Scientific and traceability checks

| Check | Outcome |
|---|---|
| Exact 35-method identity | Citation-key set matches the retained H2 core subset exactly; no duplicate method/key and no DynEA workshop row. |
| Layer consistency | Retained assignments preserved. L2 feature/weight construction remains separate from L3 pooling; auxiliary relation-schema alignment remains Context. |
| Decomposition depth | Six selected traces distinguished from 29 method summaries. Opaque composites and unknown internals remain explicit. |
| Current corrections | TS-align comparison-denominator verification supersedes the older uncertainty flag in both main and operation sheets. Automatic-seed predicate remains unresolved. |
| Numeric extraction | First 25 pairs exactly match the existing comparison-matrix numeric fields; additional values reconcile to the retained ablation descriptions, TREA core extraction and Phase 9.4 claims. No plot values estimated. |
| Mechanism inference | Surviving paths and objective/capacity/feedback confounds retained. No cross-paper performance ordering or pooled effect magnitude produced. |
| Protocol unknowns | Seed, query, candidate, denominator, validation and repeat uncertainties retained; missing extraction is not converted into source non-reporting. |
| Citation keys | Every S1 key resolves in current `references_kais.bib`; every S2 and operation key joins to S1. |
| DOI handling | 34 DOI fields populated from existing bibliography; STEA is Not Verified with its retained ACL Anthology URL provided. No DOI invented. |
| Publication versus inspected version | PAT-Align issue/online dates, HyDRA arXiv v1, DualMatch author v2 and T3A-LLM workshop/formal distinction retained. |
| Duplicates and missing cells | No duplicate main record IDs, duplicate mapping rows or empty mandatory cells. Explicit missing-data states are not numerical zeros. |
| Preservation | All **738 inventoried source/manuscript files** retain their pre-export SHA-256 hashes; source matrices, manuscript chapters and historical files in the inventory were not overwritten. |

## Workbook and visual checks

Both XLSX files were exported with the spreadsheet authoring library, reopened by that library, and independently read with an OOXML-compatible workbook reader. All main-sheet cells match their CSV counterparts exactly, including numeric values and citation keys. The operation sheet also matches the public operation extraction exactly.

S1 has three sheets (`S1 Taxonomy`, `Operation detail`, `Field guide`); S2 has two (`S2 Evidence`, `Field guide`). Main and operation sheets freeze the header row and two identifier columns at C2; field guides freeze the first row and first column at B2. Every sheet has a filterable table. Publication years and observed numeric values are stored as numeric cells; unknown states are text. The files contain no formulas, macros, merged cells or external workbook dependencies.

Rendered views of every worksheet were visually inspected, including the main headers, L1–L4 fields, operation trace, evidence/limitation fields, numeric columns and field guides. Wrapped text and readable widths are retained; no clipped headers, spreadsheet errors or truncated numbers were observed in the inspected views. The files are intended for scrolling, not for forcing the full wide matrices onto one printed page.

Package CRC and workbook structure checks passed. A native Microsoft Excel application was not launched, so native-application opening is not claimed as a separate test; compatibility was checked through successful export, two independent readers and the saved workbook features.

## Privacy and redistribution checks

Public CSV, Markdown and XLSX XML content was scanned for absolute local paths, internal paper IDs, private Zotero item keys, credential patterns and formula-error strings. None was found. Private row lineage and authoring/review diagnostics stay outside the public materials directory. The author-review ZIP is restricted to the seven requested files and contains no original research-paper PDF, API credential, raw access cache or private research log.

## Independent limited review and recheck

An independent review agent that did not generate the data reconciled the 35-method identity, detailed-operation scope and all 44 selected experimental records against the retained source assets. This is model-agent review, not human verification or fresh full-paper replication.

The initial review identified a minor source-locator issue and an editorial interpretation issue. TREA Table 4 locators were corrected to §§5.5–5.6, PDF p.7; PAT-Align Tables 6–7 to §§5.2.3–5.2.5; AGN Table 3 now includes §5. README and the S2 field guide explicitly distinguish capability-directed experiments from unconditional validation of a general capability.

**Final independent recheck: completed.** Both findings are closed. No open Critical, Major, Minor or Editorial finding remains within this limited review. The reviewer independently checked the main CSV/XLSX cells, operation-sheet parity, citation keys and bibliographic titles/years/DOIs, filter/freeze/wrap settings and workbook CRC. Source-preservation hashes, visual rendering and final ZIP assembly were checked by the generating agent, not represented as independent reviewer checks. The full review record is retained in the private authoring archive; the public report contains its findings, corrections and scope.

## Author decisions and retained limitations

1. Decide whether the submission should carry this explicitly scoped 35-method supplement or an expanded 43-method version. No manuscript counts or supplement cross-references were changed here.
2. Confirm the source-version boundaries, especially T3A-LLM's workshop evidence and the separate formal DOI. STEA's DOI remains unverified in the existing metadata.
3. Retain the table-specific unresolved conditions: ATEA denominator/corruption sampler; PAT-Align split; LightTEA ablation feedback; CTEA fact/pair allocation; unnamed QLGAN/ITEA experimental populations; and documented source-metric contradictions.
4. Review opaque submodules and the six-versus-29 coding-depth distinction before describing the supplement's coverage. A method-level synopsis is not a complete operation audit.

These conditions are visible evidence boundaries, not omitted rows or silently filled fields. No upload or submission was performed.


## Expansion to 43 methods (Claude, 23 October 2026)

**Added rows.** S1-36 to S1-43: Tem-EA, TEA (Liu et al.), TGA-EA, ActiveTKGA, RL-TEA, DTTEA, DynEA (formal chapter) and PAGEA. S2-045 to S2-067: 23 numeric contrasts from TGA-EA (10), DTTEA (4), DynEA formal (1), ActiveTKGA (3), TEA by Liu et al. (3) and PAGEA (2). Rows S1-01 to S1-35 and S2-001 to S2-044, the operation-detail sheet (51 records) and all existing field-guide entries other than the counts were left unchanged; IDs are stable, so the new rows are appended rather than sorted by year.

**Sources.** Publisher PDFs supplied by the author (22 October 2026 for seven papers; 23 October 2026 for PAGEA, available online 2 August 2026). Operation-level coding records: `coded_rows_a/b/c.csv` (model-agent coding from the full texts, with key equations and table values spot-checked against rendered pages) and `coding_notes_PAGEA.md` (coded directly, tables read on rendered pages 8–11). L1–L4 wording follows the manuscript's Appendix A rows.

**Counts after expansion.**

| Table | Rows | Breakdown |
|---|---:|---|
| S1 | 43 | 6 selected operation-level traces; 37 method-level summaries |
| S2 | 67 | 37 methods; 61 numeric, 6 qualitative; Whole-pipeline Performance 8, Temporal Component Contribution 55, Temporal Capability Validation 4; 8 flagged for source inconsistency |
| Source mapping | 323 associations | 253 original + 70 for the added rows (coding record, publisher PDF and bibliography for each S1 row; coding record and PDF for each S2 row) |

**Checks run on the expanded files.**

| Check | Outcome |
|---|---|
| CSV–XLSX parity | Every cell of both main sheets matches its CSV counterpart (numeric cells compared as numbers). |
| Citation keys and DOIs | All 43 S1 keys and all S2 keys resolve in the current `references_kais.bib`; titles, years and DOIs for the new rows are taken from it. STEA's DOI remains Not Verified. |
| Duplicates and empty cells | No duplicate record IDs; no empty mandatory cells. |
| Numeric values | Every value in S2-045 to S2-067 appears in the corresponding coding record, which was itself checked against the rendered source tables. No value was estimated from a figure. |
| Excluded numbers | DynEA "Without CLM" (non-monotone), TEA (Liu et al.) Digit + Time (changes digit content) and the inconsistent full-model rows of its Tables 5–6, PAGEA Table 6 base row and RL-TEA's text gains are not used. |
| Workbook structure | Table ranges extended to the new last rows (S1 A1:S44; S2 A1:AA68); header freeze and filters unchanged; publication years and observed values stored as numbers; cell styles copied from the preceding row. |
| Privacy | No absolute local paths, private identifiers or credentials in the public files; publisher PDFs are referenced by file name and hash only and are not bundled. |

**Review scope.** The original edition's independent model-agent review covered rows S1-01 to S1-35 and S2-001 to S2-044 only. The added rows were checked by the generating agent (Claude) against the coding records and rendered source tables; no separate independent review of the added rows was run, and none of this is human verification.

**Author decisions.** (1) Whether to attach these files as Online Resources and add manuscript cross-references. (2) Whether to spot-check the eight added S1 rows and the 23 added S2 rows against the PDFs in `papers/`.
