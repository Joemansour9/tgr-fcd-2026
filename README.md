# TGR-FCD-2026 Audit Benchmark Dataset

This repository contains the raw experimental data for the study **"Optimizing Multi-Agent Systems for Financial Auditing using Token-to-Goal Ratio (TGR)"**. 

## Dataset Overview
The file `TGR_Paper_Data.csv` includes results from **1,500 individual runs** (500 per architectural pattern) conducted on the FCD-2026 Audit Benchmark.

## Column Descriptions
| Column | Description |
| :--- | :--- |
| `run_id` | Unique identifier for each trial within the 500-task set. |
| `architecture` | The agentic pattern used: **Hierarchical**, **SLM Gated**, or **Reviewer Pattern**. |
| `success_binary` | Binary indicator of task completion (1 = Success, 0 = Failure). All trials reported here achieved $S=1$. |
| `handoff_count` | Total number of inter-agent transfers recorded during the task execution ($H$ variable). |
| `total_tokens` | Aggregate input and output tokens ($T_{in} + T_{out}$) used to calculate the TGR. |
| `cost_usd` | The total operational cost of the run in USD, based on current model pricing. |

## Key Findings Supported
1. **Orchestration Tax:** The data demonstrates a **66% increase** in token consumption when moving from Hierarchical to Reviewer patterns.
2. **Cost Efficiency:** Shows the **94% reduction** in cost achieved by the SLM Gated Architect compared to high-reasoning baselines.
3. **Success Consistency:** Verified 100% success rate across all 500 financial audit tasks.
