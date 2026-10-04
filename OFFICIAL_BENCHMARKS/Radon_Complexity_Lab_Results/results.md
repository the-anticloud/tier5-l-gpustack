# Radon_Complexity_Lab_Results
**Project:** `L_GPUSTACK` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 5.90625}`
- **complexity_grade:** `B`
- **complexity_score:** `5.90625`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_GPUSTACK\UPSTREAM\scripts\convert_te_onnx_to_trt_onnx.py `

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_GPUSTACK\UPSTREAM\scripts\convert_te_onnx_to_trt_onnx.py
    F 76:0 cast_scale - B (9)
    F 177:0 replace_customop_qdq_with_onnx_qdq - B (9)
    F 121:0 custom_op_to_opset19 - B (8)
    F 34:0 find_node_by_tensor - B (7)
    F 166:0 update_quantize_node_type - A (4)
    F 47:0 redirect_quantize_input - A (3)
    F 56:0 redirect_dequantize_output - A (3)
    F 69:0 get_attr - A (3)
    F 157:0 check_model - A (3)
    F 65:0 get_attr_numpy_tensor - A (2)
    F 110:0 create_constant_tensor - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_GPUSTACK\UPSTREAM\scripts\copyright-scan.py
    F 110:0 update - B (9)
    F 153:0 copyright_scan - B (6)
    F 100:0 parse_args - A (1)
    F 166:0 main - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_GPUSTACK\UPSTREAM\.agents\skills\trt-perf-analysis\scripts\analyze_trt_perf.py
    F 45:0 main - A (4)
    F 20:0 parse_args - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_GPUSTACK\UPSTREAM\.agents\skills\trt-perf-analysis\scripts\package_report.py
    F 348:0 main - B (10)
    F 282:0 package_input_folder - B (8)
    F 243:0 package_existing_json - B (7)
    F 129:0 next_available_report_dir - A (4)
    F 143:0 resolve_new_report_dir - A (4)
    F 156:0 validate_template_dir - A (4)
    F 199:0 stage_report_assets - A (4)
    F 219:0 copy_analyze_markdown - A (4)
    F 327:0 package_new_analysis - A (4)
    F 80:0 i
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_