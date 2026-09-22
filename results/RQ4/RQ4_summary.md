# RQ4 Summary: Cost-Effective Deployment

## Experiment Configurations

| Item | Configuration |
|---|---|
| Agents | Codex, PPTAgent , MiniSWEAgent |
| T1 | GPT-5.6 Sol / max |
| T2 | GPT-5.6 Sol / medium |
| T3 | GPT-5.6 Terra / high |
| T4 | GPT-5.6 Luna / medium |
| Target | x86-64, GCC-O2, stripped, six projects |

## Six-Project Metrics

| Agent | Tier | Source run | Accuracy | DSR | Precision | F1 | Recall |
|---|---|---|---:|---:|---:|---:|---:|
| Codex | T1 | `sol-max-raw` | 0.9683 | 0.9611 | 0.9596 | 0.9710 | 0.9828 |
| Codex | T2 | `sol-medium-raw` | 0.9554 | 0.9469 | 0.9554 | 0.9554 | 0.9554 |
| Codex | T3 | `terra-high` | 0.8962 | 0.8444 | 0.8839 | 0.9000 | 0.9167 |
| Codex | T4 | `luna-medium` | 0.8068 | 0.7261 | 0.8000 | 0.8148 | 0.8302 |
| PPTAgent | T1 | `sol-max` | 0.9859 | 0.9502 | 0.9906 | 0.9859 | 0.9813 |
| PPTAgent | T2 | `sol-medium` | 0.9509 | 0.9181 | 0.9322 | 0.9524 | 0.9735 |
| PPTAgent | T3 | `terra_high` | 0.9474 | 0.8919 | 0.9519 | 0.9474 | 0.9429 |
| PPTAgent | T4 | `luna_medium` | 0.7178 | 0.6223 | 0.6718 | 0.7554 | 0.8627 |
| MiniSWEAgent | T1 | `sol-max` | 0.9902 | 0.8978 | 0.9813 | 0.9906 | 1.0000 |
| MiniSWEAgent | T2 | sol-medium | 0.9556 | 0.9556 | 0.9402 | 0.9565 | 0.9735 |
| MiniSWEAgent | T3 | `terra-high` | 0.9279 | 0.9190 | 0.9406 | 0.9268 | 0.9135 |
| MiniSWEAgent | T4 | luna-medium | 0.8400 | 0.8253 | 0.8235 | 0.8448 | 0.8673 |

## Token Usage Per Raw Case

| Agent | Tier | Cases with usage | Total tokens/case | Input/case | Output/case | Cache hit/case | Cache miss/case | Reasoning/case |
|---|---|---:|---:|---:|---:|---:|---:|
| Codex | T1 | 621/628 | 223,315 | 219,604 | 3,710 | 174,062 | 45,542 | 2,412 |
| Codex | T2 | 235/240 | 280,149 | 278,021 | 2,128 | 228,211 | 49,810 | 928 |
| Codex | T3 | 235/240 | 536,278 | 532,222 | 4,057 | 379,554 | 152,667 | 2,535 |
| Codex | T4 | 240/240 | 563,106 | 559,664 | 3,441 | 450,607 | 109,057 | 1,717 |
| PPTAgent | T1 | 231/240 | 813,343 | 797,634 | 15,708 | 443,358 | 354,276 | 9,570 |
| PPTAgent | T2 | 239/239 | 293,458 | 289,345 | 4,113 | 236,169 | 53,176 | 1,292 |
| PPTAgent | T3 | 236/239 | 448,081 | 440,395 | 7,686 | 373,679 | 66,716 | 4,015 |
| PPTAgent | T4 | 239/239 | 610,782 | 604,647 | 6,135 | 534,564 | 70,083 | 2,505 |
| MiniSWEAgent | T1 | 237/239 | 622,456 | 611,243 | 11,214 | 522,666 | 88,576 | 7,732 |
| MiniSWEAgent | T2 | 239/239 | 165,320 | 162,241 | 3,079 | 118,872 | 43,369 | 1,053 |
| MiniSWEAgent | T3 | 228/239 | 278,588 | 274,019 | 4,568 | 224,687 | 49,333 | 2,597 |
| MiniSWEAgent | T4 | 239/239 | 390,594 | 386,586 | 4,008 | 332,204 | 54,381 | 1,902 |
