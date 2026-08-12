# FluencyScore — WMT public release artifacts

Safe, self-contained package for the FluencyScore WMT research paper **without** proprietary judge prompts or sub-dimension weights.

## Contents

| Path | Description |
|------|-------------|
| `paper/` | `fluencyscore.tex`, `.bib`, `.pdf`, ACL style files |
| `artifacts/tables/` | Precomputed numeric CSV/JSON tables (Spearman/PA aggregates) |
| `artifacts/mqm/` | MQM summary CSVs only (no segment-level text parquets) |
| `artifacts/notebooks/` | Scrubbed evaluation & error-analysis notebooks |

## Explicitly excluded (proprietary)

- Full FluencyScore `SYSTEM_PROMPT` / rubric text
- Sub-dimension weight tuples
- Prompt-edit / “actionable system prompt” guidance from internal notebooks
- Segment-level parquets that are large or unnecessary for table reproduction
- Internal compute scripts under `algebras-ml/tools/compute_fluency2_*.py` and `algebras-ml/prompts/`

## Path mapping (monorepo → this package)

| Internal (private monorepo) | Public release |
|-----------------------------|----------------|
| `notebooks/wmt/fluency2/fluency2_wmt_evaluation.ipynb` | `artifacts/notebooks/fluency2_wmt_evaluation_SAFE.ipynb` |
| `notebooks/fluency2_error_analysis.ipynb` | `artifacts/notebooks/fluency2_error_analysis_SAFE.ipynb` |
| `data_interim/final_results_tables/` | `artifacts/tables/` |
| `data_interim/wmt_mqm/*.csv` | `artifacts/mqm/` |
| `paper/wmt26/fluencyscore_wmt_research/` | `paper/` |

## Reproduce paper tables

Open the SAFE notebooks and point data loaders at `artifacts/tables/` and `artifacts/mqm/` (or the corresponding paths documented in the paper appendix). Numeric headline tables are already included as CSV.

## Citation

See `paper/fluencyscore.bib` and the PDF in `paper/fluencyscore.pdf`.

## Contact

Confidential reviewer access to weights/prompt (not in this repo): via the paper corresponding author / Algebras AI.
