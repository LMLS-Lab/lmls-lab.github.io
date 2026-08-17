---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
featured: false
title: "Asynchronous I/O Strategy for Large-scale Deep Learning Applications"
authors: "Sunwoo Lee, Qiao Kang, Kewei Wang, Jan Balewski, Alex Sim, Ankit Agrawal, Alok Choudhary, Peter Nugent, Kesheng Wu, Wei-keng Liao"
venue: "HiPC"
year: 2021
type: "conference"          # conference | journal | preprint | workshop
doi: "10.1109/HiPC53243.2021.00046"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{lee2021asynchronous,
    title={Asynchronous I/O strategy for large-scale deep learning applications},
    author={Lee, Sunwoo and Kang, Qiao and Wang, Kewei and Balewski, Jan and Sim, Alex and Agrawal, Ankit and Choudhary, Alok and Nugent, Peter and Wu, Kesheng and Liao, Wei-keng},
    booktitle={2021 IEEE 28th International Conference on High Performance Computing, Data, and Analytics (HiPC)},
    pages={322--331},
    year={2021},
    organization={IEEE}
  }
---
This paper proposes an asynchronous I/O strategy for large-scale deep learning training, in which a dedicated per-process I/O thread reads many training samples at once and overlaps I/O with computation via double-buffering, and shows on CosmoFlow and Neuron-Inverter that this significantly improves scaling performance without degrading regression accuracy.
