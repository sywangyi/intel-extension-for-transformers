Step-by-Step
============
This document describes the step-by-step instructions to run GPT-J on 4th Gen Intel® Xeon® Scalable Processor (SPR) with PyTorch and Intel® Extension for PyTorch.

The script ```run_gptj.py``` is based on [EleutherAI/gpt-j-6B](https://huggingface.co/EleutherAI/gpt-j-6B) and provides inference benchmarking.

For [EleutherAI/gpt-j-6B](https://huggingface.co/EleutherAI/gpt-j-6B) quantization, please refer to [quantization example](../quantization/inc)

# Prerequisite
## Create Environment
```
conda install mkl mkl-include -y
conda install jemalloc gperftools -c conda-forge -y
pip install torch==1.13.1 --extra-index-url https://download.pytorch.org/whl/cpu
pip install intel_extension_for_pytorch==1.13.0
pip install -r requirements.txt
```
## Setup Environment Variables
```
export KMP_BLOCKTIME=1
export KMP_SETTINGS=1
export KMP_AFFINITY=granularity=fine,compact,1,0

# IOMP
export OMP_NUM_THREADS=< Cores to use >
export LD_PRELOAD=${LD_PRELOAD}:${CONDA_PREFIX}/lib/libiomp5.so
# Jemalloc
export LD_PRELOAD=${LD_PRELOAD}:${CONDA_PREFIX}/lib/libjemalloc.so
export MALLOC_CONF="oversize_threshold:1,background_thread:true,metadata_thp:auto,dirty_decay_ms:9000000000,muzzy_decay_ms:9000000000"
```

# Performance
```bash
numactl -m <node N> -C <cpu list> python run_gptj.py <fp32/bf16>
```

>**Note:** Inference performance speedup with Intel DL Boost (VNNI/AMX) on Intel(R) Xeon(R) hardware, Please refer to [Performance Tuning Guide](https://intel.github.io/intel-extension-for-pytorch/cpu/latest/tutorials/performance_tuning/tuning_guide.html) for more optimizations.

