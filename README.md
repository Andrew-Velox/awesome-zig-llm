# Awesome Zig LLM [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome Large Language Model (LLM), Machine Learning, and AI projects, libraries, and resources built with the [Zig](https://ziglang.org/) programming language.

Zig's performance, explicit memory management, and seamless C/C++ interoperability make it an exceptionally powerful tool for AI inference, tensor operations, and building fast, resource-efficient LLM tooling. This list tracks the growing ecosystem of Zig-based AI projects — from production-grade inference stacks to educational implementations built from scratch.

Contributions are welcome! Please read the [contribution guidelines](#contributing) first.

---

## Contents

- [Inference Engines](#inference-engines)
- [Training & Autograd](#training--autograd)
- [Bindings & Wrappers](#bindings--wrappers)
- [Tensors & Math](#tensors--math)
- [Linear Algebra](#linear-algebra)
- [Tokenizers](#tokenizers)
- [Tools & Applications](#tools--applications)
- [Learning Resources](#learning-resources)
- [Community](#community)

---

## Inference Engines

*Native or highly optimized inference stacks written in or targeting Zig.*

* **[ZML](https://github.com/zml/zml)** — High-performance, production-ready AI inference stack built in Zig. Designed for speed, safety, and easy deployment of LLMs across hardware targets.
* **[zig-ml](https://github.com/ApoorvaJ/zig-ml)** — LLM inference written from scratch in pure Zig, without any high-level ML libraries. Built to understand AI inference internals and optimize workloads for modest hardware. Heavily inspired by `llama2.c`.
* **[LLaMa2.zig (cgbur)](https://github.com/cgbur/llama2.zig)** — Inference for LLaMA 2 in a single file of pure Zig. Minimal and easy to read.
* **[LLaMa2.zig (clebert)](https://github.com/clebert/llama2.zig)** — Another pure-Zig LLaMA 2 inference implementation, focused on clarity and correctness.
* **[ZigFormer](https://github.com/CogitatorTech/zigformer)** — A transformer-based LLM implemented entirely in pure Zig. Explores how transformer architectures can be expressed using Zig's comptime and type system.
* **[zig_gpt2](https://github.com/EugenHotaj/zig_gpt2)** — A GPT-2 neural network inference engine written in Zig. Capable of running [NanoGPT](https://github.com/karpathy/nanoGPT) models.
* **[llm.zig](https://github.com/Saimirbaci/llm.zig)** — A clean, simple, and fast LLM implementation in Zig, starting with GPT-2. A notable port of Andrej Karpathy's `llm.c`.

---

## Training & Autograd

*Frameworks and libraries for training neural networks and computing gradients in Zig.*

* **[dnns-from-scratch-in-zig](https://github.com/SilasMarvin/dnns-from-scratch-in-zig)** — A minimal, educational implementation of deep neural networks built bottom-up in Zig. Great for understanding what happens under the hood of ML frameworks.
* **[Zant](https://github.com/ZantFoundation/Z-Ant)** — An open-source, cross-platform SDK written in Zig for deploying neural networks on microcontrollers (ARM Cortex-M, RISC-V, x86). Imports, optimizes, and deploys models to constrained hardware. Supports quantization, pruning, and SIMD/GPU offloading.
* **[zig-neural-networks](https://github.com/MadLittleMods/zig-neural-networks)** — An annotated, from-scratch neural network library in Zig implementing a multi-layer perceptron (MLP) with backpropagation and SGD. Focused on readability and learning. Includes gradient checks and the MNIST dataset example.
* **[Zigrad](https://github.com/Marco-Christiani/zigrad)** — A deep learning framework built on a tensor-valued autograd engine. Offers high-level PyTorch-like abstractions alongside low-level control. Benchmarks show **2.5× faster** training than PyTorch on Apple Silicon and **1.5× faster** on x86 CPU. Supports CUDA (experimental), MKL/OpenBLAS, and Tensorboard integration. ⚠️ Currently undergoing a rewrite; public release planned for mid-2026.

---

## Bindings & Wrappers

*Zig bindings and wrappers for popular C/C++ machine learning frameworks and APIs.*

* **[llama.cpp.zig](https://github.com/Deins/llama.cpp.zig)** — Full `llama.cpp` bindings and build utilities for Zig, targeting Zig 0.14.x. Provides ergonomic Zig-style wrappers over `llama.h`, including camelCase naming, prefix removal, and struct-grouped functions. Supports building `llama.cpp` directly via `zig build`.
* **[ollama-zig](https://github.com/dravenk/ollama-zig)** — Zig client library for the Ollama API. Run and interact with locally-served LLMs via Ollama from pure Zig.
* **[onnxruntime.zig](https://github.com/recursiveGecko/onnxruntime.zig)** — Experimental Zig wrapper for the ONNX Runtime, with working examples including Silero VAD (voice activity detection) and NSNet2 (noise suppression).
* **[gpt4all.zig](https://github.com/renerocksai/gpt4all.zig)** — Zig build and terminal-based chat client for GPT4All models (~800k GPT-3.5-Turbo generations based on LLaMA). Features automatic model downloading and serves as a starting point for Zig apps with built-in LLM capabilities.
* **[zig-llm](https://github.com/mattfreire/zig-llm)** — A Zig wrapper around cloud LLM APIs (OpenAI and compatible). Provides simple, idiomatic Zig interfaces for making LLM API requests.

---

## Tensors & Math

*Libraries for tensor operations, matrix multiplication, linear algebra, and SIMD-accelerated math essential for neural networks.*

* **[zgml](https://github.com/candrewlee14/zgml)** — A tensor library for machine learning written in Zig, directly inspired by ggml. Aims to provide similar primitives with a more Zig-native API.
* **[ZEIN](https://github.com/andrewCodeDev/ZEIN)** — A Zig-based tensor library named for *einsum* notation. Planned support for full AVX SIMD and CUDA acceleration.
* **[zensor](https://github.com/ethanthoma/zensor)** — A lightweight Zig tensor library for building basic tensor computation graphs.
* **[zigTensor](https://github.com/cryptodeal/zigTensor)** — A fast, flexible machine learning library written entirely in Zig, inspired by the Flashlight library. Provides core tensor and tensor-ops functionality with ArrayFire as the backend. Autograd is in progress.
* **[zten](https://github.com/maihd/zten)** — A tensor library for Zig based on ggml. Provides a lightweight wrapper around ggml's C API with a Zig-friendly build system.

---

## Linear Algebra

*Vector math, matrix operations, and probability libraries — foundational building blocks for ML in Zig.*

* **[algae](https://github.com/BanchouBoo/algae)** — A Zig math library focused on game development with a clean, concise API for vectors and matrices.
* **[alg](https://github.com/Laremere/alg)** — Algebra utilities for Zig.
* **[VecFns](https://github.com/omaraaa/VecFns)** — Automatic vector math functions for Zig using comptime generics to generate SIMD-friendly operations.
* **[zalgebra](https://github.com/kooparse/zalgebra)** — A linear algebra library for games and real-time graphics, including vectors, matrices, and quaternions.
* **[zlm](https://github.com/ziglibs/zlm)** — Zig linear mathematics: a simple, dependency-free vector and matrix math library.
* **[zmath](https://github.com/JungerBoyo/zmath)** — A simple linear algebra library written in Zig, designed for clarity and ease of use.
* **[zprob](https://github.com/pblischak/zprob)** — A Zig library for probability distributions. Useful for statistical modelling and sampling in ML pipelines.

---

## Tokenizers

*BPE, SentencePiece, and other tokenizer implementations written in Zig.*

* **[tokenizer (jaco-bro)](https://github.com/jaco-bro/tokenizer)** — A BPE tokenizer implemented entirely in pure Zig. Supports multiple models (e.g., Phi-4, Qwen2.5-Coder) via CLI flags. Also pip-installable as a Python package (`tokenizerz`) for cross-language use.
* **[tokeni.zig](https://github.com/alvarobartt/tokeni.zig)** — A minimal Byte Pair Encoding tokenizer in Zig with a focus on learning tokenizer internals (particularly GPT-2 BPE). Aims to eventually support `from_pretrained`-style loading from the Hugging Face Hub.
* **[llm-tokenizer-zig](https://github.com/Mario-SO/llm-tokenizer-zig)** — A BPE tokenizer in pure Zig 0.15 (zero dependencies outside `std`) that tokenizes text and calculates estimated costs across multiple LLM provider pricing tiers.
* **[zig-bpe](https://github.com/dbtreasure/zig-bpe)** — A clean Byte Pair Encoding tokenizer implementation in Zig 0.13.0. Includes training, encoding, decoding, and serialization/deserialization of merge operations.

---

## Tools & Applications

*CLI tools, terminal clients, agents, and deployment utilities for LLMs built with Zig.*

* **[nullclaw](https://github.com/nullclaw/nullclaw)** — Self-described as the fastest, smallest, and fully autonomous AI assistant infrastructure written in Zig.
* **[zig-llm (OpenAI client)](https://github.com/mattfreire/zig-llm)** — A dependency-free Zig client for OpenAI-compatible inference servers. Uses `std.http` and `std.json` for a minimal, arena-allocated HTTP client that fits in one `.zig` file.

---

## Learning Resources

*Tutorials, articles, blog posts, and guides on building AI/ML tools from scratch using Zig.*

### Articles & Blog Posts

* **[A Single-File Zig Client for llama.cpp's OpenAI API Server](https://medium.com/computatrum-veneficus/a-single-file-zig-client-for-llama-cpps-openai-compatible-api-server-e37657580c4f)** — Demonstrates building a minimal, dependency-free Zig HTTP client for `llama.cpp`'s OpenAI-compatible server using only `std.http` and `std.json`.
* **[Deep Neural Networks from Scratch in Zig (Hacker News)](https://news.ycombinator.com/item?id=35696776)** — HN discussion on implementing DNNs from scratch in Zig. The thread contains valuable insights on how Zig's comptime enables clean shape-checking that Python libraries have struggled with for years.
* **[High-Performance AI/LLM Implementation Ideas (Ziggit)](https://ziggit.dev/t/high-performance-ai-llm-implementation-idea-thoughts/10371)** — Community brainstorming thread on leveraging Zig's comptime and SIMD features for efficient LLM inference, including the DeepZig-V3 proposal.
* **[Zigrad: Deep Learning Faster Than PyTorch](https://ziggit.dev/t/zigrad-deep-learning-faster-than-pytorch/6938)** — Ziggit showcase post introducing Zigrad with benchmark comparisons showing 2.5× PyTorch speedup on Apple Silicon.

### Reference Projects (Educational)

* **[llm.c by Andrej Karpathy](https://github.com/karpathy/llm.c)** *(C, not Zig — but the inspiration for many Zig ports)* — The canonical reference implementation that spawned `llm.zig`, `zig-ml`, and others. Essential reading for anyone porting AI workloads to low-level languages.

---

## Community

*Places to discuss Zig AI/ML projects and connect with other developers.*

* **[Ziggit](https://ziggit.dev)** — The official Zig community forum. The Showcase section regularly features new Zig ML/AI projects.
* **[Zig Discord](https://discord.gg/zig)** — Official Zig Discord server with channels for project discussion.
* **[r/Zig](https://www.reddit.com/r/Zig/)** — The Zig subreddit.
* **[Zig News](https://ziglang.org/news/)** — Official news from the Zig core team.
* **[zigcc/awesome-zig](https://github.com/zigcc/awesome-zig)** — The broader Zig ecosystem list, which includes a Machine Learning section.

---

## Contributing

Your contributions are always welcome!

1. **Relevance** — Ensure the project is directly related to LLMs, ML, or AI *and* uses Zig as a primary language (not just a wrapper with one `.zig` file).
2. **Activity** — Prefer projects that are actively maintained or historically significant. Clearly mark archived/unmaintained projects.
3. **Descriptions** — Keep entries concise and objective. One sentence is ideal; two is the maximum. Don't editorialize.
4. **No duplicates** — Search existing entries before submitting a Pull Request.
5. **Alphabetical order** — Within each section, add entries in alphabetical order by project name.
6. **Format** — Follow the existing `**[Name](url)** — Description.` format precisely.

---

