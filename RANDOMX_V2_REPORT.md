# Scash RandomX v2 Upgrade Report (branch: scash-v2)

## 1. Configuration Summary (`src/configuration.h`)
```cpp
#define RANDOMX_ARGON_MEMORY       262144
#define RANDOMX_ARGON_ITERATIONS   3
#define RANDOMX_ARGON_LANES        1
#define RANDOMX_ARGON_SALT        "RandomX-Scash\x02"
#define RANDOMX_CACHE_ACCESSES     8
#define RANDOMX_DATASET_BASE_SIZE  2147483648
#define RANDOMX_DATASET_EXTRA_SIZE 33554368
#define RANDOMX_PROGRAM_SIZE_V1    256
#define RANDOMX_PROGRAM_SIZE_V2    384
#define RANDOMX_PROGRAM_MAX_SIZE   384
#define RANDOMX_PROGRAM_ITERATIONS 2048
#define RANDOMX_PROGRAM_COUNT      8
#define RANDOMX_SCRATCHPAD_L3      2097152
//Scratchpad L2 size in bytes. Must be a power of two and less than or equal to RANDOMX_SCRATCHPAD_L3.
#define RANDOMX_SCRATCHPAD_L2      262144
//Scratchpad L1 size in bytes. Must be a power of two (minimum 64) and less than or equal to RANDOMX_SCRATCHPAD_L2.
#define RANDOMX_SCRATCHPAD_L1      16384
#define RANDOMX_FREQ_CFROUND        1
```

## 2. Build Status (exit code: 0)
```text
RandomX v2 (librandomx.a) compiled cleanly with RANDOMX_PROGRAM_SIZE=384 and RANDOMX_ARGON_SALT="RandomX-Scash\x02"!
-rw-r--r-- 1 runner runner 763K Oct 31 04:27 build/librandomx.a
-rwxr-xr-x 1 runner runner 241K Oct 31 04:27 build/randomx-benchmark
-rwxr-xr-x 1 runner runner 151K Oct 31 04:27 build/randomx-codegen
```
