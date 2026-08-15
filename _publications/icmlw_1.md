---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Ghosted Layers: Unconstrained Activation Alignment for Recovering Layer-pruned LLMs"
authors: "Vincent-Daniel Yun, Junhyuk Jo, Sai Praneeth Karimireddy, Sunwoo Lee"
venue: "ICML Workshop"
year: 2026
type: "workshop"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2605.15491"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @article{yun2026ghosted,
    title={Ghosted Layers: Unconstrained Activation Alignment for Recovering Layer-Pruned LLMs},
    author={Yun, Vincent-Daniel and Jo, Junhyuk and Karimireddy, Sai Praneeth and Lee, Sunwoo},
    journal={arXiv preprint arXiv:2605.15491},
    year={2026}
  }
---
This work proposes Ghosted Layers, a training-free recovery module for layer-pruned Transformer LLMs that derives a closed-form optimal linear operator from a small calibration set to correct the boundary activation mismatch introduced by pruning, achieving the unconstrained optimum of the alignment objective and consistently improving accuracy and perplexity over prior training-free baselines while preserving pruning's efficiency gains.
