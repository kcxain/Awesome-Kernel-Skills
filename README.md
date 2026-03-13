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
| [Butanium/nnterp](https://github.com/Butanium/nnterp/tree/main/.claude/skills) | Triton kernels / GPU performance engineering | `.claude/skills` | A smaller but very relevant project for kernel-level experimentation and optimization. |

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

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
