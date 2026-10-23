# Supplementary materials for C1 and C2

**Manuscript:** Temporal Modeling for Entity Alignment in Temporal Knowledge Graphs: A Survey and Taxonomy  
**Prepared:** 23 October 2026 (35-method edition by Codex; expanded to 43 methods by Claude the same day)  
**Scope:** all 43 core methods of the current manuscript: the 35 retained core methods (S1-01 to S1-35), the seven methods whose publisher full texts were coded on 22 October 2026 (S1-36 to S1-42) and PAGEA, added by the DBLP recall check and coded on 23 October 2026 (S1-43). The DynEA AIDEM 2025 workshop version, which the manuscript indexes separately, is not a row.

## Contents and units of observation

| File or worksheet | Unit | Records |
|---|---|---:|
| Supplementary_Table_S1_Taxonomy.csv / XLSX `S1 Taxonomy` | One core method, with version and variant qualifications | 43 |
| XLSX `Operation detail` | One retained operation or auxiliary dependency within a specified variant | 51 |
| Supplementary_Table_S2_Evidence.csv / XLSX `S2 Evidence` | One selected experiment or within-paper contrast; some qualitative records summarize a figure experiment | 67 |
| supplementary_source_mapping.csv | One association between an output record and a source asset | See validation report |

The CSV files reproduce the two main worksheets. The S1 workbook additionally preserves the existing detailed operation records and a field guide; the S2 workbook includes a field guide. The operation detail is not 51 additional methods. Numeric cells in S2 are searchable and editable values; the descriptive result field retains their interpretation. No cross-paper ranking or pooled effect estimate is supplied.

## Contribution C1: operational taxonomy

S1 preserves the four-layer output-and-use rule:

- **L1, Temporal Input Representation:** temporal support and symbolic organization, including timestamp identities, intervals, endpoints and unknown-time symbols.
- **L2, Temporal Feature Encoding:** numerical features, transformations, affinities and attention weights.
- **L3, Temporal Information Fusion:** pooling or combining feature, message, score or contextual evidence. Pooling within one temporal channel also belongs here.
- **L4, Temporal Alignment and Matching:** cross-graph entity comparison, candidate filtering, correspondence decisions, transport and pseudo-seed selection.

These are operation roles rather than a mandatory execution sequence. A direct pair score (L4) can enter a score mixture (L3) before another matching decision (L4). Prediction feedback can modify supervision or reconstruct input support. Training objectives constrain the operations they train and are not a fifth layer. The one `Context` row in the operation sheet records MGTEA's auxiliary relation-schema alignment; it is excluded from the 50 temporal-operation count.

Six methods have selected detailed traces: TEA-GNN (9 records), TS-align (4), FTFS (6), HyDRA (10), MGTEA (12, including the Context row) and HTEA (10). The other 37 records are method-level summaries, including all eight added methods. Even a detailed trace does not imply exhaustive decomposition of every implementation primitive. Opaque composites, including sequence encoders and proxy modules, retain their unresolved internal roles.

`Publication Year` follows the existing consolidated bibliographic record. PAT-Align has a 2027 issue year and a 2026 online publication; HyDRA uses arXiv v1. T3A-LLM retains the stable key and DOI for the 2026 formal chapter, but its technical evidence is explicitly the inspected 2025 workshop text. DualMatch uses author preprint v2 linked to the formal publication. A DOI identifies the bibliographic work and does not establish technical equivalence between versions.

STEA has no DOI in the retained consolidated bibliography; its DOI cell is therefore `Not Verified`, and its existing ACL Anthology URL is provided in the source-location field. This does not assert that the work has no assigned DOI.

## Contribution C2: mechanism–evidence correspondence

S2 links interventions to removed operations, surviving temporal paths, observed outcomes and the inference supported by the design. Its 67 records cover 37 methods. Records S2-001 to S2-044 come from the retained extraction; S2-045 to S2-067 come from the publisher full texts of six added methods. The 67 records comprise:

- **Whole-pipeline Performance (8):** system outcomes, wider configuration changes, or perturbations outside the timestamp channel. These records do not isolate a temporal component.
- **Temporal Component Contribution (55):** the contribution of a named temporal path or module in its reported configuration. Remaining temporal routes, changed feedback and protocol gaps limit attribution.
- **Temporal Capability Validation (4):** three ATEA corruption contrasts and one TREA future-time observation. The category identifies a capability-directed intervention, not an unconditional endorsement of the metric or a general capability guarantee. ATEA's corruption operator and output denominator remain unresolved; TREA's inference is specific to its cutoff and unseen-input protocol.

There are 61 records with numeric observations and six with qualitative evidence. The eight records flagged for source inconsistency (five retained, plus DynEA formal and two PAGEA rows) preserve reported Hits@1 values together with conflicting companion metrics, prose or version evidence. They are unsuitable for an unqualified effect-size synthesis. S2 selects contrasts useful for C2; it is not an exhaustive inventory of every experiment in the 43 papers. EAMLLM, TimeGate, TKGA-RP and TEA (multi-source, Zhu et al. 2024) have no selected S2 record: the existing evidence does not supply a suitable isolated temporal contrast for this selection, which does not assert that these papers contain no experiments. Tem-EA and RL-TEA have no S2 record because their full texts were checked and report no experiment that removes or changes temporal input.

The added records cover: TGA-EA "-T" (ten contrasts: two variants × five datasets; time removed from aggregated messages only); DTTEA "w/o TIME" and "w/o OVLP" on two datasets (temporal encoder versus direct dictionary-overlap matching); DynEA formal "Without Time" (removed paths unstated; the non-monotone "Without CLM" row is not used); ActiveTKGA temporal-embedding removal on two datasets and one time-aware versus random selection contrast; TEA (Liu et al.) relation versus relation + time-context on three DBP15k pairs (general KGs with date literals, not quadruple benchmarks; the Digit + Time contrast is not used because it also changes digit content); and PAGEA "w/o PTE" on two datasets (best-configuration values; surviving temporal paths unstated; inconsistent base row in its Table 6).

For a comparison, first specify the intended estimand: configured-system outcome, component removal, or capability under a defined intervention. Then match six conditions: dataset/release and query population; supervision and feedback; temporal information; non-temporal information; candidates and matching; and optimization/tuning/compute. A known nuisance mismatch prevents a narrow causal interpretation. Missing information is an unresolved comparability condition, not evidence of a match. The STEA score-removal contrast includes pseudo-supervision feedback; LightTEA's Sinkhorn-removal contrast lacks a verified frozen-supervision control; TEA-GNN and QUARTER include objective/capacity confounds in the designated configurations.

Most numeric entries use the fractions already normalized in the retained extraction (for example, 88.7% becomes 0.887); no new experimental value is computed. MGTEA retains the explicitly quoted percent scale, 68.59 and 64.22. Rows S2-045 to S2-067 keep the scale of their source table (percent for TGA-EA, DTTEA, DynEA, ActiveTKGA and TEA by Liu et al.; fraction for PAGEA). Use `Numeric Unit` for every row. The TREA future-time row is one observed configuration, so its comparison value is `Not Applicable`. No zeros substitute for missing data. S2's selected metric is generally Hits@1; companion metrics are retained when needed to identify a source inconsistency, not to imply a complete transcription of each table.

## Evidence states

| Term | Meaning |
|---|---|
| Full-text evidence retained | An existing source-specific full-text extraction supports the record. This preparation reconciles that evidence; it does not claim a new reading of every original paper or an experimental replication. |
| Selected operation-level trace | Existing input–operation–output–downstream records are included for this method; completeness is bounded by the recorded decomposition. |
| Method-level summary | L1–L4 synopsis is available, but no uniform detailed trace is claimed. |
| Unresolved | Inspected evidence leaves an ambiguity, contradiction or underdetermined technical/protocol choice. |
| Not Verified | The field has not been established by the retained verification at the required specificity. It may be reported in the original paper. |
| Not Reported | Reserved for an explicitly documented check showing that the specified source/version does not report a field. Absence from a local extraction is insufficient. This export does not convert missing extractions into this state. |
| Not Extracted | A precise numerical observation was not transcribed into the retained record; qualitative evidence can still be present. |
| Not Applicable | The field does not apply to the record, such as a comparator for a single future-time observation. |
| Not specified in source | Used only in rows S1-36 to S1-43 and S2-045 to S2-067: the inspected full text was checked and does not state the detail. |
| Full-text evidence (publisher PDF supplied by author) | Rows S1-36 to S1-43: operation-level coding by model agents from the publisher PDF, with key equations and table values spot-checked against rendered pages. Not human verification. |
| Not separately recorded in retained coding | No separate decomposition/context entry exists in the retained matrix; not a claim that the mechanism is absent. |

Record-level verification labels do not override cell-level unknowns. No author assertion of improvement is promoted to independent capability validation merely because it accompanies an ablation.

## Authoritative sources and reconciliation

The authoritative export view uses the following precedence, rather than mixing historical copies indiscriminately:

1. **Cohort and method summaries:** `master_temporal_methods_matrix_H2.csv`, retaining its 35 core entries (S1-01 to S1-35) and excluding its separate DynEA workshop entry. H2 includes the verified STGEA distance clarification and local-gap wording for TSM-GNN.
2. **Detailed operations:** `retained_operation_records.csv`, 51 records. Existing layer assignments and opaque-module boundaries are preserved.
3. **Current corrections:** the latest modular KAIS manuscript dated 23 October 2026 and `claim_evidence_updates.csv` provide the later TS-align denominator verification. The older “normalization unresolved” flag is superseded only for the inspected comparison equations; the automatic-seed predicate remains unresolved. The detailed operation row and S1 summary carry the same correction.
4. **Experiment observations:** `temporal_methods_comparison.csv` and `core_methods_matrix.csv`; the later `phase94_claim_evidence_updates.csv` supplies MGTEA, HTEA and the STEA DICEWS-200 card. `chapter06_comparability_cases.csv`, the protocol inventory and later manuscript analysis preserve attribution and denominator restrictions.
5. **Bibliography:** current `references_kais.bib`. Citation keys, titles, DOIs and bibliographic years are taken from this existing consolidated source.
6. **Added methods (S1-36 to S1-43; S2-045 to S2-067):** `coded_rows_a.csv`, `coded_rows_b.csv`, `coded_rows_c.csv` and `coding_notes_PAGEA.md`, coded from the publisher PDFs supplied by the author on 22–23 October 2026, with the manuscript's Appendix A rows as the wording reference.

`supplementary_source_mapping.csv` connects each output record to source identifiers, source hashes, selectors and original-paper locators. The public selectors use citation keys; private database identifiers and absolute local paths are excluded. Original source files remain in the author's research archive and are not bundled. A separate private lineage record retains the original row identifiers for reproducibility.

## Relationship to the latest manuscript and author decisions

S1 now matches the manuscript's 43 core methods (Appendix A, excluding the separately indexed DynEA workshop row). The eight added rows use the same L1–L4 wording as Appendix A. Their coding records are `coded_rows_a/b/c.csv` and `coding_notes_PAGEA.md` in the R2 coding folder; the publisher PDFs are in the author's `papers/` folder and are not bundled. The operation-detail sheet is unchanged: it still holds the six selected traces, and the added methods are method-level summaries.

Before attaching these files to a submission, the author should decide whether to cite them as Online Resources and add the corresponding cross-references; this task does not modify manuscript captions, counts or cross-references. Remaining technical questions include the selected ATEA denominator/corruption specification, PAT-Align split, LightTEA ablation feedback, T3A-LLM version equivalence, opaque composite modules, PAGEA's confidence thresholds and the source inconsistencies stated in S2. Verification and review scope are documented in `supplementary_validation_report.md`.

The author-review ZIP includes only the two workbooks, two main CSVs, this README, the public source mapping and validation report. It excludes publisher PDFs, credentials, private research logs and internal lineage. No material has been publicly uploaded or submitted.
