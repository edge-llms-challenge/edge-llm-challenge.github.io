---
layout: default
---
# Tracks

<p style='text-align: justify;'>
1. <b> Post-training LLM compression for edge devices:</b> teams are required to come up with their own compression approaches to reduce the size of three pre-trained LLMs separately: Phi-2, Llama3-7B, and Qwen-7B. The submitted compressed models should operate on a smartphone with 12 GB DRAM. Entries will be evaluated based on the averaged scores of the three models on a portion of the OpenCompass benchmark, which performs an in-depth and holistic assessment of LLMs across multiple fundamental dimensions. 
 
2. <b> Training edge LLMs from scratch:</b> involves training language models from scratch without leveraging any pre-trained LLMs. No limitations are placed on model designs, training procedures, or time as long as the final models can run on a smartphone with 12 GB DRAM. Participants can either design their architectures or leverage existing LLM architectures to fulfill this task.  Although, there is a restriction on the training data; only the C4 and Alpaca datasets are allowed for training and fine-tuning respectively.
  
<b>Please note that no quantization methods are allowed</b> since 8-bit or 4-bit quantization for LLMs is already a well-established technique. Instead, participants must submit models in FP16 or FP32 formats.
</p>

# Metrics

<p style='text-align: justify;'>

To comprehensively evaluate submissions, we will employ a set of rigorously curated metrics, which include:
</p>

* <b>Performance Score:</b> One of our primary scoring metrics is the performance score on the selected evaluation task. Each submission will be ranked individually for each task based on the performance score, with the top 10 submissions per task receiving scores from 10 to 1. The final score of the submission is calculated as the sum across all evaluation tasks.
  
*<b>Memory Requirement:</b> The memory footprint during inference is a crucial metric for real-life edge devices. To qualify, the peak memory usage of all models must be less than 12GB.

* <b>Throughput:</b> The throughput of an LLM typically refers to the rate at which the model can process input data and generate output tokens. It is often measured in terms of tokens per second. Throughput is a critical metric for evaluating the efficiency and performance of LLMs, especially in real-time or near-real-time applications where the speed of processing is crucial. Achieving high throughput implies that the model can handle large volumes of data quickly, making it suitable for tasks requiring rapid language processing, such as live chatbots, real-time translation, or speech recognition systems. This value will be measured on a smartphone with 12GB DRAM.

* <b>Parameter count:</b> Submissions should also include the model size, expressed as the parameter count, to represent the model’s dimensions. This metric is used for information only, not for ranking.

# Baseline, code, and materials provided

<p style='text-align: justify;'>
The “starting kit” will be released to provide a starting point for people who are interested in our challenge before June 25th, 2024. This starting kit will provide detailed clarifications on what a submission looks like exactly, and how it will be evaluated and submitted. This starting kit will include an end-to-end submission flow, exemplified with a simple baseline:
 </p>

* Loading a large language model choosing from Phi-2, Llama3-8B, or Qwen-7B.
* Performing the basic L1 norm structured pruning on this model so that the compressed model can fit the smartphone.
* Evaluating the pruned model on the OpenCompass benchmark. We will provide an easy-to-tun pipeline for participants to evaluate their model on the subset of the OpenCompass benchmark. 
* Deploying the resulting model on a smartphone platform and measuring its throughput. We will provide a tool that can help participants easily deploy their LLMs on the smartphone platform and measure throughput.

# Dataset

<p style='text-align: justify;'>
This competition will not evaluate submissions based on the analysis of data. Our competition features two tracks: (1) post-training LLM compression for edge devices; and (2) training edge LLMs from scratch. We will allow participants to use and only use the C4 dataset and (Chinese) Alpaca for both tracks. The C4 dataset is a colossal, cleaned version of Common Crawl’s web crawl corpus, which is mainly intended to pre-train language models and word representations. Language models like MPT-7B and T5 are pre-trained with the C4 dataset. C4 is a large enough dataset that can make the competition interesting and draw conclusive and statistically significant results. 

* The C4 dataset is public and can be accessed through: [C4 dataset](https://huggingface.co/datasets/c4)
<br>
* The Chinese version of Alpaca can be accessed through: [Alphaca](https://huggingface.co/datasets/silk-road/alpaca-data-gpt4-chinese)
<br>
