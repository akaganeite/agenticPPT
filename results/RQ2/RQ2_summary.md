# RQ2 Summary: Robustness Under Realistic Binary Conditions

## Experiment Configuration

| Experiment | Run | Build condition | Model |
|---|---|---|---|
| Stripped baseline | `RQ2-stripped-5.6-sol-max-raw` | x86-64, GCC-O2, stripped | GPT-5.6 Sol / max |
| Stripped medium | `RQ2-stripped-5.6-sol-medium-raw` | x86-64, GCC-O2, stripped | GPT-5.6 Sol / max |
| GCC-O3 | `RQ2-gcc-o3-sol-max` | x86-64, GCC-O3, stripped | GPT-5.6 Sol / max |
| Clang-O2 | `RQ2-clang-o2-sol-max` | x86-64, Clang-O2, stripped | GPT-5.6 Sol / max |
| AArch64 | `RQ2-aarch64-stripped-5.6-sol-max` | AArch64, GCC-O2, stripped | GPT-5.6 Sol / max |
| Deployed | `RQ2-deployed-5.6-sol-max` | Ubuntu x86-64 deployed ELF | GPT-5.6 Sol / max |
| PatchEvolution | `RQ2-PatchEvolution-sol-max`, `PatchEvolution-cliproxy-sol-max` | x86-64, GCC-O2, stripped | GPT-5.6 Sol / max |
| NAFT | `RQ2-NAFT` | x86-64, GCC-O2, stripped | GPT-5.6 Sol / max |

## Build and Deployment Metrics

| Experiment | Accuracy | DSR | Precision | F1 | Recall | Error |
|---|---:|---:|---:|---:|---:|---:|
| Stripped baseline | 0.9683 | 0.9611 | 0.9596 | 0.9710 | 0.9828 | 59 |
| Stripped medium | 0.9554 | 0.9469 | 0.9554 | 0.9554 | 0.9554 | 5 |
| GCC-O3 | 0.9859 | 0.9677 | 0.9817 | 0.9862 | 0.9907 | 12 |
| Clang-O2 | 0.9755 | 0.9522 | 0.9722 | 0.9767 | 0.9813 | 19 |
| AArch64 | 0.9831 | 0.9775 | 0.9894 | 0.9841 | 0.9789 | 50 |
| Deployed | 0.9682 | 0.9682 | 0.9781 | 0.9675 | 0.9571 | 10 |

## PatchEvolution and NAFT Metrics

| Experiment | Projects | Cases | Accuracy | DSR | Precision | F1 | Recall | Error | Inconclusive | NA accuracy |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| PatchEvolution | libxml2 + OpenSSL | 73 | 0.9492 | 0.8615 | 1.0000 | 0.9739 | 0.9492 | 2 | 6 | - |
| NAFT | curl + FFmpeg + SQLite + OpenSSL | 58 | 0.9483 | - | - | - | - | 0 | 0 | 0.9483 |
