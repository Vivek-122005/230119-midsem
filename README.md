# Advanced ML Mid-Sem Part B Submission

This repository contains my Part B work for **Advanced Machine Learning (Rishihood University)**.

## Student Details

- Name: **Vivek Vishnoi**
- Enrollment / Roll Number: **230119**
- Course: **Advanced Machine Learning**
- Assessment: **Mid-Semester Examination**

## Paper and Scope

- Selected paper: **Early Prediction on Time Series: A Nearest Neighbor Approach** (IJCAI 2009)
- Reproduction focus: prefix-based early classification behavior using 1NN on a public benchmark
- Dataset used: **FordA** (UCR-style TSV files in `partB/data/`)

## Part A and Part B Overview

- `partA/` contains Part A work: paper selection, paper understanding notes, and LLM disclosure for Part A.
- `partB/` contains Part B work: reproduction, ablations, failure mode analysis, report, and Part B LLM disclosures.
- The selected paper for both parts is the same: **Early Prediction on Time Series: A Nearest Neighbor Approach**.

## Guideline-Aligned Protocol

- FordA is kept at original full sequence length (**500**).
- Early prediction is evaluated by prefix slicing of the same 500-length series.
- A 100-timestep view is treated as a **20% prefix**, not as a truncated replacement dataset.
- Task 3.1 uses **exactly two independent component ablations** (as required).

## Repository Layout

- `partB/task_1_1.ipynb`, `partB/task_1_2.ipynb`, `partB/task_1_3.ipynb`  
  Question 1: paper understanding (markdown-only, no code)
- `partB/task_2_1.ipynb`, `partB/task_2_2.ipynb`, `partB/task_2_3.ipynb`  
  Question 2: dataset setup, reproduction, result comparison, reproducibility checklist
- `partB/task_3_1.ipynb`, `partB/task_3_2.ipynb`  
  Question 3: two-component ablation + failure mode analysis
- `partB/report.pdf`  
  Question 4.1 final report (IEEE style)
- `partB/llm_task_*.json`  
  Question 4.2 LLM disclosure files (10 files)
- `partB/data/FordA_TRAIN.tsv`, `partB/data/FordA_TEST.tsv`  
  dataset files
- `partB/results/`  
  saved plots and CSV outputs referenced by notebooks/report

## Environment Setup

From repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r partB/requirements.txt
```

## Notebook Execution Order

Open Jupyter from repository root:

```bash
jupyter lab
```

Run all notebooks in this sequence:

1. `partB/task_1_1.ipynb`
2. `partB/task_1_2.ipynb`
3. `partB/task_1_3.ipynb`
4. `partB/task_2_1.ipynb`
5. `partB/task_2_2.ipynb`
6. `partB/task_2_3.ipynb`
7. `partB/task_3_1.ipynb`
8. `partB/task_3_2.ipynb`

## Key Outputs

- `partB/results/task_2_2_prefix_accuracy.csv`
- `partB/results/task_2_2_accuracy_vs_prefix.png`
- `partB/results/task_2_3_stability_plot.png`
- `partB/results/task_3_1_ablation1_summary.csv`
- `partB/results/task_3_1_metric_comparison.csv`
- `partB/results/task_3_1_ablation1.png`
- `partB/results/task_3_1_ablation2.png`
- `partB/results/task_3_2_failure_accuracy.csv`
- `partB/results/task_3_2_failure_curve.png`

## Reproducibility Notes

- Random seeds are fixed in code notebooks.
- Experiments are CPU-only and use classical Python ML libraries.
- Paths and outputs are explicitly documented in notebook markdown cells.
- Task 2.3 contains the final reproducibility checklist required by guideline.
