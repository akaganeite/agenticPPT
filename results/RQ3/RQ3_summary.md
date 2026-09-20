# RQ3 Summary: Factors Influencing Capability

## Model Configurations

| Tier | Codex run | Model/reasoning | Accuracy | DSR | Precision | F1 | Recall | TC | Error |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|
| T1 | `RQ2-stripped-5.6-sol-max-raw` | GPT-5.6 Sol / max | 0.9683 | 0.9611 | 0.9596 | 0.9710 | 0.9828 | 599 | 59 |
| T2 | `RQ2-stripped-5.6-sol-medium-raw` | GPT-5.6 Sol / medium | 0.9554 | 0.9469 | 0.9554 | 0.9554 | 0.9554 | 231 | 5 |
| T3 | `RQ5-gcc-o2-terra-high` | GPT-5.6 Terra / high | 0.8962 | 0.8444 | 0.8839 | 0.9000 | 0.9167 | 230 | 5 |
| T4 | `RQ5-gcc-o2-luna-medium` | GPT-5.6 Luna / medium | 0.8068 | 0.7261 | 0.8000 | 0.8148 | 0.8302 | 230 | 0 |

## Model-Tier Failure Mechanisms

| Failure mechanism | T1 | T2 | T3 | T4 |
|---|---:|---:|---:|---:|
| Target function not found | 0 | 0 | 7 | 20 |
| Wrong patch site in target function | 3 | 2 | 12 | 27 |
| Patch site not found in target function | 0 | 0 | 2 | 3 |
| Patch semantics misjudged | 3 | 8 | 10 | 11 |
| Applicability misjudged | 2 | 2 | 0 | 2 |
| No distinguishable binary evidence | 4 | 2 | 1 | 0 |
| Total classified failures | 12 | 14 | 32 | 63 |

## Metadata and Ghidra Ablation

| Variant | Accuracy | DSR | Precision | F1 | Recall | TC | TP | TN | FP | FN | Inconclusive | Error |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| m0_b0 | 0.8962 | 0.8520 | 0.8839 | 0.9000 | 0.9167 | 228 | 99 | 91 | 13 | 9 | 11 | 5 |
| m0_b1 | 0.9171 | 0.8356 | 0.9223 | 0.9179 | 0.9135 | 225 | 95 | 93 | 8 | 9 | 20 | 0 |
| m1_b0 | 0.9628 | 0.9200 | 0.9630 | 0.9630 | 0.9630 | 227 | 104 | 103 | 4 | 4 | 10 | 2 |
| m1_b1 | 0.9539 | 0.9119 | 0.9474 | 0.9558 | 0.9643 | 227 | 108 | 99 | 6 | 4 | 10 | 0 |