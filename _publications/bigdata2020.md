---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Communication-Efficient Local Stochastic Gradient Descent for Scalable Deep Learning"
authors: "Sunwoo Lee, Qiao Kang, Ankit Agrawal, Alok Choudhary, Wei-keng Liao"
venue: "BigData"
year: 2020
type: "conference"          # conference | journal | preprint | workshop
doi: "10.1109/BigData50022.2020.9378178"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{lee2020communication,
    title={Communication-efficient local stochastic gradient descent for scalable deep learning},
    author={Lee, Sunwoo and Kang, Qiao and Agrawal, Ankit and Choudhary, Alok and Liao, Wei-keng},
    booktitle={2020 IEEE International Conference on Big Data (Big Data)},
    pages={718--727},
    year={2020},
    organization={IEEE}
  }
---
This paper proposes a hierarchical local-SGD training strategy that groups workers into multiple data-parallel subgroups with periodic cross-group model averaging (using a cheaper-than-allreduce averaging scheme), plus a practical metric for choosing the largest worker count that avoids significant accuracy loss, and shows experimentally that this achieves markedly better scalability than synchronous SGD while retaining comparable accuracy.
