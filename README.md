# AI Problems Guide

An opinionated list of unusually good resources for building intuition about modern AI.

This is not a complete curriculum. It is intentionally short.

The bar for inclusion is that a resource should span a meaningful body of knowledge, not just explain one isolated trick. The best resources here should help you build taste, connect ideas, and understand a subject well enough to reason from first principles when you hit a real problem.

Tags are scan aids. The colored badges mark format, subject, and whether the resource has a meaningful implementation, exercise, workbook, or companion repo.

This is an **[AI for Software Engineers](https://aiforswes.com)** resource. **[Subscribe](https://aiforswes.com/subscribe)** for more fundamentals and technical deep dives.

## Machine Learning Foundations

This section is for building the shared base layer. If you want to build useful AI systems, you need enough programming fluency, ML vocabulary, math intuition, and deep learning mechanics to understand what the model is doing and why it fails.

### Programming Fluency

#### [Elements of Programming Interviews in Python](https://www.amazon.com/Elements-Programming-Interviews-Python-Insiders/dp/1537713949) by Adnan Aziz, Tsung-Hsien Lee, and Amit Prakash

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Python](https://img.shields.io/badge/Python-1565C0?style=flat-square) ![Algorithms](https://img.shields.io/badge/algorithms-2E7D32?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square)

Useful if Python fluency blocks you from implementing small models, data pipelines, or learning exercises.

### Core Machine Learning

#### [The Hundred-Page Machine Learning Book](https://themlbook.com/) by Andriy Burkov

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![ML foundations](https://img.shields.io/badge/ML%20foundations-1565C0?style=flat-square) ![Classical ML](https://img.shields.io/badge/classical%20ML-2E7D32?style=flat-square)

The shortest serious pass through classical ML, loss, optimization, generalization, and model selection.


#### [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/) by Aurelien Geron

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Applied ML](https://img.shields.io/badge/applied%20ML-1565C0?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

A broad applied path from classical ML through deep learning, with runnable examples for engineers who learn by building.

**Companion code**

[ageron/handson-ml3](https://github.com/ageron/handson-ml3)

### Math for Models

#### [Mathematics of Machine Learning](https://www.packtpub.com/en-us/product/mathematics-of-machine-learning-9781837027873) by Tivadar Danka

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Math](https://img.shields.io/badge/math-00838F?style=flat-square) ![Linear algebra](https://img.shields.io/badge/linear%20algebra-2E7D32?style=flat-square) ![Probability](https://img.shields.io/badge/probability-2E7D32?style=flat-square)

A structured path through linear algebra, calculus, and probability for machine learning.


#### The Deep Learning Math Workbook by Professor Tom Yeh

![Workbook](https://img.shields.io/badge/workbook-455A64?style=flat-square) ![Math](https://img.shields.io/badge/math-00838F?style=flat-square) ![Deep learning](https://img.shields.io/badge/deep%20learning-1565C0?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square)

Useful when neural networks, gradients, tensors, and training math still feel too abstract.

### Deep Learning Mechanics

#### [Deep Learning with Python, Third Edition](https://www.manning.com/books/deep-learning-with-python-third-edition) by Francois Chollet and Matthew Watson

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Deep learning](https://img.shields.io/badge/deep%20learning-1565C0?style=flat-square) ![Keras](https://img.shields.io/badge/Keras-D32F2F?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square)

A practical deep learning book for model building, training, and modern neural network workflows.


#### [Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero) by Andrej Karpathy

![Course](https://img.shields.io/badge/course-455A64?style=flat-square) ![Deep learning](https://img.shields.io/badge/deep%20learning-1565C0?style=flat-square) ![LLMs](https://img.shields.io/badge/LLMs-6A1B9A?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

A from-scratch path through backprop, language modeling, tensors, training loops, GPT, and tokenization.

## Engineering for ML/AI

This section is for turning foundations into useful ML and AI systems. The emphasis is on product judgment, data and systems design, evals, deployment, inference, LLM internals, post-training, and agent workflows.

### Research Versus Engineering

#### [The Art of Doing Science and Engineering](https://www.stripe.press/art-of-doing-science-and-engineering) by Richard Hamming

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Research taste](https://img.shields.io/badge/research%20taste-00838F?style=flat-square) ![Learning](https://img.shields.io/badge/learning-2E7D32?style=flat-square)

A mindset book for choosing important problems, learning how to learn, and thinking clearly about technical work.

### Systems Programming and Data Infrastructure

#### [Elements of Programming Interviews in C++](https://www.amazon.com/Elements-Programming-Interviews-Adnan-Aziz/dp/1479274836) by Adnan Aziz, Tsung-Hsien Lee, and Amit Prakash

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![C++](https://img.shields.io/badge/C%2B%2B-1565C0?style=flat-square) ![Systems](https://img.shields.io/badge/systems-2E7D32?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square)

Useful when reading performance-sensitive inference, kernels, runtimes, and systems code.


#### [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/) by Martin Kleppmann

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Systems](https://img.shields.io/badge/systems-2E7D32?style=flat-square) ![Data infrastructure](https://img.shields.io/badge/data%20infrastructure-1565C0?style=flat-square)

The systems book for storage, streams, replication, consistency, reliability, and data infrastructure.

### ML Systems and Operations

#### [Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/) by Chip Huyen

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![ML systems](https://img.shields.io/badge/ML%20systems-1565C0?style=flat-square) ![MLOps](https://img.shields.io/badge/MLOps-2E7D32?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

The best durable reference for production ML system design, from data loops to monitoring and deployment.

**Companion code**

[chiphuyen/dmls-book](https://github.com/chiphuyen/dmls-book)


#### [Made With ML](https://madewithml.com/) by Goku Mohandas

![Course](https://img.shields.io/badge/course-455A64?style=flat-square) ![MLOps](https://img.shields.io/badge/MLOps-2E7D32?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

A practical MLOps path from product framing through deployment and monitoring.

**Companion code**

[GokuMohandas/Made-With-ML](https://github.com/GokuMohandas/Made-With-ML)

### AI Product Engineering

#### [AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) by Chip Huyen

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![AI engineering](https://img.shields.io/badge/AI%20engineering-1565C0?style=flat-square) ![LLM apps](https://img.shields.io/badge/LLM%20apps-6A1B9A?style=flat-square)

The best broad resource for building products on foundation models, including prompting, retrieval, agents, evals, and deployment tradeoffs.


#### [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain

![Essay](https://img.shields.io/badge/essay-455A64?style=flat-square) ![Evals](https://img.shields.io/badge/evals-D32F2F?style=flat-square) ![AI products](https://img.shields.io/badge/AI%20products-1565C0?style=flat-square)

The clearest practical argument that evals are the core engineering loop for improving AI products.


#### [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) by Anthropic

![Guide](https://img.shields.io/badge/guide-455A64?style=flat-square) ![Agents](https://img.shields.io/badge/agents-6A1B9A?style=flat-square) ![Tool use](https://img.shields.io/badge/tool%20use-2E7D32?style=flat-square) ![Workflows](https://img.shields.io/badge/workflows-1565C0?style=flat-square)

A compact resource for designing agent workflows, tool use, autonomy, and when to keep systems simple.

### LLM Internals

#### [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) by Andrej Karpathy

![Video](https://img.shields.io/badge/video-455A64?style=flat-square) ![LLMs](https://img.shields.io/badge/LLMs-6A1B9A?style=flat-square) ![High-level](https://img.shields.io/badge/high--level-00838F?style=flat-square)

A high-level map of what LLMs are, how they are trained, and why they behave the way they do.


#### [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) by Jay Alammar

![Explainer](https://img.shields.io/badge/explainer-455A64?style=flat-square) ![Transformers](https://img.shields.io/badge/transformers-6A1B9A?style=flat-square) ![Visual](https://img.shields.io/badge/visual-00838F?style=flat-square)

The clearest visual explanation of attention and transformer blocks before reading code or papers.


#### [Hands-On Large Language Models](https://www.oreilly.com/library/view/hands-on-large-language/9781098150952/) by Jay Alammar and Maarten Grootendorst

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![LLMs](https://img.shields.io/badge/LLMs-6A1B9A?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

A broad, visual LLM guide covering embeddings, transformers, retrieval, fine-tuning, and practical workflows.

**Companion code**

[HandsOnLLM/Hands-On-Large-Language-Models](https://github.com/HandsOnLLM/Hands-On-Large-Language-Models)


#### [nanoGPT](https://github.com/karpathy/nanoGPT) by Andrej Karpathy

![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square) ![LLMs](https://img.shields.io/badge/LLMs-6A1B9A?style=flat-square) ![Training](https://img.shields.io/badge/training-2E7D32?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square)

A compact reference implementation for training and fine-tuning GPT-style models without a giant framework.


#### [Build a Large Language Model From Scratch](https://www.manning.com/books/build-a-large-language-model-from-scratch) by Sebastian Raschka

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![LLMs](https://img.shields.io/badge/LLMs-6A1B9A?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

The code-level path from tokenizer and transformer blocks through pretraining and fine-tuning.

**Companion code**

[rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)

### Post-Training and Reasoning

#### [Build a Reasoning Model From Scratch](https://www.manning.com/books/build-a-reasoning-model-from-scratch) by Sebastian Raschka

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Reasoning](https://img.shields.io/badge/reasoning-6A1B9A?style=flat-square) ![Post-training](https://img.shields.io/badge/post--training-D32F2F?style=flat-square) ![Hands-on](https://img.shields.io/badge/hands--on-E65100?style=flat-square) ![Code](https://img.shields.io/badge/code-6A1B9A?style=flat-square)

A hands-on bridge from general LLM mechanics into reasoning datasets, reinforcement learning, and verifiable rewards.

**Companion code**

[rasbt/reasoning-from-scratch](https://github.com/rasbt/reasoning-from-scratch)


#### [RLHF Book](https://rlhfbook.com/) by Nathan Lambert

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![RLHF](https://img.shields.io/badge/RLHF-D32F2F?style=flat-square) ![Post-training](https://img.shields.io/badge/post--training-D32F2F?style=flat-square)

The best structured path into preference data, reward models, policy optimization, and post-training tradeoffs.

### Inference and Scaling

#### [Inference Engineering](https://www.baseten.co/inference-engineering/) by Philip Kiely

![Guide](https://img.shields.io/badge/guide-455A64?style=flat-square) ![Inference](https://img.shields.io/badge/inference-D32F2F?style=flat-square) ![Serving](https://img.shields.io/badge/serving-2E7D32?style=flat-square) ![Production](https://img.shields.io/badge/production-1565C0?style=flat-square)

Useful for understanding the engineering layer between a trained model and a fast, reliable, cost-aware product experience.


#### [How to Scale Your Model](https://jax-ml.github.io/scaling-book/) by Jacob Austin et al.

![Book](https://img.shields.io/badge/book-455A64?style=flat-square) ![Scaling](https://img.shields.io/badge/scaling-1565C0?style=flat-square) ![Training](https://img.shields.io/badge/training-2E7D32?style=flat-square) ![Inference](https://img.shields.io/badge/inference-D32F2F?style=flat-square)

A systems view of scaling LLM training and inference across TPUs and GPUs, with practical intuition for rooflines, parallelism, memory, profiling, and serving.

**Questions?** [Message me on X](https://x.com/loganthorneloe).
