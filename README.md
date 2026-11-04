# 📂 Input Data for Reproducibility

This repository contains the pre-generated scheduling instances used in our study:

> *Quality- and Load-Guided Path Selection and Scheduling in Wafer Fabrication under Queue Time Limits*

## 🔍 Dataset Description

The datasets in this repository correspond to the data generation and experimental setup described in Section 5.1 of our study.

We consider a semiconductor wafer fabrication environment with six processing stages and 5, 3, 7, 3, 5, and 7 eligible machines at the respective stages. All instances are synthetically generated for the computational evaluation of integrated path selection and scheduling under queue time limits.

The repository contains 120 scheduling instances. The instances cover three problem sizes, two processing-time settings, two QTL-value settings, and two QTL-coverage settings. Five instances are generated for each experimental condition.

The candidate processing paths used in this study were adopted from Kim et al. and are available in the [GAInS repository](https://github.com/ODM-Lab/GAInS).

## 📁 Contents

1. [N10 Collection](Dataset/N10_collection/)  
   Small instances with `N = 10` jobs.

2. [N30 Collection](Dataset/N30_collection/)  
   Medium instances with `N = 30` jobs.

3. [N50 Collection](Dataset/N50_collection/)  
   Large instances with `N = 50` jobs.

Each collection contains eight Excel workbooks, corresponding to all combinations of the two processing-time, QTL-value, and QTL-coverage settings. Each workbook contains five generated instances.

## 📝 Workbook Contents

Each workbook contains the following sheets:

- `Job_split`: product-type composition and generation seed for each instance.
- `QTL_length`: QTL windows and limit values by product type.
- `QTL_resolved`: QTL limits resolved for applicable stage transitions.
- `PT_A`, `PT_B`, and `PT_C`: processing times by machine for the three product types.
- `Checks`: data-validation results.
- `Setting`: data-generation settings and machine configuration.

## ⚠️ Notes

- All instances are synthetically generated for algorithm testing and performance evaluation.
- The file names follow the convention `PT*_Q*_C*_N*.xlsx`.
- The `PT3` file label denotes the wide processing-time setting, which is referred to as `PT2` in the manuscript.
- Candidate processing paths are not duplicated in this repository; please refer to the linked GAInS repository.

## 📄 Citation

Citation information will be added upon publication.
