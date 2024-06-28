---
layout: default
---
# Tracks

<p style='text-align: justify;'>
<b> 1. Compression Challenge:</b> teams are tasked with developing their own compression methods to compress three pre-trained LLMs individually: Phi-2, Llama-3-8B, and Qwen-7B. Each model submitted must be capable of running on a smartphone device with 12 GB DRAM. Each model will be evaluated on a subset of the OpenCompass benchmark, which comprehensively assesses LLMs across multiple fundamental dimensions. For each task, the final submission score will be determined by calculating the average score of the three models involved. </p>

<p style='text-align: justify;'>
<b> 2. Training from Scratch Challenge:</b> teams are challenged to train language models from scratch without utilizing any pre-trained LLMs. There are no constraints on model architectures, training procedures, or duration, as long as the final models can run on a smartphone device with 12GB memory. Participants are free to design their architectures or utilize existing LLM architectures for this task. However, there is a restriction on the training data: only the C4 and Alpaca datasets are permitted for training and fine-tuning.</p>

<p style='text-align: justify;'>
<b>Please note that quantization methods are not allowed</b> since 8-bit or 4-bit quantization for LLMs is a well-established technique. Participants must submit models in FP16 or FP32 format.
</p>

# Submission
<p style='text-align: justify;'>
To participate in the challenge, you need to submit your entry by filling out a form. The form requires you to provide a link to your GitHub repository where your code is hosted. Additionally, you should <b> add our repository <i> edge-llms-challenge</i> as a collaborator on your repository</b>. This will allow us to access and review your code.</p>

Here are the steps to complete the submission:

1. Create a GitHub repository for your project.
2. Add your code to the repository, including the source code for pre-training or compression, model definition files, configuration files, and a CSV file containing evaluated results that are evaluated locally.
3. A .txt file containing Google Drive links to download model checkpoints and the compiled model for building Android APP. 
4. Fill out the [submission form](https://forms.gle/S367FfxUDcjSKz1Q9) with the required information, including the link to your GitHub repository.
5. Add the edge-llm-challenge repository as a collaborator on your repository and meanwhile make your repository as private.
6. Submit the form to complete your entry.

Please, refer to this [link](https://github.com/TianjinYellow/EdgeDeviceLLMCompetition-Starting-Kit?tab=readme-ov-file#submission-requirements) for more details about the submission.

By following these steps, you will have successfully submitted your entry for the challenge. Good luck!

# Evaluation

The evaluation process in our competition will include two stages. 

<p style='text-align: justify;'> <b>The first stage:</b> the submitted models will be evaluated on a diverse subset of the OpenCompass benchmark, including CSQA, BIG-Bench Hard, GSM8K, LongBench, HumanEval, TruthfulQA, CHID, along with a set of secret holdout tasks to avoid overfitting. A self-contained code base will be provided to facilitate participants in easily evaluating their models on seven diverse tasks via the OpenCompass benchmark. </p>

* <p style='text-align: justify;'> Each submission will be ranked individually for each task, with the top 10 submissions with the highest score per task receiving scores from 10 to 1. The score of each task is calculated as the average score of the three models for the first track. For the second track, the score is the score of the submitted model. </p>
    
* <p style='text-align: justify;'> We will measure the models' throughput on a smartphone platform provided by the sponsor. Submissions will be ranked based on throughput. To emphasize the importance of inference speed, the score for the throughput task will be <b>doubled</b>, ranging from 20 to 2 for the top 10 submissions. To assist participants in improving the speed of their models, we will provide an easy-to-run pipeline to measure throughput on a GPU, where the throughput values are roughly scaled to those on the smartphone platform.</p>
    
* <p style='text-align: justify;'> We will measure the inference memory usage of all models. Submissions with models that exceed 12GB of memory usage for inference will be disqualified.</p>
    
* <p style='text-align: justify;'> The final rank of submissions will be determined by the sum of scores across all evaluation tasks including seven diverse tasks as shown in the Table below (100 scores in total), maximum 70 scores, one secret holdout task (maximum 10 scores), and the throughput measurement (maximum 20 scores). </p>

<p style='text-align: justify;'> The top 15 teams with the highest scores will be displayed on the leaderboard. Participants are required to submit their source codes, evaluation log files, and models to the organizers (Check <i>Submission</i> section for details). </p>

<p style='text-align: justify;'>Participating teams are encouraged to submit their models for a preliminary review on the 25th of August to identify potential bugs and format issues, ensuring that the final submissions are in the correct format. Each team can make three submissions to each track after the deadline of the preliminary review. The best-performing model will be used to rank the team on the leaderboard and selected for the final model evaluation.</p>

<p style='text-align: justify;'> <b>The second stage:</b>  After the competition is closed on October 25th, 2024, we will contact the top 3 teams with the highest scores in both tracks, requesting that they submit all necessary code and data to reproduce their results. We will then replicate their entire process, to ensure it is fully repeatable and the final model can be run on a smartphone with 12 GB RAM with the same results. If the top-scoring model cannot be reproduced under these imposed conditions or can not fit the smartphone, we will move on to consider the next highest-scoring submission in the category, until a reproducible and high-performing submission is selected. </p>

<p style='text-align: justify;'> Our evaluation will leverage an extensive array of rigorously curated datasets across multiple fundamental dimensions: language comprehension, knowledge precision, logical deduction, mathematical problem-solving, programming proficiency, extended text analysis, and intelligent agent engagement. Details of the evaluation tasks we chose are shown below: </p>

## Evaluation datasets

<table class="foo">
    <tr>
        <td width="50%"><b>Dataset</b></td>
        <td width="50%"><b>Dimension</b></td>
        <td width="100%"><b>Source</b></td>
    </tr>
    <tr>
        <td width="50%">CommonsenseQA</td>
        <td width="50%">Knowledge</td>
         <td width="100%"><a href="https://www.tau-nlp.sites.tau.ac.il/commonsenseqa">https://www.tau-nlp.sites.tau.ac.il/commonsenseqa</a></td>
    </tr>
    <tr>
        <td width="50%">BIG-Bench Hard</td>
        <td width="50%">Reasoning</td>
         <td width="100%"><a href="https://github.com/suzgunmirac/BIG-Bench-Hard">https://github.com/suzgunmirac/BIG-Bench-Hard</a></td>
    </tr>
    <tr>
        <td width="50%">GSM8K</td>
        <td width="50%">Math</td>
         <td width="100%"><a href="https://github.com/openai/grade-school-math">https://github.com/openai/grade-school-math</a></td>
    </tr>
    <tr>
        <td width="50%">LongBench</td>
        <td width="50%">Long-Context</td>
         <td width="100%"><a href="https://github.com/THUDM/LongBench">https://github.com/THUDM/LongBench</a></td>
    </tr>
    <tr>
        <td width="50%">HumanEval</td>
        <td width="50%">Programming</td>
        <td width="100%"><a href="https://github.com/openai/human-eval">https://github.com/openai/human-eval</a></td>
    </tr>
    <tr>
        <td width="50%">TruthfulQA</td>
        <td width="50%">Knowledge</td>
         <td width="100%"><a href="https://github.com/sylinrl/TruthfulQA">https://github.com/sylinrl/TruthfulQA</a></td>
    </tr>
    <tr>
        <td width="50%">CHID</td>
        <td width="50%">Language</td>
         <td width="100%"><a href="https://github.com/chujiezheng/ChID-Dataset">https://github.com/chujiezheng/ChID-Dataset</a></td>
    </tr>
</table>


# Metrics

<p style='text-align: justify;'>

To comprehensively evaluate submissions, we will employ a set of rigorously curated metrics, which include:
</p>

* <b>Performance Score:</b> One of our primary scoring metrics is the performance score on the selected evaluation task. Each submission will be ranked individually for each task based on the performance score, with the top 10 submissions per task receiving scores from 10 to 1. The final score of the submission is calculated as the sum across all evaluation tasks.
  
* <b>Memory Requirement:</b> The memory footprint during inference is a crucial metric for real-life edge devices. To qualify, the peak memory usage of all models must be less than 12GB.

* <b>Throughput:</b> The throughput of an LLM typically refers to the rate at which the model can process input data and generate output tokens. It is often measured in terms of tokens per second. Throughput is a critical metric for evaluating the efficiency and performance of LLMs, especially in real-time or near-real-time applications where the speed of processing is crucial. Achieving high throughput implies that the model can handle large volumes of data quickly, making it suitable for tasks requiring rapid language processing, such as live chatbots, real-time translation, or speech recognition systems. This value will be measured on a smartphone with 12GB DRAM.

* <b>Parameter count:</b> Submissions should also include the model size, expressed as the parameter count, to represent the model’s dimensions. This metric is used for information only, not for ranking.

# Baseline, code, and materials

<p style='text-align: justify;'>
The “starting kit” will be released to provide a starting point for people who are interested in our challenge before June 25th, 2024. This starting kit will provide detailed clarifications on what a submission looks like exactly, and how it will be evaluated and submitted. This starting kit will include an end-to-end submission flow, exemplified with a simple baseline:
 </p>

* Loading a large language model choosing from <b>Phi-2, Llama3-8B, or Qwen-7B</b>.
* Evaluating the pruned model on the OpenCompass benchmark. We will provide an easy-to-run pipeline for participants to evaluate their model on the subset of the OpenCompass benchmark. We will also provide a tool for measuring the throughput and GPU memory usage of a LLM.
* Compile a model into a binary model library that can be run on android devices. We will provide a tool that can help participants easily deploy their LLMs on the smartphone platform.

# Training datasets

<p style='text-align: justify;'>
This competition will not evaluate submissions based on the analysis of data. Our competition features two tracks: (1) post-training LLM compression for edge devices; and (2) training edge LLMs from scratch. We will allow participants to use and only use the C4 dataset and (Chinese) Alpaca for both tracks. The C4 dataset is a colossal, cleaned version of Common Crawl’s web crawl corpus, which is mainly intended to pre-train language models and word representations. Language models like MPT-7B and T5 are pre-trained with the C4 dataset. C4 is a large enough dataset that can make the competition interesting and draw conclusive and statistically significant results.  </p>

* The <b>C4 dataset</b> can be accessed through: [C4 dataset](https://huggingface.co/datasets/c4).

* The Chinese version of <b>Alpaca</b> can be accessed through: [Alpaca dataset](https://huggingface.co/datasets/silk-road/alpaca-data-gpt4-chinese).
