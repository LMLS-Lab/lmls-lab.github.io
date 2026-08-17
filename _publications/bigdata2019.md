---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Improving Scalability of Parallel CNN Training by Adjusting Mini-batch Size at Run-time"
authors: "Sunwoo Lee, Qiao Kang, Sandeep Madireddy, Prasanna Balaprakash, Ankit Agrawal, Alok Choudhary, Richard Archibald, Wei-keng Liao"
venue: "BigData"
year: 2019
type: "conference"          # conference | journal | preprint | workshop
doi: "10.1109/BigData47090.2019.9006550"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{lee2019improving,
    title={Improving scalability of parallel CNN training by adjusting mini-batch size at run-time},
    author={Lee, Sunwoo and Kang, Qiao and Madireddy, Sandeep and Balaprakash, Prasanna and Agrawal, Ankit and Choudhary, Alok and Archibald, Richard and Liao, Wei-keng},
    booktitle={2019 IEEE international conference on big data (big data)},
    pages={830--839},
    year={2019},
    organization={IEEE}
  }
---
This paper proposes a parallel CNN training strategy that progressively grows the mini-batch size and learning rate during training, and shows across various image regression and classification models and datasets that this improves scalability while keeping accuracy close to that of fixed small-batch training.
