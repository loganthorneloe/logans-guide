# AI Problems Guide

An opinionated list of unusually good resources for building intuition about modern AI.

This is not a complete curriculum. It is intentionally short.

The bar for inclusion is that a resource should span a meaningful body of knowledge, not just explain one isolated trick. The best resources here should help you build taste, connect ideas, and understand a subject well enough to reason from first principles when you hit a real problem.

Tags are scan aids. <kbd>Hands-on</kbd> means the resource has a meaningful implementation, exercise, or workbook component. <kbd>Code</kbd> means there is a useful repo or source implementation linked.

This is an **[AI for Software Engineers](https://aiforswes.com)** resource. **[Subscribe](https://aiforswes.com/subscribe)** for more fundamentals and technical deep dives.

## ML Quick Start

### [The Hundred-Page Machine Learning Book](https://themlbook.com/) by Andriy Burkov

<kbd>Book</kbd> <kbd>ML foundations</kbd> <kbd>Classical ML</kbd>

**Why it matters**

The shortest serious pass through classical ML, loss, optimization, generalization, and model selection.


### [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/) by Aurelien Geron

<kbd>Book</kbd> <kbd>Applied ML</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

A broad applied path from classical ML through deep learning, with runnable examples for engineers who learn by building.

**Companion code**

[ageron/handson-ml3](https://github.com/ageron/handson-ml3)


### The Deep Learning Math Workbook by Professor Tom Yeh

<kbd>Workbook</kbd> <kbd>Math</kbd> <kbd>Deep learning</kbd> <kbd>Hands-on</kbd>

**Why it matters**

Useful when neural networks, gradients, tensors, and training math still feel too abstract.


### [Mathematics of Machine Learning](https://www.packtpub.com/en-us/product/mathematics-of-machine-learning-9781837027873) by Tivadar Danka

<kbd>Book</kbd> <kbd>Math</kbd> <kbd>Linear algebra</kbd> <kbd>Probability</kbd>

**Why it matters**

A structured path through linear algebra, calculus, and probability for machine learning.


### [Deep Learning with Python, Third Edition](https://www.manning.com/books/deep-learning-with-python-third-edition) by Francois Chollet and Matthew Watson

<kbd>Book</kbd> <kbd>Deep learning</kbd> <kbd>Keras</kbd> <kbd>Hands-on</kbd>

**Why it matters**

A practical deep learning book for model building, training, and modern neural network workflows.


### [Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero) by Andrej Karpathy

<kbd>Course</kbd> <kbd>Deep learning</kbd> <kbd>LLMs</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

A from-scratch path through backprop, language modeling, tensors, training loops, GPT, and tokenization.


### [Elements of Programming Interviews in Python](https://www.amazon.com/Elements-Programming-Interviews-Python-Insiders/dp/1537713949) by Adnan Aziz, Tsung-Hsien Lee, and Amit Prakash

<kbd>Book</kbd> <kbd>Python</kbd> <kbd>Algorithms</kbd> <kbd>Hands-on</kbd>

**Why it matters**

Useful if Python fluency blocks you from implementing small models, data pipelines, or learning exercises.

## Machine Learning and AI Engineering

### [The Art of Doing Science and Engineering](https://www.stripe.press/art-of-doing-science-and-engineering) by Richard Hamming

<kbd>Book</kbd> <kbd>Research taste</kbd> <kbd>Learning</kbd>

**Why it matters**

A mindset book for choosing important problems, learning how to learn, and thinking clearly about technical work.


### [Elements of Programming Interviews in C++](https://www.amazon.com/Elements-Programming-Interviews-Adnan-Aziz/dp/1479274836) by Adnan Aziz, Tsung-Hsien Lee, and Amit Prakash

<kbd>Book</kbd> <kbd>C++</kbd> <kbd>Systems</kbd> <kbd>Hands-on</kbd>

**Why it matters**

Useful when reading performance-sensitive inference, kernels, runtimes, and systems code.


### [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/) by Martin Kleppmann

<kbd>Book</kbd> <kbd>Systems</kbd> <kbd>Data infrastructure</kbd>

**Why it matters**

The systems book for storage, streams, replication, consistency, reliability, and data infrastructure.


### [Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/) by Chip Huyen

<kbd>Book</kbd> <kbd>ML systems</kbd> <kbd>MLOps</kbd> <kbd>Code</kbd>

**Why it matters**

The best durable reference for production ML system design, from data loops to monitoring and deployment.

**Companion code**

[chiphuyen/dmls-book](https://github.com/chiphuyen/dmls-book)


### [AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) by Chip Huyen

<kbd>Book</kbd> <kbd>AI engineering</kbd> <kbd>LLM apps</kbd>

**Why it matters**

The best broad resource for building products on foundation models, including prompting, retrieval, agents, evals, and deployment tradeoffs.


### [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain

<kbd>Essay</kbd> <kbd>Evals</kbd> <kbd>AI products</kbd>

**Why it matters**

The clearest practical argument that evals are the core engineering loop for improving AI products.


### [Made With ML](https://madewithml.com/) by Goku Mohandas

<kbd>Course</kbd> <kbd>MLOps</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

A practical MLOps path from product framing through deployment and monitoring.

**Companion code**

[GokuMohandas/Made-With-ML](https://github.com/GokuMohandas/Made-With-ML)


### [How to Scale Your Model](https://jax-ml.github.io/scaling-book/) by Jacob Austin et al.

<kbd>Book</kbd> <kbd>Scaling</kbd> <kbd>Training</kbd> <kbd>Inference</kbd>

**Why it matters**

A systems view of scaling LLM training and inference across TPUs and GPUs, with practical intuition for rooflines, parallelism, memory, profiling, and serving.


### [Inference Engineering](https://www.baseten.co/inference-engineering/) by Philip Kiely

<kbd>Guide</kbd> <kbd>Inference</kbd> <kbd>Serving</kbd> <kbd>Production</kbd>

**Why it matters**

Useful for understanding the engineering layer between a trained model and a fast, reliable, cost-aware product experience.


### [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) by Andrej Karpathy

<kbd>Video</kbd> <kbd>LLMs</kbd> <kbd>High-level</kbd>

**Why it matters**

A high-level map of what LLMs are, how they are trained, and why they behave the way they do.


### [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) by Jay Alammar

<kbd>Explainer</kbd> <kbd>Transformers</kbd> <kbd>Visual</kbd>

**Why it matters**

The clearest visual explanation of attention and transformer blocks before reading code or papers.


### [Hands-On Large Language Models](https://www.oreilly.com/library/view/hands-on-large-language/9781098150952/) by Jay Alammar and Maarten Grootendorst

<kbd>Book</kbd> <kbd>LLMs</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

A broad, visual LLM guide covering embeddings, transformers, retrieval, fine-tuning, and practical workflows.

**Companion code**

[HandsOnLLM/Hands-On-Large-Language-Models](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models)


### [nanoGPT](https://github.com/karpathy/nanoGPT) by Andrej Karpathy

<kbd>Code</kbd> <kbd>LLMs</kbd> <kbd>Training</kbd> <kbd>Hands-on</kbd>

**Why it matters**

A compact reference implementation for training and fine-tuning GPT-style models without a giant framework.


### [Build a Large Language Model From Scratch](https://www.manning.com/books/build-a-large-language-model-from-scratch) by Sebastian Raschka

<kbd>Book</kbd> <kbd>LLMs</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

The code-level path from tokenizer and transformer blocks through pretraining and fine-tuning.

**Companion code**

[rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)


### [Build a Reasoning Model From Scratch](https://www.manning.com/books/build-a-reasoning-model-from-scratch) by Sebastian Raschka

<kbd>Book</kbd> <kbd>Reasoning</kbd> <kbd>Post-training</kbd> <kbd>Hands-on</kbd> <kbd>Code</kbd>

**Why it matters**

A hands-on bridge from general LLM mechanics into reasoning datasets, reinforcement learning, and verifiable rewards.

**Companion code**

[rasbt/reasoning-from-scratch](https://github.com/rasbt/reasoning-from-scratch)


### [RLHF Book](https://rlhfbook.com/) by Nathan Lambert

<kbd>Book</kbd> <kbd>RLHF</kbd> <kbd>Post-training</kbd>

**Why it matters**

The best structured path into preference data, reward models, policy optimization, and post-training tradeoffs.


### [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) by Anthropic

<kbd>Guide</kbd> <kbd>Agents</kbd> <kbd>Tool use</kbd> <kbd>Workflows</kbd>

**Why it matters**

A compact resource for designing agent workflows, tool use, autonomy, and when to keep systems simple.

**Questions?** [Message me on X](https://x.com/loganthorneloe).
