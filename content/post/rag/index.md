---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Understanding RAG: What is this thing?"
subtitle: ""
summary: "Simply put, RAG combines LLMs with an external knowledge retrieval mechanism to fetch up-to-date relevant information without having to retrain the LLM."
authors: []
tags: []
categories: ["RAG"]
date: 2025-08-16
lastmod: 2025-08-16
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Wenqi Fan, Yujuan Ding, Liangbo Ning, Shijie Wang, Hengyun Li, Dawei Yin, Tat-Seng Chua, and Qing Li. 2024. A Survey on RAG Meeting LLMs: Towards Retrieval-Augmented Large Language Models. In Proceedings of the 30th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD ‘24). Association for Computing Machinery, New York, NY, USA, 6491–6501. https://doi.org/10.1145/3637528.3671470"
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## Table of Contents
1. [What is RAG?](#what-is-rag)
2. [What goes into a RAG?](#what-goes-into-rag)
   1. [Retrieval](#retrieval)
   2. [Pre-retrieval and Post-retrieval Enhancement](#enhancement)
   3. [Augmentation](#augmentation)
   4. [Generation](#generation)

<a href="https://medium.com/@bajra.pradeep/understanding-rag-what-is-this-thing-41a48611d856">READ IN MEDIUM</a>

Large Language Models (LLMs) have swept the world off its feet with its remarkable ability to apparently do almost anything. It is able to perform a wide variety of tasks that were previously considered “human”. From generating coherent text, summarization of documents, and language translation to more complex tasks like creative writing, and reasoning. It is able to do these wonders, to put simply, is because they are fundamentally statistical models that have been trained on an insanely vast amounts of text data.

These models, however, aren’t without limitations. One of the common problem that LLMs face is hallucination where the model produces information that is outdated or incorrect or non-factual. This is where <b>Retrieval-Augmented Generation (RAG)</b> comes to the rescue. In this post, we will go through a TL;DR approach to understanding RAG borrowing information from the survey paper titled “<a href="https://dl.acm.org/doi/pdf/10.1145/3637528.3671470">A Survey on RAG Meets LLMs: Towards Retrieval-Augmented Large Language Models</a>”.

<h2 id="what-is-rag">What is RAG?</h2>
Without RAG, if you ask the questions like “Who won the last Premiere League?” If the model was not upto date, the conversation might go something like below

<blockquote>User: Who won the last Premiere League?<br/>
Assistant: Manchester City won the Premiere League in 2022</blockquote>

This isn’t wrong but it isn’t what we expected either. We were expecting the answer to be the up to date as Liverpool

Simply put, RAG combines LLMs with an external knowledge retrieval mechanism to fetch up-to-date relevant information without having to retrain the LLM.

<h2 id="what-goes-into-rag">What goes into a RAG?</h2>
The following figure borrowed from the <a href="https://dl.acm.org/doi/pdf/10.1145/3637528.3671470">survey paper</a> shows a detailed illustration of a RAG combined with LLM and what goes into it. It mainly consists of <b>Retrieval</b>, <b>Augmentation</b> and <b>Generation</b>.

<h3 id="retrieval">Retrieval</h3>
The main component is the source of information i.e. an external database which can be open-sourced or closed-source stored as a database, document corpus, or vector store. Based on the information and its encoding methods, the retrievals can be sparse or dense.

In sparse retrievers, they use word based comparison or embedding like TF-IDF to find similar documents chunks from retriever. We cannot train these as the measures depend on terms as term frequency, document frequency which depends strongly on the quality of documents and query

Contrary to sparse retrievers, dense retrievers first split the query and documents into “chunks” and the chunks can vary from tokens to texts to documents. The chunks are then converted to vector embeddings which will be indexed for retrieval. There are different ways we can train these model to output an embedding which is the main difference between the two. The paper goes into detail of different retriever design which we will skip for now and maybe explore in future posts.

<h3 id="enhancement">Pre-retrieval and Post-retrieval Enhancement</h3>
To ensure the information fetched by the retriever is accurate and relevant, various pre-retrieval and post-retrieval strategies have been proposed. Among the pre-retrieval strategies, there are three broader categories

<ol>
<li><b>Query Expansion</b>: The prompt provided by the user is processed by the LLM and using the relevant information obtained from the response by few-shot prompting the LLMs, the query is expanded.</li>
<li><b>Query Rewrite</b>: The LLM itself is used to rephrase the query prompts from the user. This step is motivated by the fact that usually, the user prompts are not coherent and there is gap between the input text and the needed knowledge in retrieval.</li>
<li><b>Query Augmentation</b>: The original query is combined with the inital generated output to form a new query which is used to further retrieve relevant information.</li>

<blockquote>Post-retrieval enhancement denotes the procedure to process the extracted top-k documents from the retriever before feeding them to the generator</blockquote>
</ol>

<h3 id="augmentation">Augmentation</h3>
Based on how the retrieved information from the retriever is augmented with the query we get

Input-layer Augmentation: Combine the input query and the retrieved information before passing them to generate more coherent response from the generator
Output-layer Augmentation: The response from the generator based on the query is augmented with the retrieved information
Intermediate-layer Augmentation: The retrieved results are integrated with the internal layers of the generation model. It is most complex among the three and requires knowledge and access to the generation models.

<h3 id="generation">Generation</h3>
The design of generators in depends on downstream tasks and can be broadly categorized as white-box (parameter-accessible) or black-box (parameter-inaccessible) models.

White-box generators (BART, T5, etc), allow parameter optimization and can be trained to better integrate retrieved information, thereby improving accuracy and relevance in generation tasks. In contrast, black-box generators like GPT, Codex, and Claude do not expose internal structures or parameters, making direct fine-tuning impractical. Instead, they rely on retrieval enhancement strategies discussed above.

After all this, we get the a response that is more coherent and upto date. Coming back to the original question about Premiere League, we then could get an upto date answer

<blockquote>User: Who won the last Premiere League?<br />
Assistant: Liverpool FC won the Premiere League in 2025</blockquote>