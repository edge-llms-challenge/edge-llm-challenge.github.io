---
layout: default
---

# Motivation

<p style='text-align: justify;'>
The rapid advancements in artificial intelligence, particularly in the domain of Natural Language Processing (NLP) propelled by Large Language Models (LLMs), have highlighted the potential of these models in influencing modern modes of work and communication. Consequently, integrating LLMs into edge devices, including smartphones, IoT devices, and in-car systems, holds significant promise within contemporary computing ecosystems. However, the massive size of LLMs presents challenges for edge devices, which typically operate with constrained resources. For instance, deploying a modest 10B LLM can demand up to 20GB of main memory (DRAM), even after quantization, a capacity that surpasses the available memory in most commodity smartphones. For example, the HUAWAI P60 boasts an 8GB DRAM capacity, and the iPhone 15 offers a 6GB DRAM. Given that DRAM is shared among the operating system and other applications, mobile apps must not exceed 10% of the DRAM allocation. Additionally, the energy consumption of LLMs presents a big barrier, with a fully charged smartphone, boasting approximately 50 kJ of energy, capable of sustaining a 7B LLM conversation for less than 2 hours at a rate of 10 tokens per second. </p>

<p style='text-align: justify;'>
We aim to deploy LLMs on edge devices in resource-bounded scenarios and address the following major issues:</p>

1. <b>Vast amounts of memory requirements</b>: LLM inference typically requires a significant amount of memory, a major bottleneck for off-the-shelf smartphones. Even high-end smartphones with 8GB are not sufficient for a sophisticated LLM.
2. <b>Prohibitive energy consumption</b>: the significant energy consumption during LLM inference presents a challenge to the battery life of smartphones.
3. <b>Large performance loss</b>: state-of-the-art LLMs might require unusually high compression ratios to fit into the memory of edge devices. Such extremely high compression ratios will significantly challenge the efficacy of existing model compression techniques, where we usually see a substantial performance drop after certain high levels of compression ratios. Therefore, achieving such high compression ratios while maintaining reasonable performance is very challenging.
4. <b>Lack of offline functionality</b>: Most off-the-shelf LLMs necessitate internet connections, which limits their usage in remote areas or in situations where internet access may be intermittent.

<p style='text-align: justify;'>
This is a brand new competition, which focuses on compressing and deploying LLMs on edge devices such as smartphones to push the boundaries of what these edge-device LLMs can achieve in terms of performance, efficiency, and versatility. This challenge is unique and distinct from the conventional model compression due to several factors.
</p>

# Scope

<p style='text-align: justify;'>
This competition encourages researchers, practitioners, and industry professionals from a wide range of fields to participate if they are interested in co-designing systems, hardware, and algorithms to enable high-performing LLMs on edge devices, unlocking new possibilities for various industries and use cases. </p>

# Potential impact

<p style='text-align: justify;'>
This competition aims to generate impacts in science, economics, and society. Scientifically, it may inspire new algorithms and optimizations for LLMs on edge devices, encourage interdisciplinary research, and involve more university experts studying LLMs despite limited resources. Economically, it could reduce energy costs, save on network bandwidth, cloud fees, and data transmission expenses, thus improving affordability and accessibility of LLM applications. Socially, the competition may tackle issues like digital inclusion, privacy, and sustainability by developing solutions promoting accessibility, privacy via on-device processing, and lower carbon footprint due to reduced reliance on centralized cloud infrastructure. By leveraging edge computing and LLMs, competition solutions have the potential to drive positive social change, promote equity, and address the needs of underrepresented communities. </p>
