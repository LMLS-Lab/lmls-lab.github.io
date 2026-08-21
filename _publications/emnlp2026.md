---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
featured: true
title: "Locality-aware Redundancy Pruning for LLM Depth Compression"
authors: "Vincent-Daniel Yun, Youngrae Kim, Woosang Lim, Youngjin Heo, Minkyu Kim, Sunwoo Lee"
note: ""
venue: "EMNLP"
year: 2026
type: "conference"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2605.27786"                   # link to arXiv page, optional
bibtex: |
  @article{yun2026locality,
    title={Locality-Aware Redundancy Pruning for LLM Depth Compression},
    author={Yun, Vincent-Daniel and Kim, Youngrae and Lim, Woosang and Heo, YoungJin and Kim, Minkyu and Lee, Sunwoo},
    journal={arXiv preprint arXiv:2605.27786},
    year={2026}
  }
---
This paper proposes LoRP, a training-free, one-shot depth pruning framework for large language models. It uses a Representation Locality Score, derived from inter-layer hidden-state similarity, to cluster layers and allocate pruning based on residual intra-cluster redundancy. The proposed approach improves both perplexity and downstream task accuracy across diverse LLM families.
