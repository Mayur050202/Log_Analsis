# Chapter 4: Results & Performance Validation

## 4.1 System Benchmarking Indicators
* **Initial Normal Baseline Log Load:** 4,004 lines processed in under 0.15 seconds.
* **Expanded Post-Attack Log Fabric:** Expanded dynamically to 4,006 lines without database indexing interruptions.
* **Total Anomaly Isolation Count:** 6 true structural outliers captured.
* **Environmental Threat Index:** 0.15% Anomaly Rate.
* **System Accuracy Metric Resolution:** 100.00% F1-Score achieved.

## 4.2 Malicious Endpoint Threat Ledger
| Index | Isolated Attacker IP Address | Calculated Risk Priority | Operational Protocol Action |
| :--- | :--- | :--- | :--- |
| **0** | `45.22.11.9` | **CRITICAL** | Isolate Traces / Drop Active Session |
| **1** | `185.220.101.5` | **CRITICAL** | Isolate Traces / Drop Active Session |
| **2** | `91.241.19.44` | **CRITICAL** | Isolate Traces / Drop Active Session |
| **3** | `103.25.41.2` | **CRITICAL** | Isolate Traces / Drop Active Session |
| **4** | `198.51.100.77` | **CRITICAL** | Drop Session (DDoS Injection) |
| **5** | `203.0.113.55` | **CRITICAL** | Drop Session (SQLi Injection) |

## 4.3 Classification Metric Mathematics
$$\text{Precision} = \frac{6}{6 + 0} = 1.00 \quad (100.00\%)$$
$$\text{Recall} = \frac{6}{6 + 0} = 1.00 \quad (100.00\%)$$
$$\text{F1-Score} = 2 \times \frac{1.00 \times 1.00}{1.00 + 1.00} = 1.00 \quad (100.00\%)$$
