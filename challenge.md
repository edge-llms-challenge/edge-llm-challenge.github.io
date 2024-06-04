---
layout: default
---

# Baselines, code, and material

<p style='text-align: justify;'>
The “starting kit” will be released to provide a starting point for people who are interested in our challenge before May 5th, 2024. This starting kit will provide detailed clarifications on what a submission looks like exactly, and how it will be evaluated and submitted. This starting kit will include an end-to-end submission flow, exemplified with a simple baseline:
 </p>

* Loading a large language model choosing from Phi-2, Llama3-8B, or Qwen-7B.
* Performing the basic L1 norm structured pruning on this model so that the compressed model can fit the smartphone.
* Evaluating the pruned model on the OpenCompass benchmark. We will provide an easy-to- tun pipeline for participants to evaluate their model on the subset of the lm-evaluation-harness benchmark.
* Deploying the resulting model on a smartphone and measuring its throughput. We will provide a tool that can help participants easily deploy their LLMs on smartphones and measure throughput. 
* Make a submission on the Leaderboard to see how we fare up against other competitors.

# Dataset

<p style='text-align: justify;'>
This competition will not evaluate submissions based on the analysis of data. Our competition features two tracks: (1) post-training LLM compression for edge devices; and (2) training edge LLMs from scratch. For the first track, we will allow the participants to use and only use the C4 dataset. For the second track, in addition to C4, the Alpaca, and Chinese Alpaca datasets are allowed for supervised fine-tuning to ensure the quality of trained models. The C4 dataset is a colossal, cleaned version of Common Crawl’s web crawl corpus, which is mainly intended to pre-train language models and word representations. Language models like MPT-7B and T5 are pre-trained with C4 dataset. C4 is a large enough dataset that can make the competition interesting and draw conclusive and statistically significant results. </p> 
* The C4 dataset is public and can be accessed through: [HuggingFace](https://huggingface.co/datasets/c4)
<br>

# Metrics

<p style='text-align: justify;'>

To comprehensively evaluate submissions, we employ a set of rigorously curated metrics, which include:
</p>

* Average Score: One of our primary scoring metrics is the average score on a subset of the OpenCompass benchmark. The average score is calculated as the geometric mean across all evaluation tasks. This metric assesses the language capacity of the submission across multiple fundamental dimensions.

* Throughput: The throughput of an LLM typically refers to the rate at which the model can process input data and generate output tokens. It is often measured in terms of tokens per second. Throughput is a critical metric for evaluating the efficiency and performance of LLMs, especially in real-time or near-real-time applications where the speed of processing is crucial. Achieving high throughput implies that the model can handle large volumes of data quickly, making it suitable for tasks requiring rapid language processing, such as live chatbots, real-time translation, or speech recognition systems. This value is expected to be measured on a smartphone with 12GB DRAM.

* Parameter count: Submissions should also include the model size, expressed as the parameter count, to indicate the model’s size.




