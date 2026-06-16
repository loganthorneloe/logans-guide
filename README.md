# AI Problems Guide

An opinionated guide to understanding the biggest problem spaces in modern AI.

This is not a complete curriculum. It is a short map of unusually good resources that build intuition quickly. The bias is toward fewer, higher-quality resources over long lists.

Use it like this:

1. Read [ML Quick Start](#ml-quick-start) if you cannot explain features, labels, loss, gradients, overfitting, tokens, attention, and evals.
2. Read [Understanding Research vs Engineering](#understanding-research-vs-engineering) so you can tell when a resource is explaining a scientific result versus a production practice.
3. Scan the problem spaces below and pick the one that feels most interesting or useful.
4. Read the resources in that section in order.
5. Build or reproduce something small before collecting more links.

Paid resources are marked as optional.

This is an **[AI for Software Engineers](https://aiforswes.com)** resource. **[Subscribe](https://aiforswes.com/subscribe)** for more fundamentals and technical deep dives.

## Contents

- [ML Quick Start](#ml-quick-start)
- [Understanding Research vs Engineering](#understanding-research-vs-engineering)
- [Core ML Principles](#core-ml-principles)
- [Data, Training Signals, and Synthetic Data](#data-training-signals-and-synthetic-data)
- [Evaluation, Benchmarks, and Reliability](#evaluation-benchmarks-and-reliability)
- [MLOps and AI Operations](#mlops-and-ai-operations)
- [Model Architectures and Reasoning](#model-architectures-and-reasoning)
- [Memory and Continual Learning](#memory-and-continual-learning)
- [Retrieval and Context](#retrieval-and-context)
- [Agents and Tool Use](#agents-and-tool-use)
- [Post-Training and Alignment](#post-training-and-alignment)
- [Training and Inference Infrastructure](#training-and-inference-infrastructure)
- [Local and Open Models](#local-and-open-models)
- [Interpretability, Safety, and Security](#interpretability-safety-and-security)

## ML Quick Start

The core loop is still the center of AI: data -> model -> prediction -> loss -> update -> evaluation. Learn just enough ML to reason about that loop before specializing.

1. [The Hundred-Page Machine Learning Book](https://themlbook.com/) by Andriy Burkov - optional paid book; the shortest serious pass through classical ML, loss, optimization, and model selection.
2. [Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) by Kaggle - train, validate, and debug a small model in code.
3. [Neural Networks](https://www.3blue1brown.com/topics/neural-networks) by 3Blue1Brown - visual intuition for gradients, backprop, and representation learning.
4. [Practical Deep Learning for Coders](https://course.fast.ai/) by fast.ai - hands-on deep learning for programmers; use this when you want intuition from working models.
5. [Learn the Basics](https://docs.pytorch.org/tutorials/beginner/basics/intro.html) by PyTorch - the modern tensor/autograd/training-loop workflow.

## Understanding Research vs Engineering

Big problem: AI resources mix research results, engineering patterns, benchmark claims, and product advice. You need to know which kind of claim you are reading before deciding what to trust or build.

Workflow:

1. Ask whether the resource is explaining a model capability, an implementation trick, an eval result, or a production operating lesson.
2. For research, skim the abstract, figures, results, and limitations before reading linearly.
3. Trace backward to the papers it builds on and forward to the papers that cite it.
4. Check whether the benchmark, dataset, or demo actually tests the claimed capability.
5. For engineering, look for code, data, ablations, failure cases, operating constraints, and independent replications.

Resources:

1. [How to Read a Paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf) by S. Keshav - a practical three-pass method for reading technical papers.
2. [Semantic Scholar](https://www.semanticscholar.org/) - use citation graphs to find the papers before and after a result.
3. [Hugging Face Papers](https://huggingface.co/papers) and [Papers With Code](https://paperswithcode.com/) - use them for discovery, code, datasets, and benchmark context.
4. [AI Index 2025](https://arxiv.org/abs/2504.07139) by Stanford HAI - an annual map of progress, investment, adoption, and benchmark movement.

## Core ML Principles

Big problem: most AI failures still come from basic ML mistakes: bad splits, leakage, weak baselines, wrong metrics, distribution shift, and confusing demos with evidence.

1. [A Few Useful Things to Know About Machine Learning](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf) by Pedro Domingos - the shortest serious essay on generalization, overfitting, data, and model selection.
2. [Machine Learning Yearning](https://www.deeplearning.ai/machine-learning-yearning/) by Andrew Ng - a practical playbook for error analysis, train/dev/test splits, and iteration strategy.
3. [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml/) by Martin Zinkevich - durable engineering lessons for launching and improving ML systems.
4. [Machine Learning Explainability](https://www.kaggle.com/learn/machine-learning-explainability) by Kaggle - quick tools for inspecting what a model learned and where it may be brittle.

## Data, Training Signals, and Synthetic Data

Big problem: models learn from the distribution, quality, labels, filtering, incentives, and leakage in their data.

1. [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) by Gebru et al. - the canonical argument for documenting dataset motivation, composition, collection, and use.
2. [Data Cascades in High-Stakes AI](https://research.google/pubs/data-cascades-in-high-stakes-ai/) by Sambasivan et al. - a grounded look at how data problems compound in real ML systems.
3. [DataComp](https://arxiv.org/abs/2304.14108) by Gadre et al. - a controlled benchmark for studying dataset curation choices.
4. [Self-Instruct](https://arxiv.org/abs/2212.10560) by Wang et al. - the classic recipe for bootstrapping instruction data from model outputs.

## Evaluation, Benchmarks, and Reliability

Big problem: AI work is not real until you can measure whether behavior improved, regressed, or failed in a new way.

1. [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain - the strongest practical argument for evals as product development.
2. [HELM](https://arxiv.org/abs/2211.09110) by Liang et al. - a serious framework for broader language-model evaluation.
3. [Benchmark Data Contamination in LLMs: A Survey](https://arxiv.org/abs/2406.04244) by Li and Flanigan - a useful map of leakage, benchmark validity, and contaminated evals.
4. [Using the Evaluation Tool](https://platform.claude.com/docs/en/test-and-evaluate/eval-tool) by Anthropic - concrete mechanics for prompt, model, and task evaluation.

## MLOps and AI Operations

Big problem: models become products only when data, deployment, monitoring, ownership, and iteration loops survive contact with production.

1. [Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/) by Chip Huyen - optional paid book; the best durable reference for production ML and AI ops.
2. [Hidden Technical Debt in Machine Learning Systems](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems) by Sculley et al. - the classic paper on why production ML complexity compounds.
3. [Full Stack Deep Learning](https://fullstackdeeplearning.com/course/) - an end-to-end view of training, deploying, and operating deep learning systems.
4. [Made With ML](https://madewithml.com/) by Goku Mohandas - practical MLOps lessons from product framing through monitoring.

## Model Architectures and Reasoning

Big problem: how do architecture, scale, modality, prompting, and test-time compute produce useful model behavior?

1. [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) by Andrej Karpathy - the best high-level explanation of what LLMs are and how they are trained.
2. [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) by Jay Alammar - the clearest visual bridge into attention and transformer blocks.
3. [Attention Is All You Need](https://arxiv.org/abs/1706.03762) by Vaswani et al. - the original transformer paper; read it for the mechanism, not the hype.
4. [Mamba](https://arxiv.org/abs/2312.00752) by Gu and Dao - the modern state-space alternative to attention for long sequence modeling.
5. [Learning to Reason with LLMs](https://openai.com/index/learning-to-reason-with-llms/) by OpenAI - useful framing for train-time and test-time compute in reasoning models.

## Memory and Continual Learning

Big problem: useful AI systems need to handle new information, changing users, and nonstationary environments without forgetting what already works.

1. [Continual Lifelong Learning with Neural Networks](https://arxiv.org/abs/1802.07569) by Parisi et al. - the standard review of catastrophic forgetting and continual-learning strategies.
2. [Overcoming Catastrophic Forgetting in Neural Networks](https://arxiv.org/abs/1612.00796) by Kirkpatrick et al. - the elastic weight consolidation paper; read for the core forgetting problem.
3. [Continual Learning for Large Language Models: A Survey](https://arxiv.org/abs/2402.01364) by Wu et al. - maps continual pretraining, instruction tuning, alignment, and evaluation for LLMs.
4. [MemGPT](https://arxiv.org/abs/2310.08560) by Packer et al. - a practical framing of external memory management for long-running LLM agents.

## Retrieval and Context

Big problem: models are limited by context, freshness, provenance, and the quality of the information they can access.

1. [The Illustrated Word2vec](https://jalammar.github.io/illustrated-word2vec/) by Jay Alammar - the best visual starting point for embeddings and vector similarity.
2. [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) by Lewis et al. - the original RAG paper; read for the problem framing.
3. [Lost in the Middle](https://arxiv.org/abs/2307.03172) by Liu et al. - shows why long context is not the same as reliable use of context.
4. [Building Agentic RAG with LlamaIndex](https://www.deeplearning.ai/courses/building-agentic-rag-with-llamaindex) by DeepLearning.AI - a compact hands-on bridge from retrieval to agentic workflows.

## Agents and Tool Use

Big problem: how do we make models take actions through tools without turning the system into an unreliable loop?

1. [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) by Anthropic - practical patterns for workflows, agents, tools, and when to keep things simple.
2. [ReAct](https://arxiv.org/abs/2210.03629) by Yao et al. - the canonical paper on interleaving reasoning traces and tool actions.
3. [Toolformer](https://arxiv.org/abs/2302.04761) by Schick et al. - a useful research framing for models learning when to call tools.
4. [12-Factor Agents](https://github.com/humanlayer/12-factor-agents) by HumanLayer - production design principles for controlling prompts, context, tools, and state.

## Post-Training and Alignment

Big problem: base models are rarely the product; behavior comes from instruction tuning, preference data, adapters, distillation, and feedback.

1. [Training Language Models to Follow Instructions with Human Feedback](https://arxiv.org/abs/2203.02155) by Ouyang et al. - the InstructGPT paper; read for the supervised/RLHF pipeline.
2. [RLHF Book](https://rlhfbook.com/) by Nathan Lambert - the best structured path into preference data, reward models, and post-training.
3. [Direct Preference Optimization](https://arxiv.org/abs/2305.18290) by Rafailov et al. - the cleanest starting point for preference optimization without an explicit reward model.
4. [PEFT](https://huggingface.co/docs/peft/index) by Hugging Face - the standard starting point for LoRA and adapter-based fine-tuning.
5. [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) by Hinton, Vinyals, and Dean - the classic paper on compressing useful behavior into smaller models.

## Training and Inference Infrastructure

Big problem: capability is constrained by GPUs, memory bandwidth, distributed training, serving latency, and cost.

1. [Machine Learning Systems](https://mlsysbook.ai/) - a free systems-level book on the hardware and software stack behind ML.
2. [The Ultra-Scale Playbook](https://huggingface.co/spaces/nanotron/ultrascale-playbook) by Hugging Face/nanotron - high-quality intuition for distributed training and GPU bottlenecks.
3. [Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556) by Hoffmann et al. - the Chinchilla paper; read for compute, data, and model-size tradeoffs.
4. [FlashAttention](https://arxiv.org/abs/2205.14135) by Dao et al. - the paper that makes attention performance feel like a memory-traffic problem.
5. [PagedAttention](https://arxiv.org/abs/2309.06180) by Kwon et al. - the key serving idea behind vLLM-style high-throughput inference.

## Local and Open Models

Big problem: how much can you do without closed model APIs, and what tradeoffs matter for inference, privacy, cost, and control?

1. [LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) by Hugging Face - the ecosystem tour for tokenizers, Transformers, datasets, fine-tuning, and the Hub.
2. [llama.cpp](https://github.com/ggml-org/llama.cpp) by ggml-org - the practical reference point for local inference and quantized models.
3. [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) by Hugging Face - a useful snapshot of open-model tradeoffs and benchmark caveats.
4. [Model Cards](https://huggingface.co/docs/hub/model-cards) by Hugging Face - the habit to build before downloading any open model: read license, data, intended use, and limitations.

## Interpretability, Safety, and Security

Big problem: how do we understand, constrain, secure, and govern systems whose behavior is learned rather than directly programmed?

1. [The Building Blocks of Interpretability](https://distill.pub/2018/building-blocks/) by Olah et al. - visual intuition for hidden representations and interpretability interfaces.
2. [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) by Elhage et al. - the clearest entry into mechanistic interpretability for transformers.
3. [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) by Amodei et al. - a practical taxonomy of accidents, reward hacking, shift, and supervision.
4. [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) by OWASP - the shortest serious map of LLM application security risks.
5. [AI Risk Management Framework](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) by NIST - governance vocabulary for mapping, measuring, managing, and monitoring AI risk.

If you are new and only want one hands-on project after the quick start, use the local [recommendation system](./recommendation-system/). It makes embeddings and training loops concrete without requiring frontier-model infrastructure.

**Questions?** [Message me on X](https://x.com/loganthorneloe).
