# Deploy Guide — L_GPUSTACK
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, gpustack 0.x, CUDA IPC, gRPC, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, gpustack 0.x, CUDA 12.x, NVLink or PCIe inter-GPU. Multiple T4/A100 GPUs.

## Environment
Multiple GPU nodes. NVLink preferred for tensor parallelism. 32GB RAM per GPU node.

## AIOSS Integration
```bash
aioss init --module L_GPUSTACK --output ./l_gpustack.aioss
aioss append --chain ./l_gpustack.aioss --payload ./output.bin --module L_GPUSTACK
aioss verify --chain ./l_gpustack.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_GPUSTACK",
    aioss_chain="./L_GPUSTACK.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_GPUSTACK.aioss --verbose
python -m L_GPUSTACK.tests.smoke
```
