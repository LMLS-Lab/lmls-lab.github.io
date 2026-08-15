---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Weight Concentration Regularization for Improving Pruning Robustness Under High Sparsity"
authors: "Vincent-Daniel Yun, Junhyuk Jo, Sunwoo Lee"
venue: "International Conference on Machine Learning Workshop"
year: 2026
type: "workshop"          # conference | journal | preprint | workshop
arxiv: "https://arxiv.org/abs/2511.14282"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
@article{yun2025weight,
  title={Weight Concentration Regularization for Improving Pruning Robustness Under High Sparsity},
  author={Yun, Vincent-Daniel and Jo, Junhyuk and Lee, Sunwoo},
  journal={arXiv preprint arXiv:2511.14282},
  year={2025}
}
---
This work proposes a Weight Concentration Regularizer (WCR) that, unlike prior uniform-shrinkage or scale-invariant sparsity regularizers, concentrates weight energy onto a small subset of informative parameters during training so that one-shot magnitude pruning removes mainly functionally negligible weights, yielding consistent pruning-robustness gains across LLM fine-tuning, image classification, and medical segmentation while remaining compatible with existing pruning-robust optimizers.
