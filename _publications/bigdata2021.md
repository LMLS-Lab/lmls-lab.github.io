---
# TODO: Template entry. Duplicate this file per publication (e.g. lee2026fedopt.md),
# fill in the fields, then delete this example (or keep `published: false`).
published: true
title: "Supporting Data Compression in PnetCDF"
authors: "Kaiyuan Hou, Qiao Kang, Sunwoo Lee, Ankit Agrawal, Alok Choudhary, Wei-keng Liao"
venue: "BigData"
year: 2021
type: "conference"          # conference | journal | preprint | workshop
doi: "10.1109/BigData52589.2021.9671998"                     # DOI (without the https://doi.org/ prefix), optional
bibtex: |
  @inproceedings{hou2021supporting,
    title={Supporting data compression in PnetCDF},
    author={Hou, Kaiyuan and Kang, Qiao and Lee, Sunwoo and Agrawal, Ankit and Choudhary, Alok and Liao, Wei-keng},
    booktitle={2021 IEEE International Conference on Big Data (Big Data)},
    pages={86--97},
    year={2021},
    organization={IEEE}
  }
---
This paper presents a variable compression feature for the Parallel NetCDF library that adopts HDF5-style chunking while enabling I/O aggregation across multiple requests, and shows through real-world scientific I/O kernels that handling multiple requests at once significantly improves parallel I/O performance on chunked and compressed data.
