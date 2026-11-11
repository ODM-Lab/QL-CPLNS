# Candidate Path Data

This directory contains the candidate processing paths and final mapped quality scores used by QL-CPLNS.

- `PHQ_path_1.csv`: product type A (425 paths)
- `PHQ_path_4.csv`: product type B (422 paths)
- `PHQ_path_3.csv`: product type C (434 paths)

`Step 1`--`Step 6` give the one-based machine indices along a processing path. `score` is the final mapped quality score used by QL-CPLNS. `Yield` and `Type` are retained source attributes and are not QL-CPLNS product-type labels.

The candidate paths were adopted from Kim et al. and can be matched to the GAInS repository by their stage-wise machine sequences.
