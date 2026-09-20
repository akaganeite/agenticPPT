# RQ1 Summary: Symbol-Known Benchmark

## Experiment Configuration

| Item | Configuration |
|---|---|
| Agent | Codex (`codexgpt`) |
| Model | `gpt-5.6-sol`, reasoning `max` |
| Projects | binutils, curl, FFmpeg, libxml2, OpenSSL, SQLite |
| Build | x86-64, GCC-O2, baseline binary |

 |

## Metrics

| Scope | Accuracy | DSR | Precision | F1 | Recall | TC | TP | TN | FP | FN | Inconclusive | Error |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Six-project total | 0.9879 | 0.9862 | 0.9968 | 0.9889 | 0.9811 | 588 | 312 | 261 | 1 | 6 | 1 | 7 |

| Project | Accuracy | DSR | Precision | F1 | Recall | TC | Error |
|---|---:|---:|---:|---:|---:|---:|---:|
| binutils | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 88 | 0 |
| curl | 0.9898 | 0.9898 | 1.0000 | 0.9901 | 0.9804 | 98 | 0 |
| FFmpeg | 0.9873 | 0.9750 | 1.0000 | 0.9905 | 0.9811 | 81 | 1 |
| libxml2 | 0.9565 | 0.9565 | 0.9828 | 0.9580 | 0.9344 | 116 | 1 |
| OpenSSL | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 94 | 1 |
| SQLite | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 1.0000 | 111 | 4 |
