# Awesome Kernel Skills

![11 projects tracked](https://img.shields.io/badge/projects-11-blue) ![updated 2026-03-31](https://img.shields.io/badge/updated-2026--03--31-green)

A curated index of open-source projects that ship in-repo `skill` definitions for LLM infrastructure, GPU kernels, and operator/compiler development.

Useful for people working on:

- LLM serving / inference runtime
- CUDA / Triton / custom operator development
- On-device inference and model compilation

> **Last checked: 2026-03-31 (UTC).** Skill directories verified at `.claude/skills` (or noted otherwise).

## Contents

- [GPU Kernel Libraries](#gpu-kernel-libraries)
- [LLM Serving & Inference Runtime](#llm-serving--inference-runtime)
- [Deep Learning Frameworks](#deep-learning-frameworks)
- [NN → GPU Compilers](#nn--gpu-compilers)
- [On-Device / Edge Inference](#on-device--edge-inference)
- [Kernel Benchmarking & Tooling](#kernel-benchmarking--tooling)
- [Triton / GPU Experimentation](#triton--gpu-experimentation)
- [Candidate Frameworks (No Skills Yet)](#candidate-frameworks-no-skills-yet)
- [Inclusion Criteria](#inclusion-criteria)
- [Contributing](#contributing)

---

## GPU Kernel Libraries

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [huggingface/kernels](https://github.com/huggingface/kernels/tree/main) *(skills at repo root)* | — | Kernel-focused repository from Hugging Face; skills live at the repository root rather than `.claude/skills`. |
| [flashinfer-ai/flashinfer](https://github.com/flashinfer-ai/flashinfer/tree/main/.claude/skills) | `add-cuda-kernel` `benchmark-kernel` `debug-cuda-crash` | Full CUDA kernel lifecycle: implement, benchmark, and debug crashes. Covers attention, decode, and custom inference ops. |

---

## LLM Serving & Inference Runtime

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [sgl-project/sglang](https://github.com/sgl-project/sglang/tree/main/.claude/skills) | `add-jit-kernel` `add-sgl-kernel` `write-sglang-test` `sglang-bisect-ci-regression` | Kernel authoring workflow, CI regression bisection, and test authoring for a major LLM serving stack. |
| [NVIDIA/TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM/tree/main/.claude/skills) | `ad-model-onboard` `ad-pipeline-failure-pr` `ci-failure-retrieval` | Production-focused LLM runtime; skills cover model onboarding and CI/pipeline incident triage. |
| [InternLM/lmdeploy](https://github.com/InternLM/lmdeploy/tree/main/.claude/skills) | `support-new-model` `code-navigation` `check-env` | Onboard new LLMs/VLMs into the PyTorch inference backend; codebase architecture guide; environment diagnostics. |

---

## Deep Learning Frameworks

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [pytorch/pytorch](https://github.com/pytorch/pytorch/tree/main/.claude/skills) | `metal-kernel` `aoti-debug` `at-dispatch-v2` `add-uint-support` | Metal GPU kernel authoring (Apple Silicon), AOT Inductor crash debugging, ATen operator dispatch, and new type support. 12 skills total. |
| [alibaba/MNN](https://github.com/alibaba/MNN/tree/master/skills) *(skills at `skills/`)* | `add-new-op` `arm-cpu-optimize` `support-new-llm` | Operator extension, ARM CPU optimization, and model-support enablement across this cross-platform inference engine. |

---

## NN → GPU Compilers

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [facebookincubator/AITemplate](https://github.com/facebookincubator/AITemplate/tree/main/.claude/skills) | `adding-operators` `migrate-gemm-to-cutedsl` `architecture` | Add operators across CUDA/HIP backends, migrate GEMM kernels to the CuTeDSL DSL, and understand the overall compiler architecture. |

---

## On-Device / Edge Inference

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [pytorch/executorch](https://github.com/pytorch/executorch/tree/main/.claude/skills) | `building` `export` `cortex-m` `profile` `binary-size` | Cross-platform builds (iOS/Android/Cortex-M), model export to `.pte`, ARM MCU backend, runtime profiling and binary-size budgeting. |

---

## Kernel Benchmarking & Tooling

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [flashinfer-ai/flashinfer-bench](https://github.com/flashinfer-ai/flashinfer-bench/tree/main/.claude/skills) | `extract-kernel-definitions` `onboard-model` `collect-workloads` | Automated pipeline: extract GPU kernel definitions from SGLang models, collect real inference workloads as benchmark traces, and onboard new LLMs across multiple repos. |

---

## Triton / GPU Experimentation

| Project | Representative Skills | Focus |
| --- | --- | --- |
| [Butanium/nnterp](https://github.com/Butanium/nnterp/tree/main/.claude/skills) | `doc-edit` | Lightweight documentation-assist skill in a Triton-centric kernel experimentation project. |

---

## Candidate Frameworks (No Skills Yet)

> As of **2026-03-31**, the following popular infra repos were checked but no skill directory was found at common paths (`.claude/skills`, `skills`). Tracked here to help contributors focus future discovery effort.

- [vllm-project/vllm](https://github.com/vllm-project/vllm)
- [triton-lang/triton](https://github.com/triton-lang/triton)
- [Dao-AILab/flash-attention](https://github.com/Dao-AILab/flash-attention)
- [mlc-ai/mlc-llm](https://github.com/mlc-ai/mlc-llm)

---

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
- (recommended) 2–5 representative skill names so readers can quickly judge fit

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
