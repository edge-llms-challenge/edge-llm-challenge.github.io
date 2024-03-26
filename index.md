---
layout: default
---

<p style='text-align: justify;'>
The rapid advancements in artificial intelligence, particularly in the domain of natural language processing (NLP) propelled by Large Language Models (LLMs), have underscored the transformative potential of these colossal models in shaping modern modes of work and communication. Conse- quently, the prospect of integrating the expansive knowledge capacity of LLMs into edge devices, including smartphones, IoT devices, and in-car systems, holds significant promise within contempo- rary computing ecosystems. However, the massive size of LLMs presents formidable challenges for edge devices, which typically operate with constrained resources. For instance, deploying a modest 10B LLM can demand up to 20GB of main memory (DRAM), even after employing INT8 quantization techniques, a capacity that surpasses the available memory in most commodity smartphones [6]. For example, the HUAWAI P60 boasts an 8GB DRAM capacity, and the iPhone 15 offers a 6GB DRAM. Given that DRAM is shared among the operating system and other applications, mobile apps must not exceed 10% of the DRAM allocation. Additionally, the energy consumption of LLMs presents a big barrier, with a fully charged smartphone, boasting approximately 50 kJ of energy, capable of sustaining a 7B LLM conversation for less than 2 hours at a rate of 10 tokens per second. </p>

<p style='text-align: justify;'>
Our goal is to to push the boundaries of what these powerful LLMs can achieve on edge devices in terms of performance, efficiency, and versatility. Specifically, our goal is to deploy LLMs on edge devices in resource-bounded scenarios and address the following major issues:</p>

1. Vast amounts of memory requirements: LLM inference typically requires a significant amount of memory, a major bottleneck for off-the-shelf smartphones. Even high-end smartphones with 8GB are not sufficient for a sophisticated LLM.
2. Prohibitive energy consumption: Moreover, the significant energy consumption during LLM inference presents a formidable challenge to the battery life of smartphones.
3. Large performance loss: SOTA LLMs might require unusually high compression ratios to fit into the memory of edge devices. Such extremely high compression ratios will signifi- cantly challenge the efficacy of existing model compression techniques, where we usually see a substantial performance drop after certain high levels of compression ratios. Therefore, achieving such high compression ratios while maintaining reasonable performance is very challenging.
4. Lack of offline functionality: Most off-the-shelf LLMs necessitate internet connections, which limits their usage in remote areas or in situations where internet access may be intermittent.

<p style='text-align: justify;'>
This is a brand new competition, which focuses on compressing and deploying LLMs on edge devices such as smartphones to push the boundaries of what these edge-device LLMs can achieve in terms of performance, efficiency, and versatility. This challenge is unique and distinct from the conventional model compression due to several factors.
</p>