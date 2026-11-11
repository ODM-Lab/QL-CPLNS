# 📂 Input Data for Reproducibility

This repository contains the pre-generated scheduling instances used in our study:

> *Quality- and Load-Guided Path Selection and Scheduling in Wafer Fabrication under Queue Time Limits*

## 🔍 Dataset Description

The datasets in this repository correspond to the data generation and experimental setup described in Section 5.1 of our study.

We consider a semiconductor wafer fabrication environment with six processing stages and 5, 3, 7, 3, 5, and 7 machines at the respective stages. All instances are synthetically generated for the computational evaluation of integrated path selection and scheduling under queue time limits.

The repository contains 120 scheduling instances. The instances cover three problem sizes, two processing-time settings, two QTL-value settings, and two QTL-coverage settings. Five instances are generated for each experimental condition.

The candidate processing paths used in this study were adopted from Kim et al. and remain available in the [GAInS repository](https://github.com/ODM-Lab/GAInS). The corresponding paths and mapped quality scores used by QL-CPLNS are provided in `Dataset/paths`.

## 📁 Contents

1. [N10 Collection](Dataset/instances/N10/)  
   Small instances with `N = 10` jobs.

2. [N30 Collection](Dataset/instances/N30/)  
   Medium instances with `N = 30` jobs.

3. [N50 Collection](Dataset/instances/N50/)<br>
   Large instances with `N = 50` jobs.

4. [Candidate Path Data](Dataset/paths/)  
   Candidate processing paths and mapped quality scores used by QL-CPLNS.

Each collection contains eight Excel workbooks, corresponding to all combinations of the two processing-time, QTL-value, and QTL-coverage settings. Each workbook contains five generated instances.

## 📝 Workbook Contents

Each workbook contains five generated instances and the following sheets.

### `Job_split`

| Column | Description |
|---|---|
| `instance_id` | Identifier of the generated instance. |
| `seed` | Random seed used to generate the instance. |
| `N_total` | Total number of jobs. |
| `n_A`, `n_B`, `n_C` | Numbers of jobs of product types A, B, and C, respectively. |

### `QTL_length`

| Column | Description |
|---|---|
| `instance_id` | Identifier of the generated instance. |
| `qtl_step_windows_A`, `qtl_values_A` | Stage window and corresponding QTL values for product type A. |
| `qtl_step_windows_B`, `qtl_values_B` | Stage window and corresponding QTL values for product type B. |
| `qtl_step_windows_C`, `qtl_values_C` | Stage window and corresponding QTL values for product type C. |

### `QTL_resolved`

| Column | Description |
|---|---|
| `instance_id` | Identifier of the generated instance. |
| `type` | Product type to which the QTL applies. |
| `r` | Index of the preceding stage in a QTL-constrained transition. |
| `L_r` | Maximum allowable waiting time between completion at stage `r` and the start at stage `r+1`. |

### `PT_A`, `PT_B`, and `PT_C`

These sheets contain processing times for product types A, B, and C, respectively.

| Column | Description |
|---|---|
| `instance_id` | Identifier of the generated instance. |
| `PT_i1k1`, ..., `PT_i6k7` | Processing time of machine `k` at stage `i` for the corresponding product type. The number after `i` identifies the stage, and the number after `k` identifies the machine. |

## 🧭 Candidate Path Data

The `Dataset/paths` directory contains the candidate processing paths and final mapped quality scores used by QL-CPLNS.

- `candidate_paths_A.csv`: product type A (425 paths)
- `candidate_paths_B.csv`: product type B (422 paths)
- `candidate_paths_C.csv`: product type C (434 paths)

`Step 1`--`Step 6` give the one-based machine indices along a processing path. `score` is the final mapped quality score used by QL-CPLNS. `Yield` is retained as a source attribute and is not used by QL-CPLNS.

The stage-wise machine sequences can be matched to those of the candidate paths in the GAInS repository.

## ⚠️ Notes

- All instances are synthetically generated for algorithm testing and performance evaluation.
- The file names follow the convention `PT{1,2}_Q{1,2}_C{1,2}_N{10,30,50}.xlsx`.

## 📄 Citation

Citation information will be added upon publication.
