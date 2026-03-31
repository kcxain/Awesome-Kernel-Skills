<div align="center">

# Awesome Kernel Skills

A curated index of open-source projects that ship in-repo `skill` definitions for<br>
**LLM infrastructure · GPU kernels · operator & compiler development**

![11 projects tracked](https://img.shields.io/badge/projects-11-blue?style=flat-square)
![updated 2026-03-31](https://img.shields.io/badge/updated-2026--03--31-green?style=flat-square)
![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)

</div>

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

> **Last checked: 2026-03-31 (UTC).** Skill directories are at `.claude/skills` unless noted otherwise.

## GPU Kernel Libraries

<details>
<summary><a href="https://github.com/huggingface/kernels/tree/main"><b>huggingface/kernels</b></a> <img src="https://img.shields.io/github/stars/huggingface/kernels?style=flat-square" alt="stars"> — GPU kernels / operator optimization &nbsp;·&nbsp; <i>skills at repo root</i></summary>
<br>

Kernel-focused repository from Hugging Face. Skills live at the **repository root** rather than `.claude/skills`.

</details>

<details>
<summary><a href="https://github.com/flashinfer-ai/flashinfer/tree/main/.claude/skills"><b>flashinfer-ai/flashinfer</b></a> <img src="https://img.shields.io/github/stars/flashinfer-ai/flashinfer?style=flat-square" alt="stars"> — GPU kernels / LLM inference ops</summary>
<br>

Full CUDA kernel lifecycle covering attention, decode, and custom inference operators.

**Skills:** <kbd>add-cuda-kernel</kbd> <kbd>benchmark-kernel</kbd> <kbd>debug-cuda-crash</kbd>

| Skill | What it does |
|---|---|
| `add-cuda-kernel` | End-to-end workflow for adding a new CUDA kernel to FlashInfer |
| `benchmark-kernel` | Benchmark kernel performance against baselines |
| `debug-cuda-crash` | Diagnose and fix CUDA illegal memory access and other low-level crashes |

</details>

## LLM Serving & Inference Runtime

<details>
<summary><a href="https://github.com/sgl-project/sglang/tree/main/.claude/skills"><b>sgl-project/sglang</b></a> <img src="https://img.shields.io/github/stars/sgl-project/sglang?style=flat-square" alt="stars"> — LLM serving / inference system</summary>
<br>

One of the most visible open-source LLM serving stacks shipping skills in-tree. Covers the full kernel authoring and CI workflow.

**Skills:** <kbd>add-jit-kernel</kbd> <kbd>add-sgl-kernel</kbd> <kbd>write-sglang-test</kbd> <kbd>sglang-bisect-ci-regression</kbd>

| Skill | What it does |
|---|---|
| `add-jit-kernel` / `add-sgl-kernel` | Author and wire up new JIT / SGLang kernels |
| `write-sglang-test` | Write correctness and performance tests for the serving stack |
| `sglang-bisect-ci-regression` | Bisect CI regressions to the introducing commit |

</details>

<details>
<summary><a href="https://github.com/NVIDIA/TensorRT-LLM/tree/main/.claude/skills"><b>NVIDIA/TensorRT-LLM</b></a> <img src="https://img.shields.io/github/stars/NVIDIA/TensorRT-LLM?style=flat-square" alt="stars"> — production LLM inference framework</summary>
<br>

NVIDIA's production-focused LLM runtime. Skills are oriented around enterprise onboarding and CI/pipeline incident handling.

**Skills:** <kbd>ad-model-onboard</kbd> <kbd>ad-pipeline-failure-pr</kbd> <kbd>ci-failure-retrieval</kbd>

| Skill | What it does |
|---|---|
| `ad-model-onboard` | Onboard a new model into the TensorRT-LLM pipeline |
| `ad-pipeline-failure-pr` | Triage and create a PR for pipeline failures |
| `ci-failure-retrieval` | Retrieve and analyze CI failure logs |

</details>

<details>
<summary><a href="https://github.com/InternLM/lmdeploy/tree/main/.claude/skills"><b>InternLM/lmdeploy</b></a> <img src="https://img.shields.io/github/stars/InternLM/lmdeploy?style=flat-square" alt="stars"> — LLM deployment toolkit / inference serving</summary>
<br>

A toolkit for compressing, deploying, and serving LLMs with TurboMind and PyTorch backends. Skills focus on model integration and developer workflow.

**Skills:** <kbd>support-new-model</kbd> <kbd>code-navigation</kbd> <kbd>check-env</kbd> <kbd>resolve-review</kbd> <kbd>submit-pr</kbd>

| Skill | What it does |
|---|---|
| `support-new-model` | Onboard new LLMs/VLMs into LMDeploy's PyTorch inference backend |
| `code-navigation` | Guided tour of the codebase architecture |
| `check-env` | Diagnose environment and dependency issues |

</details>

## Deep Learning Frameworks

<details>
<summary><a href="https://github.com/pytorch/pytorch/tree/main/.claude/skills"><b>pytorch/pytorch</b></a> <img src="https://img.shields.io/github/stars/pytorch/pytorch?style=flat-square" alt="stars"> — deep learning framework / operator authoring &nbsp;·&nbsp; <i>12 skills</i></summary>
<br>

The core PyTorch framework. Skills cover GPU kernel authoring, AOT compilation debugging, operator dispatch, and type extension.

**Skills:** <kbd>metal-kernel</kbd> <kbd>aoti-debug</kbd> <kbd>at-dispatch-v2</kbd> <kbd>add-uint-support</kbd> <kbd>pt2-bug-basher</kbd> + 7 more

| Skill | What it does |
|---|---|
| `metal-kernel` | Author Metal GPU kernels for PyTorch operators on Apple Silicon |
| `aoti-debug` | Debug AOTInductor segfaults, device mismatches, and CUDA illegal access errors |
| `at-dispatch-v2` | Work with the ATen operator dispatch mechanism |
| `add-uint-support` | Extend PyTorch operators with unsigned integer type support |
| `pt2-bug-basher` | Systematic bug-fixing workflow for PyTorch 2.0 issues |

</details>

<details>
<summary><a href="https://github.com/alibaba/MNN/tree/master/skills"><b>alibaba/MNN</b></a> <img src="https://img.shields.io/github/stars/alibaba/MNN?style=flat-square" alt="stars"> — inference engine / operator runtime &nbsp;·&nbsp; <i>skills at <code>skills/</code></i></summary>
<br>

A cross-platform inference framework with strong low-level optimization support. Skills cover operator extension and hardware-specific tuning.

**Skills:** <kbd>add-new-op</kbd> <kbd>arm-cpu-optimize</kbd> <kbd>support-new-llm</kbd>

| Skill | What it does |
|---|---|
| `add-new-op` | Add a new operator to the MNN runtime |
| `arm-cpu-optimize` | Tune operators for ARM CPU performance |
| `support-new-llm` | Enable support for a new LLM architecture |

</details>

## NN → GPU Compilers

<details>
<summary><a href="https://github.com/facebookincubator/AITemplate/tree/main/.claude/skills"><b>facebookincubator/AITemplate</b></a> <img src="https://img.shields.io/github/stars/facebookincubator/AITemplate?style=flat-square" alt="stars"> — neural network → GPU binary compiler (CUDA/HIP)</summary>
<br>

A Python framework that compiles high-level neural network definitions into high-performance CUDA/HIP C++ code via operator fusion and backend code generation. Skills focus on operator addition and the CuTeDSL backend.

**Skills:** <kbd>adding-operators</kbd> <kbd>migrate-gemm-to-cutedsl</kbd> <kbd>add-cutedsl-backend</kbd> <kbd>architecture</kbd> <kbd>testing</kbd>

| Skill | What it does |
|---|---|
| `adding-operators` | Implement a new operator: Python definition, backend codegen, tests |
| `migrate-gemm-to-cutedsl` | Migrate GEMM kernels from legacy templates to the CuTeDSL DSL |
| `add-cutedsl-backend` | Add a new CuTeDSL backend for a hardware target |
| `architecture` | Overview of the AITemplate compiler pipeline |

</details>

## On-Device / Edge Inference

<details>
<summary><a href="https://github.com/pytorch/executorch/tree/main/.claude/skills"><b>pytorch/executorch</b></a> <img src="https://img.shields.io/github/stars/pytorch/executorch?style=flat-square" alt="stars"> — on-device / edge inference runtime</summary>
<br>

PyTorch's framework for running models on mobile and embedded devices. Skills cover the full lifecycle from build to deployment on resource-constrained hardware.

**Skills:** <kbd>building</kbd> <kbd>export</kbd> <kbd>cortex-m</kbd> <kbd>profile</kbd> <kbd>binary-size</kbd> <kbd>setup</kbd>

| Skill | What it does |
|---|---|
| `building` | Compile ExecuTorch for iOS, Android, CUDA, Metal, CoreML, and Cortex-M |
| `export` | Export a PyTorch model to the `.pte` format for on-device execution |
| `cortex-m` | Target ARM Cortex-M MCUs with the ExecuTorch runtime |
| `profile` | Profile runtime performance on device |
| `binary-size` | Analyze and budget binary size for embedded targets |

</details>

## Kernel Benchmarking & Tooling

<details>
<summary><a href="https://github.com/flashinfer-ai/flashinfer-bench/tree/main/.claude/skills"><b>flashinfer-ai/flashinfer-bench</b></a> <img src="https://img.shields.io/github/stars/flashinfer-ai/flashinfer-bench?style=flat-square" alt="stars"> — LLM kernel benchmarking / workload analysis</summary>
<br>

A benchmarking companion to FlashInfer that automates the entire pipeline from kernel discovery to trace-based benchmarking. Interfaces closely with SGLang for real-world workload capture.

**Skills:** <kbd>extract-kernel-definitions</kbd> <kbd>onboard-model</kbd> <kbd>collect-workloads</kbd> <kbd>add-reference-tests</kbd> <kbd>track-models</kbd> <kbd>clone-repos</kbd>

| Skill | What it does |
|---|---|
| `extract-kernel-definitions` | Extract GPU kernel definitions from SGLang model implementations into standardized JSON schemas |
| `onboard-model` | End-to-end pipeline: discover a new LLM, extract its kernels, collect workloads, open PRs across repos |
| `collect-workloads` | Capture real inference traces from SGLang runs and submit them as benchmark datasets |
| `add-reference-tests` | Add reference correctness tests for onboarded kernels |

</details>

## Triton / GPU Experimentation

<details>
<summary><a href="https://github.com/Butanium/nnterp/tree/main/.claude/skills"><b>Butanium/nnterp</b></a> <img src="https://img.shields.io/github/stars/Butanium/nnterp?style=flat-square" alt="stars"> — Triton kernels / GPU performance engineering</summary>
<br>

A smaller but highly focused project for Triton-based kernel experimentation and GPU performance research.

**Skills:** <kbd>doc-edit</kbd>

</details>

## Candidate Frameworks (No Skills Yet)

> As of **2026-03-31**, the following popular infra repos were checked but no skill directory was found at common paths (`.claude/skills`, `skills`). Tracked here to focus future contributor discovery effort.

| Project | Area |
|---|---|
| [vllm-project/vllm](https://github.com/vllm-project/vllm) <img src="https://img.shields.io/github/stars/vllm-project/vllm?style=flat-square" alt="stars"> | High-throughput LLM inference engine |
| [triton-lang/triton](https://github.com/triton-lang/triton) <img src="https://img.shields.io/github/stars/triton-lang/triton?style=flat-square" alt="stars"> | GPU kernel compiler / Triton language |
| [Dao-AILab/flash-attention](https://github.com/Dao-AILab/flash-attention) <img src="https://img.shields.io/github/stars/Dao-AILab/flash-attention?style=flat-square" alt="stars"> | Memory-efficient attention kernels |
| [mlc-ai/mlc-llm](https://github.com/mlc-ai/mlc-llm) <img src="https://img.shields.io/github/stars/mlc-ai/mlc-llm?style=flat-square" alt="stars"> | LLM compilation and deployment toolkit |

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
