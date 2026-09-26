# Chapter 2: Literature Review

## 2.1 Taxonomy of Historical Log Parsing Frameworks
The evolution of automated log analysis tools over the past two decades can be categorized into three distinct technical eras: rule-based string matching, heuristic-based token parsing, and contemporary deep learning semantic mapping. Early security frameworks relied heavily on deterministic regular expression filters. While these systems achieved high operational throughput due to low computational complexity, they exhibited severe fragility when exposed to structural updates in system logs. A minor software update that altered an output format string would break the regular expression syntax, leading to high false-negative rates in production environments.

To address this rigidity, researchers introduced automated log parsers designed to group structural log shapes without human intervention. The most prominent baseline tools include:
* **SLCT (Simple Log Clustering Tool):** An early text-mining utility that uses frequent-itemset mining concepts to pass through log files and identify recurring patterns.
* **IPLoM (Iterative Partitioning Log Mining):** A heuristic framework that splits a log file into smaller, specialized sub-clusters based on structural attributes.
* **DRAIN:** A state-of-the-art heuristic approach that maps log structures using a fixed-depth parsing tree.

## 2.2 Comparative Evaluation Matrix of Extant Methodologies
| Methodology Era | Typical Frameworks | Primary Advantages | Critical Vulnerabilities & Bottlenecks |
| :--- | :--- | :--- | :--- |
| **Deterministic Rule Filtering** | Grep Pipelines, Snort Rules, Fixed RegEx | Near-instant processing; minimal RAM footprint. | Incapable of capturing novel threat patterns; high maintenance overhead. |
| **Heuristic Tree Parsing** | DRAIN, IPLoM, LogSig | High template extraction accuracy on rigid formats. | Fails on unstructured data; sensitive to fixed parameter constraints. |
| **Relational SIEM Systems** | Splunk Core, ELK Stack | Powerful global indexing; structured long-term storage. | Massive disk-write bottlenecks; expensive cluster hosting costs. |
| **Proposed Framework** | **TF-IDF + K-Means** | **Zero database overhead; autonomous outlier isolation.** | Requires dynamic allocation of memory (RAM) for spatial vector matrices. |
