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

## Skill Content Snapshot (Research Notes)

> Last checked: **2026-03-19 (UTC)**.

To make this list more actionable, below is a quick summary of what each project's in-repo skills are actually covering:

| Project | Example Skills Observed | What the Skills Emphasize |
| --- | --- | --- |
| [sglang](https://github.com/sgl-project/sglang/tree/main/.claude/skills) | `add-jit-kernel`, `add-sgl-kernel`, `sglang-bisect-ci-regression`, `write-sglang-test` | Kernel authoring workflow + CI regression bisection + test authoring for a serving stack. |
| [flashinfer](https://github.com/flashinfer-ai/flashinfer/tree/main/.claude/skills) | `add-cuda-kernel`, `benchmark-kernel`, `debug-cuda-crash` | CUDA kernel lifecycle: implementation, benchmarking, and low-level crash debugging. |
| [MNN](https://github.com/alibaba/MNN/tree/master/skills) | `add-new-op`, `arm-cpu-optimize`, `support-new-llm` | Operator extension plus ARM CPU optimization and model-support enablement. |
| [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM/tree/main/.claude/skills) | `ad-model-onboard`, `ad-pipeline-failure-pr`, `ci-failure-retrieval` | Enterprise/production workflows: model onboarding and CI/pipeline incident handling. |
| [nnterp](https://github.com/ndif-team/nnterp/tree/main/.claude/skills) | `doc-edit.md` | Lightweight documentation-assist skill in a Triton-centric experimentation project. |

## Candidate Infra Frameworks (No in-repo skills found yet)

As of 2026-03-19, the following popular infra repos were checked but no in-repo skill directory was found at common paths (e.g., `.claude/skills`, `skills`):

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
