# Design And Analysis of Cache Architecture

**📌 Project Overview**

The core of this project is to design and evaluate optimal cache configurations for various memory access patterns. By manipulating hardware parameters such as Cache Size, Associativity, and Block Size, the project explores how different architectures handle specific computational workloads.

**🔍 Workload Patterns & Traces**

The analysis covers five distinct memory traces representing common software behaviors:

Trace 1 (Temporal Locality): A repeating loop of specific addresses.

Trace 2 (Streaming/Spatial): Sequential data access with fixed strides.

Trace 3 (Random Access): Sparse, non-linear memory references.

Trace 4 (Strided Access): Large-gap sequential processing.

Trace 5 (Conflict Hazard): Interleaved buffer processing (Ping-Pong effect).

**🛠 Experimental Methodology**

Using a Cache Simulator, several experiments were conducted:

Step A: Testing Block Size impact on spatial locality.

Step B: Evaluating Associativity to mitigate conflict misses (specifically resolving the 50% hit-rate bottleneck in Trace 5).

Step C: Identifying the "Working Set" through cache capacity scaling.

Step D: Comparing replacement policies (LRU, FIFO, Random).

**💡 Key Findings: Human vs. AI Insight**

A unique aspect of this project is the comparison between manual architectural analysis and AI-driven (GPT-4/Gemini) recommendations:

The Thrashing Proof: While AI predicted "thrashing" in Trace 5, my simulation quantified it—showing exactly how a move to 2-Way Associativity restored performance from 50% to 83.3%.

Engineering Reality: AI often suggests high associativity for everything. My analysis proves that for specific workloads, Direct-Mapped configurations are more efficient due to lower complexity and hit time.

**📂 Repository Contents**

pdf: Comprehensive analysis and experimental results.

pptx: Presentation of the Analysis.

**Author**
Yusuf Taha ÖNCÜ
