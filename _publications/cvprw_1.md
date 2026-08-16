---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "TimelyFL: Heterogeneity-aware Asynchronous Federated Learning with Adaptive Partial Training"
authors: "Tuo Zhang, Lei Gao, Sunwoo Lee, Mi Zhang, Salman Avestimehr"
venue: "Conference on Computer Vision and Pattern Recognition Workshop"
year: 2023
type: "workshop"          # conference | journal | preprint | workshop
doi: "10.1109/CVPRW59228.2023.00535"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{zhang2023timelyfl,
    title={Timelyfl: Heterogeneity-aware asynchronous federated learning with adaptive partial training},
    author={Zhang, Tuo and Gao, Lei and Lee, Sunwoo and Zhang, Mi and Avestimehr, Salman},
    booktitle={2023 IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW)},
    pages={5064--5073},
    year={2023},
    organization={IEEE}
  }
---
This work proposes TimelyFL, a heterogeneity-aware asynchronous federated learning framework that adaptively adjusts each client's local training workload based on real-time resource capacity to reduce staleness and boost participation, improving participation rate by 21.13%, convergence efficiency by 1.28x to 2.89x, and test accuracy by 6.25% over the state-of-the-art FedBuff.
