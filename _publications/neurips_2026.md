---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
featured: true
title: "Ghosted Layers: Unconstrained Activation Alignment for Recovering Layer-Pruned LLMs"
authors: "Daniel Yun, Junhyuk Jo, Sai Praneeth Karimireddy, Sunwoo Lee"
note: ""
venue: "NeurIPS"
year: 2026
type: "conference"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2605.15491"                   # link to arXiv page, optional
bibtex: |
  @article{yun2026ghosted,
    title={Ghosted Layers: Unconstrained Activation Alignment for Recovering Layer-Pruned LLMs},
    author={Yun, Vincent-Daniel and Jo, Junhyuk and Karimireddy, Sai Praneeth and Lee, Sunwoo},
    journal={arXiv preprint arXiv:2605.15491},
    year={2026}
  }
---
Layer pruning removes entire Transformer decoder blocks, causing a mismatch between the hidden states produced by surviving layers and the distributions they were trained to process, which can significantly degrade performance. We propose *Ghosted Layers*, a training-free recovery method that learns a closed-form optimal linear operator from a small calibration set to align boundary activations, consistently improving accuracy and perplexity across LLMs and pruning strategies while preserving the efficiency gains of layer pruning.
