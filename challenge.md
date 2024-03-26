---
layout: default
---

# Baselines, code, and material

<p style='text-align: justify;'>
The “starting kit” will be released to provide a starting point for people who are interested in our challenge before May 5th, 2024. This starting kit will provide detailed clarifications on what a submission looks like exactly, and how it will be evaluated and submitted. This starting kit will include an end-to-end submission flow, exemplified with a simple baseline:
 </p>

* Loading a large language model choosing from Phi-2, Llama 2 7B, or Mamba 7B.
* Performing the basic L1 norm structured pruning on this model so that the compressed model can fit the smartphone.
* Evaluating the pruned model on the OpenCompass benchmark. We will provide an easy-to- tun pipeline for participants to evaluate their model on the subset of the lm-evaluation-harness benchmark.
* Deploying the resulting model on a Huawei Meta 60 and measuring its TPOT. We will provide a tool that can help participants easily deploy their LLMs on Huawei smartphones and measure TPOP.
* Make a submission on the Leaderboard to see how we fare up against other competitors.

# Dataset

<p style='text-align: justify;'>
This competition will not evaluate submissions based on the analysis of data. Our competition features two tracks: (1) post-training LLM compression for edge devices; and (2) training edge LLMs from scratch. For both tracks, we will allow the participants to use and only use the C4 dataset [13]. The C4 dataset is a colossal, cleaned version of Common Crawl’s web crawl corpus, which is mainly intended to pre-train language models and word representations. Language models like MPT-7B and T5 are pre-trained with C4 dataset. C4 is a large enough dataset that can make the competition interesting and draw conclusive and statistically significant results.  </p> 
* The C4 dataset is public and can be accessed through: [HuggingFace](https://huggingface.co/datasets/c4)
<br>

# Metrics

<p style='text-align: justify;'>

To comprehensively evaluate submissions, we employ a set of rigorously curated metrics, which include:

* Averaged accuracy: One of our primary scoring metrics is the averaged accuracy on a subset of the OpenCompass benchmark. This metric assesses the language capacity of the submission across seven fundamental dimensions.

* Time Per Output Token (TPOT): Another critical performance metric is the average time for submitted models to generate each output token. This measurement is essential for evaluating real-time interaction between users and smartphones. TPOT can be calculated as the overall time taken by the model to generate the full response divided by the number of generated tokens. This value is expected to be measured on a Huawei Meta 60 with 12GB DRAM.

* Parameter count: Submissions should also include the model size, expressed as the parameter count, to indicate the model’s size.

</p>


