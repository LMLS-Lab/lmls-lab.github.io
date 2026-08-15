---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Partial Model Averaging in Federated Learning: Performance Guarantees and Benefits"
authors: "Sunwoo Lee, Anit Sahu, Chaoyang He, Salman Avestimehr"
venue: "Neurocomputing"
year: 2023
type: "journal"          # conference | journal | preprint | workshop
doi: "10.1016/j.neucom.2023.126647"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @article{lee2023partial,
    title={Partial model averaging in federated learning: Performance guarantees and benefits},
    author={Lee, Sunwoo and Sahu, Anit Kumar and He, Chaoyang and Avestimehr, Salman},
    journal={Neurocomputing},
    volume={556},
    pages={126647},
    year={2023},
    publisher={Elsevier}
  }
---
This work proposes a partial model averaging framework for Federated Learning that reduces the model discrepancy caused by periodic full averaging in FedAvg-style local SGD, achieving up to 2.2% higher accuracy than periodic full averaging on CIFAR-10/100 and FEMNIST with 128 clients under a fixed training budget.
