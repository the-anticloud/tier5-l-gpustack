# Developer Cookbook — L_GPUSTACK
**Stack:** Python 3.11, gpustack 0.x, CUDA IPC, gRPC, PAX 27B, AIOSS_FORMAT
**Domain:** GPUStack: multi-GPU inference cluster management for Anticloud sovereign deployment

## Start GPU cluster
```python
from l_gpustack import GPUStackCluster

cluster = GPUStackCluster(
    gpus=["cuda:0", "cuda:1", "cuda:2", "cuda:3"],
    model="./pax-27b-fp16.safetensors",
    parallelism="tensor",
    aioss_chain="./gpustack.aioss"
)
cluster.start()

# Inference request (automatically load-balanced)
result = cluster.infer(prompt="Analyze biosignal data", max_tokens=256)
print(f"Served by: {result.gpu_id}, latency: {result.latency_ms:.0f}ms")
```

## Monitor cluster health
```python
status = cluster.health()
for gpu in status.gpus:
    print(f"cuda:{gpu.id}: {gpu.utilization:.0%} util, {gpu.vram_used_mb:.0f}MB VRAM")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
