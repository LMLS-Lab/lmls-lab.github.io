---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Evaluation of K-Means Data Clustering Algorithm on Intel Xeon Phi"
authors: "Sunwoo Lee, Wei-keng Liao, Ankit Agrawal, Nikos Hardavellas, Alok Choudhary"
venue: "BigData"
year: 2019
type: "conference"          # conference | journal | preprint | workshop
doi: "10.1109/BigData.2016.7840856"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{lee2016evaluation,
    title={Evaluation of K-means data clustering algorithm on Intel Xeon Phi},
    author={Lee, Sunwoo and Liao, Wei-keng and Agrawal, Ankit and Hardavellas, Nikos and Choudhary, Alok},
    booktitle={2016 IEEE International Conference on Big Data (Big Data)},
    pages={2251--2260},
    year={2016},
    organization={IEEE}
  }
---
This paper studies how to optimize K-means for Intel Xeon Phi's MIC architecture using compiler-intrinsic-based memory layouts, data padding for VPU-width alignment, and parallel reduction for better cache and thread/data-level parallelism, achieving up to 68.65%/56.14% speedups over auto-vectorization on aligned/unaligned datasets and up to 53.49% on large-scale parallel runs with high-dimensional data.
