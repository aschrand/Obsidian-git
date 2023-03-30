---
created: 2023-03-01T10:07:41 (UTC +01:00)
tags: [AI]
source: https://blogs.nvidia.com/blog/2023/01/26/what-are-large-language-models-used-for/
author: Angie Lee
type: artikel
---

> ## Excerpt
> Large language models recognize, summarize, translate, predict and generate text and other content.

---
AI applications are summarizing articles, writing stories and engaging in long conversations — and large language models are doing the heavy lifting.

A large language model, or LLM, is a deep learning algorithm that can recognize, summarize, translate, predict and generate text and other content based on knowledge gained from massive datasets.

Large language models are among the most successful applications of [transformer models](https://blogs.nvidia.com/blog/2022/03/25/what-is-a-transformer-model/). They aren’t just for teaching AIs human languages, but for understanding proteins, writing software code, and much, much more.

In addition to accelerating natural language processing applications — like translation, chatbots and AI assistants — large language models are used in [healthcare](https://blogs.nvidia.com/blog/2022/09/20/bionemo-large-language-models-drug-discovery/), software development and use cases in [many other fields](https://blogs.nvidia.com/blog/2022/10/10/llms-ai-horizon/).

## **What Are Large Language Models Used For?**

Language is used for more than human communication.

Code is the language of computers. Protein and molecular sequences are the language of biology. Large language models can be applied to such languages or scenarios in which communication of different types is needed.

These models broaden AI’s reach across industries and enterprises, and are expected to enable a new wave of research, creativity and productivity, as they can help to generate complex solutions for the world’s toughest problems.

For example, an AI system using large language models can learn from a database of molecular and protein structures, then use that knowledge to provide viable chemical compounds that help scientists develop groundbreaking vaccines or treatments.

Large language models are also helping to create reimagined search engines, tutoring chatbots, composition tools for songs, poems, stories and marketing materials, and more.

## **How Do Large Language Models Work?**

Large language models learn from huge volumes of data. As its name suggests, central to an LLM is the size of the dataset it’s trained on. But the definition of “large” is growing, along with AI.

Now, large language models are typically trained on datasets large enough to include nearly everything that has been written on the internet over a large span of time.

Such massive amounts of text are fed into the AI algorithm using [unsupervised learning](https://blogs.nvidia.com/blog/2018/08/02/supervised-unsupervised-learning/) — when a model is given a dataset without explicit instructions on what to do with it. Through this method, a large language model learns words, as well as the relationships between and concepts behind them. It could, for example, learn to differentiate the two meanings of the word “bark” based on its context.

And just as a person who masters a language can guess what might come next in a sentence or paragraph — or even come up with new words or concepts themselves — a large language model can apply its knowledge to predict and generate content.

Large language models can also be customized for specific use cases, including through techniques like fine-tuning or prompt-tuning, which is the process of feeding the model small bits of data to focus on, to train it for a specific application.

Thanks to its computational efficiency in processing sequences in parallel, the transformer model architecture is the building block behind the largest and most powerful LLMs.

## **Top Applications for Large Language Models**

Large language models are unlocking new possibilities in areas such as search engines, natural language processing, healthcare, robotics and code generation.

The popular [ChatGPT](https://openai.com/blog/chatgpt/) AI chatbot is one application of a large language model. It can be used for a myriad of natural language processing tasks.

The nearly infinite applications for LLMs also include:

-   [Retailers and other service providers](https://blogs.nvidia.com/blog/2022/09/20/kt-large-language-models/) can use large language models to provide improved customer experiences through dynamic chatbots, AI assistants and more.
-   Search engines can use large language models to provide more direct, human-like answers.
-   [Life science researchers](https://blogs.nvidia.com/blog/2022/09/20/bionemo-large-language-models-drug-discovery/) can train large language models to understand proteins, molecules, DNA and RNA.
-   Developers can [write software](https://www.tabnine.com/) and [teach robots physical tasks](https://www.deepmind.com/publications/a-generalist-agent) with large language models.
-   Marketers can train a large language model to organize customer feedback and requests into clusters, or segment products into categories based on product descriptions.
-   [Financial advisors](https://blogs.nvidia.com/blog/2021/12/08/ai-accelerating-financial-services/) can summarize earnings calls and create transcripts of important meetings using large language models. And credit-card companies can use LLMs for anomaly detection and fraud analysis to protect consumers.
-   [Legal teams](https://soundcloud.com/theaipodcast/lawyers-ai-legal-lawgeex) can use large language models to help with legal paraphrasing and scribing.

Running these massive models in production efficiently is resource-intensive and requires expertise, among other challenges, so [enterprises](https://blogs.nvidia.com/blog/2022/10/05/ai-large-language-models-triton/) turn to [NVIDIA Triton Inference Server](https://developer.nvidia.com/nvidia-triton-inference-server), software that helps standardize model deployment and deliver fast and scalable AI in production.

## **Where to Find Large Language Models**

In June 2020, OpenAI released [GPT-3](https://openai.com/blog/gpt-3-apps/) as a service, powered by a 175-billion-parameter model that can generate text and code with short written prompts.

In 2021, NVIDIA and Microsoft developed [Megatron-Turing Natural Language Generation 530B](https://developer.nvidia.com/blog/using-deepspeed-and-megatron-to-train-megatron-turing-nlg-530b-the-worlds-largest-and-most-powerful-generative-language-model/), one of the world’s largest models for reading comprehension and natural language inference, which eases tasks like summarization and content generation.

And HuggingFace last year introduced [BLOOM](https://bigscience.huggingface.co/blog/bloom), an open large language model that’s able to generate text in 46 natural languages and over a dozen programming languages.

Another LLM, [Codex](https://openai.com/blog/openai-codex/), turns text to code for software engineers and other developers.

NVIDIA offers tools to ease the building and deployment of large language models:

-   [NVIDIA NeMo LLM service](https://www.nvidia.com/en-us/gpu-cloud/nemo-llm-service/) provides a fast path to customizing large language models and deploying them at scale using NVIDIA’s managed cloud API, or through private and public clouds.
-   [NVIDIA NeMo Megatron](https://developer.nvidia.com/nemo/megatron), part of the NVIDIA AI platform, is a framework for easy, efficient, cost-effective training and deployment of large language models. Designed for enterprise application development, NeMo Megatron provides an end-to-end workflow for automated distributed data processing; training large-scale, customized model types including GPT-3 and T5; and deploying these models for inference at scale.
-   [NVIDIA BioNeMo](https://www.nvidia.com/en-us/gpu-cloud/bionemo/) is a domain-specific managed service and framework for large language models in proteomics, small molecules, DNA and RNA. It’s built on NVIDIA NeMo Megatron for training and deploying large biomolecular transformer AI models at supercomputing scale.

## **Challenges of Large Language Models**

Scaling and maintaining large language models can be difficult and expensive.

Building a foundational large language model often requires months of training time and millions of dollars.

And because LLMs require a significant amount of training data, developers and enterprises can find it a challenge to access large-enough datasets.

Due to the scale of large language models, deploying them requires technical expertise, including a strong understanding of deep learning, transformer models and distributed software and hardware.

Many leaders in tech are working to advance development and build resources that can expand access to large language models, allowing consumers and enterprises of all sizes to reap their benefits.
