## Awesome Kernel Skills

This repository collects public `skill` definitions from well-known open-source projects focused on LLM infrastructure, GPU kernels, compiler/operator development.

The goal is to build a curated index for people working on:

- LLM infra
- CUDA / Triton / custom operator development

## Collected Projects

The projects below are already using in-repo skills and are closely related to large-model infra or operator/kernel development.

| Project | Area | Skill Location | Notes |
| --- | --- | --- | --- |
| [huggingface/kernels](https://github.com/huggingface/kernels/tree/main) | GPU kernels / operator optimization | repository root | Kernel-focused repository from Hugging Face. |
| [sgl-project/sglang](https://github.com/sgl-project/sglang/tree/main/.claude/skills) | LLM serving / inference system | `.claude/skills` | One of the most visible open-source LLM serving stacks shipping skills in-tree. |
| [alibaba/MNN](https://github.com/alibaba/MNN/tree/master/skills) | inference engine / operator runtime | `skills` | General inference framework with relevant low-level optimization workflows. |
| [flashinfer-ai/flashinfer](https://github.com/flashinfer-ai/flashinfer/tree/main/.claude/skills) | GPU kernels / LLM inference ops | `.claude/skills` | Highly relevant for attention, decode, and custom inference operator work. |
| [NVIDIA/TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM/tree/main/.claude/skills) | production LLM inference framework | `.claude/skills` | NVIDIA's production-focused LLM runtime; skills are oriented around onboarding and CI failure triage. |
| [Butanium/nnterp](https://github.com/Butanium/nnterp/tree/main/.claude/skills) | Triton kernels / GPU performance engineering | `.claude/skills` | A smaller but very relevant project for kernel-level experimentation and optimization. |
| [pytorch/pytorch](https://github.com/pytorch/pytorch/tree/main/.claude/skills) | deep learning framework / operator authoring | `.claude/skills` | 12 skills covering Metal kernel authoring (Apple Silicon), AOT Inductor debugging, ATen operator dispatch, and unsigned integer type support. |
| [pytorch/executorch](https://github.com/pytorch/executorch/tree/main/.claude/skills) | on-device / edge inference runtime | `.claude/skills` | 6 skills for cross-platform builds (iOS/Android/Cortex-M), model export to `.pte` format, binary-size analysis, and profiling. |
| [InternLM/lmdeploy](https://github.com/InternLM/lmdeploy/tree/main/.claude/skills) | LLM deployment toolkit / inference serving | `.claude/skills` | 5 skills for onboarding new LLMs/VLMs into the PyTorch backend, environment checks, and codebase navigation. |
| [facebookincubator/AITemplate](https://github.com/facebookincubator/AITemplate/tree/main/.claude/skills) | neural network → GPU binary compiler (CUDA/HIP) | `.claude/skills` | 6 skill files covering operator addition, CuTeDSL DSL backend migration, GEMM optimization, and testing. |
| [flashinfer-ai/flashinfer-bench](https://github.com/flashinfer-ai/flashinfer-bench/tree/main/.claude/skills) | LLM kernel benchmarking / workload analysis | `.claude/skills` | 6 skills automating the kernel benchmarking pipeline: GPU kernel definition extraction, model onboarding, and real-world workload collection from SGLang. |

## Skill Content Snapshot (Research Notes)

> Last checked: **2026-03-31 (UTC)**.

To make this list more actionable, below is a quick summary of what each project's in-repo skills are actually covering:

| Project | Example Skills Observed | What the Skills Emphasize |
| --- | --- | --- |
| [sglang](https://github.com/sgl-project/sglang/tree/main/.claude/skills) | `add-jit-kernel`, `add-sgl-kernel`, `sglang-bisect-ci-regression`, `write-sglang-test` | Kernel authoring workflow + CI regression bisection + test authoring for a serving stack. |
| [flashinfer](https://github.com/flashinfer-ai/flashinfer/tree/main/.claude/skills) | `add-cuda-kernel`, `benchmark-kernel`, `debug-cuda-crash` | CUDA kernel lifecycle: implementation, benchmarking, and low-level crash debugging. |
| [MNN](https://github.com/alibaba/MNN/tree/master/skills) | `add-new-op`, `arm-cpu-optimize`, `support-new-llm` | Operator extension plus ARM CPU optimization and model-support enablement. |
| [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM/tree/main/.claude/skills) | `ad-model-onboard`, `ad-pipeline-failure-pr`, `ci-failure-retrieval` | Enterprise/production workflows: model onboarding and CI/pipeline incident handling. |
| [nnterp](https://github.com/ndif-team/nnterp/tree/main/.claude/skills) | `doc-edit.md` | Lightweight documentation-assist skill in a Triton-centric experimentation project. |
| [pytorch/pytorch](https://github.com/pytorch/pytorch/tree/main/.claude/skills) | `metal-kernel`, `aoti-debug`, `at-dispatch-v2`, `add-uint-support` | Metal GPU kernel authoring on Apple Silicon, AOT Inductor crash debugging, ATen operator dispatch mechanism, unsigned integer type extension. |
| [pytorch/executorch](https://github.com/pytorch/executorch/tree/main/.claude/skills) | `building`, `export`, `cortex-m`, `profile`, `binary-size` | Cross-platform build (iOS/Android/MCU), model export to `.pte`, ARM Cortex-M backend, runtime profiling and binary-size budgeting. |
| [InternLM/lmdeploy](https://github.com/InternLM/lmdeploy/tree/main/.claude/skills) | `support-new-model`, `code-navigation`, `check-env` | Onboarding new LLMs/VLMs into LMDeploy's PyTorch inference backend; codebase architecture guide; environment diagnostics. |
| [facebookincubator/AITemplate](https://github.com/facebookincubator/AITemplate/tree/main/.claude/skills) | `adding-operators`, `migrate-gemm-to-cutedsl`, `architecture` | Adding custom operators across CUDA/HIP backends, migrating GEMM kernels to the CuTeDSL DSL, and overall compiler architecture. |
| [flashinfer-ai/flashinfer-bench](https://github.com/flashinfer-ai/flashinfer-bench/tree/main/.claude/skills) | `extract-kernel-definitions`, `onboard-model`, `collect-workloads` | Automated pipeline: extract GPU kernel definitions from SGLang models, collect real inference workloads as benchmark traces, and onboard new LLMs across multiple repos. |

## Candidate Infra Frameworks (No in-repo skills found yet)

As of 2026-03-31, the following popular infra repos were checked but no in-repo skill directory was found at common paths (e.g., `.claude/skills`, `skills`):

- [vllm-project/vllm](https://github.com/vllm-project/vllm)
- [triton-lang/triton](https://github.com/triton-lang/triton)
- [Dao-AILab/flash-attention](https://github.com/Dao-AILab/flash-attention)
- [mlc-ai/mlc-llm](https://github.com/mlc-ai/mlc-llm)

This section is intentionally tracked to help future contributors focus discovery effort on frameworks that may add skills later.

## Inclusion Criteria

This list prefers projects that satisfy at least one of the following:

- the repository ships a `skills`, `.claude/skills`, or equivalent in-repo skill directory
- the project is clearly focused on LLM serving, inference runtime, kernels, or operator development
- the repository is reasonably well-known in the open-source large-model infra ecosystem

Projects that are only general-purpose prompt collections or unrelated agent demos should not be added here.


## Contributing

Pull requests are welcome. When adding a new project, please include:

- the repository link
- the exact skill directory path
- a short note explaining why it is relevant to LLM infra or operator/kernel development
- (recommended) 2-5 representative skill names so readers can quickly judge fit

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
