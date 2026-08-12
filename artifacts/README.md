# Artifacts

## Included

- **tables/** — numeric-only CSV/JSON from `data_interim/final_results_tables/` (fair-subset correlations, per-pair PA, chrF++ aggregates, mask variants).
- **mqm/** — aggregate/ablation CSVs from `data_interim/wmt_mqm/` (no `*.parquet`).
- **notebooks/** — SAFE copies of the WMT evaluation and error-analysis notebooks.

## Not included

- Proprietary FluencyScore prompts and weight tuples
- Full segment parquets (`all_metrics_mqm.parquet`, fluency checkpoints, etc.)
- Any cell that printed system-prompt patches (replaced with a redaction note)

If you need segment-level scores for secondary analyses, request reviewer materials separately; do not expect prompts in that bundle either unless under NDA/reviewer confidentiality.
