# AI Problems Guide

An opinionated guide to understanding the biggest problem spaces in modern AI.

This is not a complete curriculum. It is a short map of unusually good resources that build intuition quickly. The bias is toward fewer, higher-quality resources over long lists.

Use it like this:

1. Read `Machine Learning Quick Start` if you cannot explain features, labels, loss, gradients, overfitting, tokens, attention, and evals.
2. Read `Understanding Research vs Engineering` so you can tell when a resource is explaining a scientific result versus a production practice.
3. Scan the problem spaces below and pick the one that feels most interesting or useful.
4. Read the resources in that section in order.
5. Build or reproduce something small before collecting more links.

This is an **[AI for Software Engineers](https://aiforswes.com)** resource. **[Subscribe](https://aiforswes.com/subscribe)** for more fundamentals and technical deep dives.

## Table of Contents

1. [**Machine Learning Quick Start**](#machine-learning-quick-start)

   Get the minimum machine learning vocabulary and training-loop intuition before specializing.

   - [The Hundred-Page Machine Learning Book](#the-hundred-page-machine-learning-book-by-andriy-burkov)
   - [Intro to Machine Learning](#intro-to-machine-learning-by-kaggle)
   - [Neural Networks](#neural-networks-by-3blue1brown)
   - [Practical Deep Learning for Coders](#practical-deep-learning-for-coders-by-fastai)
   - [Learn the Basics](#learn-the-basics-by-pytorch)

2. [**Understanding Research vs Engineering**](#understanding-research-vs-engineering)

   Learn how to separate research claims, machine learning engineering lessons, and agentic engineering patterns.

   - [How to Read a Paper](#how-to-read-a-paper-by-s-keshav)
   - [Semantic Scholar](#semantic-scholar)
   - [Hugging Face Papers and Papers With Code](#hugging-face-papers-and-papers-with-code)
   - [AI Index 2025](#ai-index-2025-by-stanford-hai)

3. [**Core Machine Learning Principles**](#core-machine-learning-principles)

   Build durable intuition for generalization, leakage, baselines, metrics, and debugging.

   - [A Few Useful Things to Know About Machine Learning](#a-few-useful-things-to-know-about-machine-learning-by-pedro-domingos)
   - [Machine Learning Yearning](#machine-learning-yearning-by-andrew-ng)
   - [Rules of Machine Learning](#rules-of-machine-learning-by-martin-zinkevich)
   - [Machine Learning Explainability](#machine-learning-explainability-by-kaggle)

4. [**Data, Training Signals, and Synthetic Data**](#data-training-signals-and-synthetic-data)

   Understand how data quality, labels, curation, feedback, and synthetic data shape behavior.

   - [Datasheets for Datasets](#datasheets-for-datasets-by-gebru-et-al)
   - [Data Cascades in High-Stakes AI](#data-cascades-in-high-stakes-ai-by-sambasivan-et-al)
   - [DataComp](#datacomp-by-gadre-et-al)
   - [Self-Instruct](#self-instruct-by-wang-et-al)

5. [**Evaluation, Benchmarks, and Reliability**](#evaluation-benchmarks-and-reliability)

   Learn how to tell whether a model or AI product actually got better.

   - [Your AI Product Needs Evals](#your-ai-product-needs-evals-by-hamel-husain)
   - [HELM](#helm-by-liang-et-al)
   - [Benchmark Data Contamination in LLMs: A Survey](#benchmark-data-contamination-in-llms-a-survey-by-li-and-flanigan)
   - [Using the Evaluation Tool](#using-the-evaluation-tool-by-anthropic)

6. [**MLOps and AI Operations**](#mlops-and-ai-operations)

   See what it takes to deploy, monitor, own, and improve learned systems in production.

   - [Designing Machine Learning Systems](#designing-machine-learning-systems-by-chip-huyen)
   - [Hidden Technical Debt in Machine Learning Systems](#hidden-technical-debt-in-machine-learning-systems-by-sculley-et-al)
   - [Full Stack Deep Learning](#full-stack-deep-learning)
   - [Made With ML](#made-with-ml-by-goku-mohandas)

7. [**Model Architectures and Reasoning**](#model-architectures-and-reasoning)

   Study how architecture, scale, attention, sequence models, and test-time compute affect capability.

   - [Intro to Large Language Models](#intro-to-large-language-models-by-andrej-karpathy)
   - [The Illustrated Transformer](#the-illustrated-transformer-by-jay-alammar)
   - [Attention Is All You Need](#attention-is-all-you-need-by-vaswani-et-al)
   - [Mamba](#mamba-by-gu-and-dao)
   - [Learning to Reason with LLMs](#learning-to-reason-with-llms-by-openai)

8. [**Retrieval and Context**](#retrieval-and-context)

   Learn how embeddings, grounding, RAG, long context, and provenance connect models to evidence.

   - [The Illustrated Word2vec](#the-illustrated-word2vec-by-jay-alammar)
   - [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](#retrieval-augmented-generation-for-knowledge-intensive-nlp-tasks-by-lewis-et-al)
   - [Lost in the Middle](#lost-in-the-middle-by-liu-et-al)
   - [Building Agentic RAG with LlamaIndex](#building-agentic-rag-with-llamaindex-by-deeplearningai)

9. [**Agents, Memory, and Tool Use**](#agents-memory-and-tool-use)

   Understand agent harnesses, tool calls, memory, state, handoffs, and action reliability.

   - [Building Effective Agents](#building-effective-agents-by-anthropic)
   - [ReAct](#react-by-yao-et-al)
   - [Toolformer](#toolformer-by-schick-et-al)
   - [12-Factor Agents](#12-factor-agents-by-humanlayer)
   - [MemGPT](#memgpt-by-packer-et-al)
   - [Continual Lifelong Learning with Neural Networks](#continual-lifelong-learning-with-neural-networks-by-parisi-et-al)

10. [**Post-Training and Alignment**](#post-training-and-alignment)

    Learn how base models become useful assistants through feedback, preference data, adapters, and distillation.

    - [Training Language Models to Follow Instructions with Human Feedback](#training-language-models-to-follow-instructions-with-human-feedback-by-ouyang-et-al)
    - [RLHF Book](#rlhf-book-by-nathan-lambert)
    - [Direct Preference Optimization](#direct-preference-optimization-by-rafailov-et-al)
    - [PEFT](#peft-by-hugging-face)
    - [Distilling the Knowledge in a Neural Network](#distilling-the-knowledge-in-a-neural-network-by-hinton-vinyals-and-dean)

11. [**Training and Inference Infrastructure**](#training-and-inference-infrastructure)

    Understand the GPU, distributed training, memory, serving, latency, and cost constraints behind capability.

    - [Machine Learning Systems](#machine-learning-systems)
    - [The Ultra-Scale Playbook](#the-ultra-scale-playbook-by-hugging-facenanotron)
    - [Training Compute-Optimal Large Language Models](#training-compute-optimal-large-language-models-by-hoffmann-et-al)
    - [FlashAttention](#flashattention-by-dao-et-al)
    - [PagedAttention](#pagedattention-by-kwon-et-al)

12. [**Local and Open Models**](#local-and-open-models)

    Learn the tradeoffs around open weights, local inference, quantization, privacy, and model selection.

    - [LLM Course](#llm-course-by-hugging-face)
    - [llama.cpp](#llamacpp-by-ggml-org)
    - [Open LLM Leaderboard](#open-llm-leaderboard-by-hugging-face)
    - [Model Cards](#model-cards-by-hugging-face)

13. [**Interpretability, Safety, and Security**](#interpretability-safety-and-security)

    Learn how people inspect, constrain, secure, and govern learned systems.

    - [The Building Blocks of Interpretability](#the-building-blocks-of-interpretability-by-olah-et-al)
    - [A Mathematical Framework for Transformer Circuits](#a-mathematical-framework-for-transformer-circuits-by-elhage-et-al)
    - [Concrete Problems in AI Safety](#concrete-problems-in-ai-safety-by-amodei-et-al)
    - [OWASP Top 10 for LLM Applications](#owasp-top-10-for-llm-applications-by-owasp)
    - [AI Risk Management Framework](#ai-risk-management-framework-by-nist)

## Machine Learning Quick Start

TODO: Write a quick blurb explaining why this section matters.

### [The Hundred-Page Machine Learning Book](https://themlbook.com/) by Andriy Burkov

Why read it: This is the shortest serious pass through classical ML, loss, optimization, generalization, and model selection.



### [Intro to Machine Learning](https://www.kaggle.com/learn/intro-to-machine-learning) by Kaggle

Why read it: It gets you training, validating, and debugging a small model in code instead of only reading definitions.



### [Neural Networks](https://www.3blue1brown.com/topics/neural-networks) by 3Blue1Brown

Why read it: It gives visual intuition for gradients, backpropagation, and representation learning before the math gets dense.



### [Practical Deep Learning for Coders](https://course.fast.ai/) by fast.ai

Why read it: It builds deep learning intuition from working models and is especially strong for software engineers who learn by building.



### [Learn the Basics](https://docs.pytorch.org/tutorials/beginner/basics/intro.html) by PyTorch

Why read it: It teaches the modern tensor, autograd, dataset, model, and training-loop workflow used in real projects.

## Understanding Research vs Engineering

TODO: Write a quick blurb explaining why this section matters.

### [How to Read a Paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf) by S. Keshav

Why read it: It gives a practical three-pass method for reading technical papers without getting stuck in every detail.



### [Semantic Scholar](https://www.semanticscholar.org/)

Why use it: Citation graphs help you find what a result builds on and which later papers took it seriously.



### [Hugging Face Papers](https://huggingface.co/papers) and [Papers With Code](https://paperswithcode.com/)

Why use them: They are useful for discovery, code, datasets, and benchmark context when a paper becomes part of the current conversation.



### [AI Index 2025](https://arxiv.org/abs/2504.07139) by Stanford HAI

Why read it: It gives a broad annual map of progress, investment, adoption, and benchmark movement so individual papers have context.

## Core Machine Learning Principles

TODO: Write a quick blurb explaining why this section matters.

### [A Few Useful Things to Know About Machine Learning](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf) by Pedro Domingos

Why read it: It is a compact, durable explanation of generalization, overfitting, data, representation, and model selection.



### [Machine Learning Yearning](https://www.deeplearning.ai/machine-learning-yearning/) by Andrew Ng

Why read it: It teaches practical error analysis, train/dev/test splits, metric choice, and iteration strategy.



### [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml/) by Martin Zinkevich

Why read it: It captures hard-won lessons for launching, debugging, and improving ML systems over time.



### [Machine Learning Explainability](https://www.kaggle.com/learn/machine-learning-explainability) by Kaggle

Why read it: It gives quick tools for inspecting what a model learned and where that behavior may be brittle.

## Data, Training Signals, and Synthetic Data

TODO: Write a quick blurb explaining why this section matters.

### [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) by Gebru et al.

Why read it: It teaches the habit of documenting dataset motivation, composition, collection process, intended use, and limitations.



### [Data Cascades in High-Stakes AI](https://research.google/pubs/data-cascades-in-high-stakes-ai/) by Sambasivan et al.

Why read it: It shows how messy data decisions compound into downstream model and product failures.



### [DataComp](https://arxiv.org/abs/2304.14108) by Gadre et al.

Why read it: It makes dataset curation feel like an experimental variable rather than background plumbing.



### [Self-Instruct](https://arxiv.org/abs/2212.10560) by Wang et al.

Why read it: It is the classic recipe for bootstrapping instruction data from model outputs, which is central to synthetic-data thinking.

## Evaluation, Benchmarks, and Reliability

TODO: Write a quick blurb explaining why this section matters.

### [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain

Why read it: It makes the practical case that evals are the core loop for building AI products, not an academic afterthought.



### [HELM](https://arxiv.org/abs/2211.09110) by Liang et al.

Why read it: It shows what broader language-model evaluation looks like when you measure multiple scenarios and metrics.



### [Benchmark Data Contamination in LLMs: A Survey](https://arxiv.org/abs/2406.04244) by Li and Flanigan

Why read it: It explains why benchmark results can be misleading when training data overlaps with evaluation data.



### [Using the Evaluation Tool](https://platform.claude.com/docs/en/test-and-evaluate/eval-tool) by Anthropic

Why read it: It turns evals into concrete mechanics for comparing prompts, models, and task behavior.

## MLOps and AI Operations

TODO: Write a quick blurb explaining why this section matters.

### [Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/) by Chip Huyen

Why read it: It is the best durable reference for production ML system design, from data loops to monitoring and deployment.



### [Hidden Technical Debt in Machine Learning Systems](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems) by Sculley et al.

Why read it: It explains why production ML complexity compounds through data dependencies, feedback loops, configuration, and ownership gaps.



### [Full Stack Deep Learning](https://fullstackdeeplearning.com/course/)

Why read it: It gives an end-to-end view of training, deploying, and operating deep learning systems.



### [Made With ML](https://madewithml.com/) by Goku Mohandas

Why read it: It is a practical MLOps path from product framing through deployment and monitoring.

## Model Architectures and Reasoning

TODO: Write a quick blurb explaining why this section matters.

### [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) by Andrej Karpathy

Why watch it: It is the clearest high-level explanation of what LLMs are, how they are trained, and why they behave the way they do.



### [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) by Jay Alammar

Why read it: It gives the best visual bridge into attention and transformer blocks before reading the original paper.



### [Attention Is All You Need](https://arxiv.org/abs/1706.03762) by Vaswani et al.

Why read it: It is the original transformer paper and the cleanest source for the mechanism that reshaped modern AI.



### [Mamba](https://arxiv.org/abs/2312.00752) by Gu and Dao

Why read it: It introduces the modern state-space alternative to attention for long sequence modeling.



### [Learning to Reason with LLMs](https://openai.com/index/learning-to-reason-with-llms/) by OpenAI

Why read it: It frames how train-time and test-time compute can change reasoning behavior in modern models.

## Retrieval and Context

TODO: Write a quick blurb explaining why this section matters.

### [The Illustrated Word2vec](https://jalammar.github.io/illustrated-word2vec/) by Jay Alammar

Why read it: It is the best visual starting point for embeddings, vector similarity, and learned representations.



### [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) by Lewis et al.

Why read it: It is the original RAG paper and explains the core problem framing behind retrieval-augmented generation and grounded answers.



### [Lost in the Middle](https://arxiv.org/abs/2307.03172) by Liu et al.

Why read it: It shows why long context is not the same as reliable use of context or reliable grounding.



### [Building Agentic RAG with LlamaIndex](https://www.deeplearning.ai/courses/building-agentic-rag-with-llamaindex) by DeepLearning.AI

Why take it: It gives a compact hands-on bridge from retrieval systems to agentic workflows.

## Agents, Memory, and Tool Use

TODO: Write a quick blurb explaining why this section matters.

### [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) by Anthropic

Why read it: It gives practical patterns for workflows, agent harnesses, tools, and when to keep systems simple.



### [ReAct](https://arxiv.org/abs/2210.03629) by Yao et al.

Why read it: It is the canonical paper on interleaving reasoning traces and tool actions.



### [Toolformer](https://arxiv.org/abs/2302.04761) by Schick et al.

Why read it: It gives a research framing for how models can learn when tool calls are useful.



### [12-Factor Agents](https://github.com/humanlayer/12-factor-agents) by HumanLayer

Why read it: It gives production design principles for agent harnesses that control prompts, context, tools, state, and human feedback.



### [MemGPT](https://arxiv.org/abs/2310.08560) by Packer et al.

Why read it: It gives a practical framing of external memory management for long-running LLM agents.



### [Continual Lifelong Learning with Neural Networks](https://arxiv.org/abs/1802.07569) by Parisi et al.

Why read it: It explains catastrophic forgetting and the continual-learning strategies behind durable agent memory.

## Post-Training and Alignment

TODO: Write a quick blurb explaining why this section matters.

### [Training Language Models to Follow Instructions with Human Feedback](https://arxiv.org/abs/2203.02155) by Ouyang et al.

Why read it: It is the InstructGPT paper and explains the supervised tuning plus RLHF pipeline that shaped modern assistants.



### [RLHF Book](https://rlhfbook.com/) by Nathan Lambert

Why read it: It is the best structured path into preference data, reward models, policy optimization, and post-training tradeoffs.



### [Direct Preference Optimization](https://arxiv.org/abs/2305.18290) by Rafailov et al.

Why read it: It is the cleanest starting point for preference optimization without training an explicit reward model.



### [PEFT](https://huggingface.co/docs/peft/index) by Hugging Face

Why read it: It is the standard practical starting point for LoRA and adapter-based fine-tuning.



### [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) by Hinton, Vinyals, and Dean

Why read it: It is the classic paper on compressing useful behavior into smaller models.

## Training and Inference Infrastructure

TODO: Write a quick blurb explaining why this section matters.

### [Machine Learning Systems](https://mlsysbook.ai/)

Why read it: It explains the hardware and software stack behind ML systems without assuming you already live in infrastructure.



### [The Ultra-Scale Playbook](https://huggingface.co/spaces/nanotron/ultrascale-playbook) by Hugging Face/nanotron

Why read it: It gives unusually clear intuition for distributed training, parallelism, GPU memory, and bottlenecks.



### [Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556) by Hoffmann et al.

Why read it: It is the Chinchilla paper and explains compute, data, and model-size tradeoffs.



### [FlashAttention](https://arxiv.org/abs/2205.14135) by Dao et al.

Why read it: It makes attention performance feel like a memory-traffic problem rather than only a math problem.



### [PagedAttention](https://arxiv.org/abs/2309.06180) by Kwon et al.

Why read it: It explains the key serving idea behind vLLM-style high-throughput inference.

## Local and Open Models

TODO: Write a quick blurb explaining why this section matters.

### [LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) by Hugging Face

Why read it: It is the ecosystem tour for tokenizers, Transformers, datasets, fine-tuning, and the Hub.



### [llama.cpp](https://github.com/ggml-org/llama.cpp) by ggml-org

Why read it: It is the practical reference point for local inference and quantized models.



### [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) by Hugging Face

Why use it: It is a useful snapshot of open-model tradeoffs, but only if you read it with benchmark caveats in mind.



### [Model Cards](https://huggingface.co/docs/hub/model-cards) by Hugging Face

Why read it: Model cards teach the habit to check license, data, intended use, and limitations before using open weights.

## Interpretability, Safety, and Security

TODO: Write a quick blurb explaining why this section matters.

### [The Building Blocks of Interpretability](https://distill.pub/2018/building-blocks/) by Olah et al.

Why read it: It gives visual intuition for hidden representations and interpretability interfaces.



### [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) by Elhage et al.

Why read it: It is the clearest entry into mechanistic interpretability for transformers.



### [Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565) by Amodei et al.

Why read it: It gives a practical taxonomy of accidents, reward hacking, shift, and supervision.



### [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) by OWASP

Why read it: It is the shortest serious map of LLM application security risks.



### [AI Risk Management Framework](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf) by NIST

Why read it: It gives governance vocabulary for mapping, measuring, managing, and monitoring AI risk.

**Questions?** [Message me on X](https://x.com/loganthorneloe).
