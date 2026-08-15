---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "SSFL: Tackling Label Deficiency in Federated Learning via Personalized Self-Supervision"
authors: "Chaoyang He, Zhengyu Yang, Erum Mushtaq, Sunwoo Lee, Mahdi Soltanolkotabi, Salman Avestimehr"
venue: "AAAI Workshop"
note: "Best Paper Award"
year: 2022
type: "workshop"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2110.02470"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @article{he2021ssfl,
    title={Ssfl: Tackling label deficiency in federated learning via personalized self-supervision},
    author={He, Chaoyang and Yang, Zhengyu and Mushtaq, Erum and Lee, Sunwoo and Soltanolkotabi, Mahdi and Avestimehr, Salman},
    journal={arXiv preprint arXiv:2110.02470},
    year={2021}
  }
---
This work proposes SSFL, a unified self-supervised and personalized Federated Learning framework that extends FedAvg to work with self-supervised methods like SimSiam and introduces Per-SSFL, a personalization algorithm that regularizes the distance between local and global representations, showing that self-supervised FL closes most of the accuracy gap with supervised FL while representation-regularized personalization outperforms other variants.
