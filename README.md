# AI Problems Guide

An opinionated guide to understanding the biggest problem spaces in modern AI.

This is not a complete curriculum. It is a short map of unusually good resources that build intuition quickly. The bias is toward fewer, higher-quality resources over long lists.

Use it like this:

1. Read `ML Quick Start` if you cannot explain features, labels, loss, gradients, overfitting, tokens, attention, and evals.
2. Read `Understanding Research vs Engineering` so you can tell when a resource is explaining a scientific result versus a production practice.
3. Scan the problem spaces below and pick the one that feels most interesting or useful.
4. Read the resources in that section in order.
5. Build or reproduce something small before collecting more links.

This is an **[AI for Software Engineers](https://aiforswes.com)** resource. **[Subscribe](https://aiforswes.com/subscribe)** for more fundamentals and technical deep dives.

## Guide Map

1. **[ML Quick Start](#ml-quick-start)**

   Get the minimum ML vocabulary and training-loop intuition before specializing.

2. **[Understanding Research vs Engineering](#understanding-research-vs-engineering)**

   Learn how to separate research claims, ML engineering lessons, and agentic engineering patterns.

3. **[Core ML Principles](#core-ml-principles)**

   Build durable intuition for generalization, leakage, baselines, metrics, and debugging.

4. **[Data, Training Signals, and Synthetic Data](#data-training-signals-and-synthetic-data)**

   Understand how data quality, labels, curation, feedback, and synthetic data shape behavior.

5. **[Evaluation, Benchmarks, and Reliability](#evaluation-benchmarks-and-reliability)**

   Learn how to tell whether a model or AI product actually got better.

6. **[MLOps and AI Operations](#mlops-and-ai-operations)**

   See what it takes to deploy, monitor, own, and improve learned systems in production.

7. **[Model Architectures and Reasoning](#model-architectures-and-reasoning)**

   Study how architecture, scale, attention, sequence models, and test-time compute affect capability.

8. **[Retrieval and Context](#retrieval-and-context)**

   Learn how embeddings, grounding, RAG, long context, and provenance connect models to evidence.

9. **[Agents, Memory, and Tool Use](#agents-memory-and-tool-use)**

   Understand agent harnesses, tool calls, memory, state, handoffs, and action reliability.

10. **[Post-Training and Alignment](#post-training-and-alignment)**

    Learn how base models become useful assistants through feedback, preference data, adapters, and distillation.

11. **[Training and Inference Infrastructure](#training-and-inference-infrastructure)**

    Understand the GPU, distributed training, memory, serving, latency, and cost constraints behind capability.

12. **[Local and Open Models](#local-and-open-models)**

    Learn the tradeoffs around open weights, local inference, quantization, privacy, and model selection.

13. **[Interpretability, Safety, and Security](#interpretability-safety-and-security)**

    Learn how people inspect, constrain, secure, and govern learned systems.

## ML Quick Start

> [!IMPORTANT]
> **[Paid] [The Hundred-Page Machine Learning Book](https://themlbook.com/) by Andriy Burkov**
>
> Why read it: This is the shortest serious pass through classical ML, loss, optimization, generalization, and model selection.

> [!TIP]
> **[Free] [Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) by Kaggle**
>
> Why read it: It gets you training, validating, and debugging a small model in code instead of only reading definitions.

> [!TIP]
> **[Free] [Neural Networks](https://www.3blue1brown.com/topics/neural-networks) by 3Blue1Brown**
>
> Why read it: It gives visual intuition for gradients, backpropagation, and representation learning before the math gets dense.

> [!TIP]
> **[Free] [Practical Deep Learning for Coders](https://course.fast.ai/) by fast.ai**
>
> Why read it: It builds deep learning intuition from working models and is especially strong for software engineers who learn by building.

> [!TIP]
> **[Free] [Learn the Basics](https://docs.pytorch.org/tutorials/beginner/basics/intro.html) by PyTorch**
>
> Why read it: It teaches the modern tensor, autograd, dataset, model, and training-loop workflow used in real projects.

## Understanding Research vs Engineering

This section matters because AI moves through papers, demos, repos, product posts, and production war stories at the same time. If you cannot tell which kind of claim you are reading, you will either over-trust research demos or under-value engineering lessons.

Useful split:

1. Research asks whether a model, method, dataset, benchmark, or training signal reveals a new capability.
2. ML engineering asks whether a learned system can be trained, evaluated, deployed, monitored, and improved reliably.
3. Agentic engineering asks whether a model can be wrapped in context, tools, memory, state, guardrails, and evals so it can take useful actions repeatedly.

Workflow:

1. Ask whether the resource is explaining a research result, ML engineering pattern, agentic engineering pattern, eval result, or production operating lesson.
2. For research, skim the abstract, figures, results, and limitations before reading linearly.
3. Trace backward to the papers it builds on and forward to the papers that cite it.
4. Check whether the benchmark, dataset, or demo actually tests the claimed capability.
5. For engineering, look for code, data, ablations, failure cases, operating constraints, and independent replications.
6. For agentic engineering, look for context design, tool contracts, state transitions, human handoffs, evals, and failure recovery.

> [!TIP]
> **[Free] [How to Read a Paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf) by S. Keshav**
>
> Why read it: It gives a practical three-pass method for reading technical papers without getting stuck in every detail.

> [!TIP]
> **[Free] [Semantic Scholar](https://www.semanticscholar.org/)**
>
> Why use it: Citation graphs help you find what a result builds on and which later papers took it seriously.

> [!TIP]
> **[Free] [Hugging Face Papers](https://huggingface.co/papers) and [Papers With Code](https://paperswithcode.com/)**
>
> Why use them: They are useful for discovery, code, datasets, and benchmark context when a paper becomes part of the current conversation.

> [!TIP]
> **[Free] [AI Index 2025](https://arxiv.org/abs/2504.07139) by Stanford HAI**
>
> Why read it: It gives a broad annual map of progress, investment, adoption, and benchmark movement so individual papers have context.

## Core ML Principles

These principles are the shared foundation under classical ML, deep learning, LLMs, agents, and production systems. They help you reason about whether a model is actually learning, overfitting, leaking data, using the right metric, or failing because the problem framing is wrong.

> [!TIP]
> **[Free] [A Few Useful Things to Know About Machine Learning](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf) by Pedro Domingos**
>
> Why read it: It is a compact, durable explanation of generalization, overfitting, data, representation, and model selection.

> [!TIP]
> **[Free] [Machine Learning Yearning](https://www.deeplearning.ai/machine-learning-yearning/) by Andrew Ng**
>
> Why read it: It teaches practical error analysis, train/dev/test splits, metric choice, and iteration strategy.

> [!TIP]
> **[Free] [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml/) by Martin Zinkevich**
>
> Why read it: It captures hard-won lessons for launching, debugging, and improving ML systems over time.

> [!TIP]
> **[Free] [Machine Learning Explainability](https://www.kaggle.com/learn/machine-learning-explainability) by Kaggle**
>
> Why read it: It gives quick tools for inspecting what a model learned and where that behavior may be brittle.

## Data, Training Signals, and Synthetic Data

This section matters because model behavior is mostly downstream of the data distribution, labels, filters, incentives, and feedback signals used to train it. Better architectures rarely save a system built on bad data or unclear supervision.

> [!TIP]
> **[Free] [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) by Gebru et al.**
>
> Why read it: It teaches the habit of documenting dataset motivation, composition, collection process, intended use, and limitations.

> [!TIP]
> **[Free] [Data Cascades in High-Stakes AI](https://research.google/pubs/data-cascades-in-high-stakes-ai/) by Sambasivan et al.**
>
> Why read it: It shows how messy data decisions compound into downstream model and product failures.

> [!TIP]
> **[Free] [DataComp](https://arxiv.org/abs/2304.14108) by Gadre et al.**
>
> Why read it: It makes dataset curation feel like an experimental variable rather than background plumbing.

> [!TIP]
> **[Free] [Self-Instruct](https://arxiv.org/abs/2212.10560) by Wang et al.**
>
> Why read it: It is the classic recipe for bootstrapping instruction data from model outputs, which is central to synthetic-data thinking.

## Evaluation, Benchmarks, and Reliability

This section matters because AI work is not real until you can detect improvement, regression, and failure. Evals turn subjective impressions into an engineering loop and keep demos from masquerading as durable capability.

> [!TIP]
> **[Free] [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain**
>
> Why read it: It makes the practical case that evals are the core loop for building AI products, not an academic afterthought.

> [!TIP]
> **[Free] [HELM](https://arxiv.org/abs/2211.09110) by Liang et al.**
>
> Why read it: It shows what broader language-model evaluation looks like when you measure multiple scenarios and metrics.

> [!TIP]
> **[Free] [Benchmark Data Contamination in LLMs: A Survey](https://arxiv.org/abs/2406.04244) by Li and Flanigan**
>
> Why read it: It explains why benchmark results can be misleading when training data overlaps with evaluation data.

> [!TIP]
> **[Free] [Using the Evaluation Tool](https://platform.claude.com/docs/en/test-and-evaluate/eval-tool) by Anthropic**
>
> Why read it: It turns evals into concrete mechanics for comparing prompts, models, and task behavior.

## MLOps and AI Operations

This section matters because useful ML systems have to survive real data, real users, monitoring gaps, ownership boundaries, and repeated iteration. MLOps is where the model becomes part of a maintained software system.

> [!IMPORTANT]
> **[Paid] [Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/) by Chip Huyen**
>
> Why read it: It is the best durable reference for production ML system design, from data loops to monitoring and deployment.

> [!TIP]
> **[Free] [Hidden Technical Debt in Machine Learning Systems](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems) by Sculley et al.**
>
> Why read it: It explains why production ML complexity compounds through data dependencies, feedback loops, configuration, and ownership gaps.

> [!TIP]
> **[Free] [Full Stack Deep Learning](https://fullstackdeeplearning.com/course/)**
>
> Why read it: It gives an end-to-end view of training, deploying, and operating deep learning systems.

> [!TIP]
> **[Free] [Made With ML](https://madewithml.com/) by Goku Mohandas**
>
> Why read it: It is a practical MLOps path from product framing through deployment and monitoring.

## Model Architectures and Reasoning

This section matters because architecture shapes what a model can represent, how much context it can use, how expensive it is to run, and what kinds of reasoning behavior can emerge. You do not need to memorize every architecture, but you should understand the major mechanisms.

> [!TIP]
> **[Free] [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) by Andrej Karpathy**
>
> Why watch it: It is the clearest high-level explanation of what LLMs are, how they are trained, and why they behave the way they do.

> [!TIP]
> **[Free] [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) by Jay Alammar**
>
> Why read it: It gives the best visual bridge into attention and transformer blocks before reading the original paper.

> [!TIP]
> **[Free] [Attention Is All You Need](https://arxiv.org/abs/1706.03762) by Vaswani et al.**
>
> Why read it: It is the original transformer paper and the cleanest source for the mechanism that reshaped modern AI.

> [!TIP]
> **[Free] [Mamba](https://arxiv.org/abs/2312.00752) by Gu and Dao**
>
> Why read it: It introduces the modern state-space alternative to attention for long sequence modeling.

> [!TIP]
> **[Free] [Learning to Reason with LLMs](https://openai.com/index/learning-to-reason-with-llms/) by OpenAI**
>
> Why read it: It frames how train-time and test-time compute can change reasoning behavior in modern models.

## Retrieval and Context

This section matters because most useful AI systems need information that is newer, more private, more specific, or more traceable than what the model learned during training. Retrieval and grounding connect model outputs to inspectable evidence.

Grounding is the discipline of connecting model outputs to evidence the system can inspect, cite, and refresh.

> [!TIP]
> **[Free] [The Illustrated Word2vec](https://jalammar.github.io/illustrated-word2vec/) by Jay Alammar**
>
> Why read it: It is the best visual starting point for embeddings, vector similarity, and learned representations.

> [!TIP]
> **[Free] [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) by Lewis et al.**
>
> Why read it: It is the original RAG paper and explains the core problem framing behind retrieval-augmented generation and grounded answers.

> [!TIP]
> **[Free] [Lost in the Middle](https://arxiv.org/abs/2307.03172) by Liu et al.**
>
> Why read it: It shows why long context is not the same as reliable use of context or reliable grounding.

> [!TIP]
> **[Free] [Building Agentic RAG with LlamaIndex](https://www.deeplearning.ai/courses/building-agentic-rag-with-llamaindex) by DeepLearning.AI**
>
> Why take it: It gives a compact hands-on bridge from retrieval systems to agentic workflows.

## Agents, Memory, and Tool Use

This section matters because agentic systems are not just prompts. They are harnesses around models: context, tools, state, memory, policies, handoffs, and failure recovery all determine whether the system can act reliably.

> [!TIP]
> **[Free] [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) by Anthropic**
>
> Why read it: It gives practical patterns for workflows, agent harnesses, tools, and when to keep systems simple.

> [!TIP]
> **[Free] [ReAct](https://arxiv.org/abs/2210.03629) by Yao et al.**
>
> Why read it: It is the canonical paper on interleaving reasoning traces and tool actions.

> [!TIP]
> **[Free] [Toolformer](https://arxiv.org/abs/2302.04761) by Schick et al.**
>
> Why read it: It gives a research framing for how models can learn when tool calls are useful.

> [!TIP]
> **[Free] [12-Factor Agents](https://github.com/humanlayer/12-factor-agents) by HumanLayer**
>
> Why read it: It gives production design principles for agent harnesses that control prompts, context, tools, state, and human feedback.

> [!TIP]
> **[Free] [MemGPT](https://arxiv.org/abs/2310.08560) by Packer et al.**
>
> Why read it: It gives a practical framing of external memory management for long-running LLM agents.

> [!TIP]
> **[Free] [Continual Lifelong Learning with Neural Networks](https://arxiv.org/abs/1802.07569) by Parisi et al.**
>
> Why read it: It explains catastrophic forgetting and the continual-learning strategies behind durable agent memory.

## Post-Training and Alignment

This section matters because base models are rarely the product. Instruction tuning, preference data, adapters, distillation, and feedback loops are how general models become useful, steerable systems.

> [!TIP]
> **[Free] [Training Language Models to Follow Instructions with Human Feedback](https://arxiv.org/abs/2203.02155) by Ouyang et al.**
>
> Why read it: It is the InstructGPT paper and explains the supervised tuning plus RLHF pipeline that shaped modern assistants.

> [!TIP]
> **[Free] [RLHF Book](https://rlhfbook.com/) by Nathan Lambert**
>
> Why read it: It is the best structured path into preference data, reward models, policy optimization, and post-training tradeoffs.

> [!TIP]
> **[Free] [Direct Preference Optimization](https://arxiv.org/abs/2305.18290) by Rafailov et al.**
>
> Why read it: It is the cleanest starting point for preference optimization without training an explicit reward model.

> [!TIP]
> **[Free] [PEFT](https://huggingface.co/docs/peft/index) by Hugging Face**
>
> Why read it: It is the standard practical starting point for LoRA and adapter-based fine-tuning.

> [!TIP]
> **[Free] [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) by Hinton, Vinyals, and Dean**
>
> Why read it: It is the classic paper on compressing useful behavior into smaller models.

## Training and Inference Infrastructure

This section matters because capability is constrained by hardware, memory bandwidth, distributed systems, serving latency, and cost. Infrastructure choices determine what can be trained, served, and iterated on in practice.

> [!TIP]
> **[Free] [Machine Learning Systems](https://mlsysbook.ai/)**
>
> Why read it: It explains the hardware and software stack behind ML systems without assuming you already live in infrastructure.

> [!TIP]
> **[Free] [The Ultra-Scale Playbook](https://huggingface.co/spaces/nanotron/ultrascale-playbook) by Hugging Face/nanotron**
>
> Why read it: It gives unusually clear intuition for distributed training, parallelism, GPU memory, and bottlenecks.

> [!TIP]
> **[Free] [Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556) by Hoffmann et al.**
>
> Why read it: It is the Chinchilla paper and explains compute, data, and model-size tradeoffs.

> [!TIP]
> **[Free] [FlashAttention](https://arxiv.org/abs/2205.14135) by Dao et al.**
>
> Why read it: It makes attention performance feel like a memory-traffic problem rather than only a math problem.

> [!TIP]
> **[Free] [PagedAttention](https://arxiv.org/abs/2309.06180) by Kwon et al.**
>
> Why read it: It explains the key serving idea behind vLLM-style high-throughput inference.

## Local and Open Models

This section matters because open weights and local inference change the tradeoffs around cost, privacy, latency, control, and customization. Understanding those tradeoffs helps you choose when closed APIs are worth it and when local models are enough.

> [!TIP]
> **[Free] [LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) by Hugging Face**
>
> Why read it: It is the ecosystem tour for tokenizers, Transformers, datasets, fine-tuning, and the Hub.

> [!TIP]
> **[Free] [llama.cpp](https://github.com/ggml-org/llama.cpp) by ggml-org**
>
> Why read it: It is the practical reference point for local inference and quantized models.

> [!TIP]
> **[Free] [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) by Hugging Face**
>
> Why use it: It is a useful snapshot of open-model tradeoffs, but only if you read it with benchmark caveats in mind.

> [!TIP]
> **[Free] [Model Cards](https://huggingface.co/docs/hub/model-cards) by Hugging Face**
>
> Why read it: Model cards teach the habit to check license, data, intended use, and limitations before using open weights.

## Interpretability, Safety, and Security

This section matters because learned systems fail in ways ordinary software often does not: hidden representations, prompt injection, reward hacking, distribution shift, misuse, and governance gaps. You need vocabulary for both understanding and constraining behavior.

> [!TIP]
> **[Free] [The Building Blocks of Interpretability](https://distill.pub/2018/building-blocks/) by Olah et al.**
>
> Why read it: It gives visual intuition for hidden representations and interpretability interfaces.

> [!TIP]
> **[Free] [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) by Elhage et al.**
>
> Why read it: It is the clearest entry into mechanistic interpretability for transformers.

> [!TIP]
> **[Free] [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) by Amodei et al.**
>
> Why read it: It gives a practical taxonomy of accidents, reward hacking, shift, and supervision.

> [!TIP]
> **[Free] [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) by OWASP**
>
> Why read it: It is the shortest serious map of LLM application security risks.

> [!TIP]
> **[Free] [AI Risk Management Framework](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) by NIST**
>
> Why read it: It gives governance vocabulary for mapping, measuring, managing, and monitoring AI risk.

**Questions?** [Message me on X](https://x.com/loganthorneloe).
