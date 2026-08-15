---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Federated Learning of Large Model at the Edge via Principal Sub-Model Training"
authors: "Yue Niu, Saurav Prakash, Souvik Kundu, Sunwoo Lee, Salman Avestimehr"
venue: "NeurIPS Workshop"
year: 2022
type: "workshop"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2208.13141"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @article{niu2022federated,
    title={Federated learning of large models at the edge via principal sub-model training},
    author={Niu, Yue and Prakash, Saurav and Kundu, Souvik and Lee, Sunwoo and Avestimehr, Salman},
    journal={arXiv preprint arXiv:2208.13141},
    year={2022}
  }
---
This work proposes PriSM, a principal sub-model training methodology for cross-device Federated Learning that assigns each resource-constrained client a small, importance-sampled low-rank sub-model derived via principal kernel analysis, letting clients collaboratively train a full large model without any client training it fully or sharing intermediate information, while together achieving near-full coverage of the model's principal kernels.
