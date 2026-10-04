# 3-Seed Simulation — L_GPUSTACK

**Seeds:** `95196` · `26533` · `60732`

**Seed method:** `sha256("L_GPUSTACK")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_GPUSTACK`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.17 | 0.1251 | ±0.2452 |
| throughput_tokens_per_sec | 3268.0 | 27.267 | ±53.4433 |
| p50_latency_ms | 48.06 | 3.7246 | ±7.3002 |
| p99_latency_ms | 119.5667 | 7.8918 | ±15.4679 |
| ttft_ms | 30.06 | 4.0002 | ±7.8404 |
| mmlu_proxy | 0.7385 | 0.0261 | ±0.0512 |
| hellaswag_proxy | 0.7597 | 0.0151 | ±0.0296 |
| truthfulqa_proxy | 0.6032 | 0.0376 | ±0.0737 |
| arc_proxy | 0.6974 | 0.0352 | ±0.069 |
| complexity_cyclomatic | 4.26 | 0.3269 | ±0.6407 |
| maintainability_index | 67.9533 | 4.1484 | ±8.1309 |
| security_issues_high | 1.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 78.6333 | 6.5576 | ±12.8529 |
| test_coverage_pct | 51.5333 | 10.585 | ±20.7466 |
| doc_coverage_pct | 65.2333 | 8.5986 | ±16.8533 |
| memory_mb | 2177.0 | 73.7281 | ±144.5071 |
| gpu_util_pct | 69.5667 | 6.3226 | ±12.3923 |
| openssf_score | 6.5333 | 0.2963 | ±0.5807 |
| eu_ai_act_compliance_pct | 76.2333 | 1.1898 | ±2.332 |
| slsa_level | 1.6667 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 95196 | Seed 26533 | Seed 60732 |
|--------|------------|------------|------------|
| trl_score | 6.994 | 7.274 | 7.242 |
| throughput_tokens_per_sec | 3276.1 | 3296.6 | 3231.3 |
| p50_latency_ms | 52.38 | 48.51 | 43.29 |
| p99_latency_ms | 108.56 | 126.67 | 123.47 |
| ttft_ms | 32.31 | 24.44 | 33.43 |
| mmlu_proxy | 0.7015 | 0.7569 | 0.757 |
| hellaswag_proxy | 0.7542 | 0.7446 | 0.7803 |
| truthfulqa_proxy | 0.5532 | 0.6128 | 0.6437 |
| arc_proxy | 0.6968 | 0.7408 | 0.6546 |
| complexity_cyclomatic | 4.72 | 3.99 | 4.07 |
| maintainability_index | 64.99 | 73.82 | 65.05 |
| security_issues_high | 1 | 1 | 2 |
| dependency_freshness_pct | 82.5 | 69.4 | 84.0 |
| test_coverage_pct | 66.5 | 43.8 | 44.3 |
| doc_coverage_pct | 61.6 | 57.0 | 77.1 |
| memory_mb | 2115.0 | 2135.4 | 2280.6 |
| gpu_util_pct | 73.0 | 75.0 | 60.7 |
| openssf_score | 6.48 | 6.2 | 6.92 |
| eu_ai_act_compliance_pct | 74.7 | 77.6 | 76.4 |
| slsa_level | 1 | 2 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._