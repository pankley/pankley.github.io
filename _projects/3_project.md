---
layout: page
title: High-Throughput Transcriptomics Across 61 Chemicals in Microalgae
description: Concentration-response RNA-seq in Raphidocelis subcapitata for mechanism-of-action profiling and tPOD derivation
img: assets/img/projects/microalgae_umap.png
importance: 2
category: Omics Research
related_publications: false
github: https://github.com/yourusername/microalgae-transcriptomics
---

A high-throughput transcriptomics screen of 61 chemicals in the freshwater
green alga *Raphidocelis subcapitata*, designed to extract mechanism-of-action
signals and transcriptomic points of departure from concentration-response
RNA-seq data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/microalgae_umap.png" title="MOA clustering" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/microalgae_heatmap.png" title="Pathway responses" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: unsupervised clustering of chemical mechanism-of-action signatures.
    Right: concentration-dependent pathway-level responses.
</div>

**Approach**

- Concentration-response modeling with `tcplfit2` and ComBat-seq batch
  correction across a 61-chemical library
- Mechanism-of-action clustering via UMAP and k-means
- Cross-species gene mapping to *Chlamydomonas* using DIAMOND BLASTX
- Signature scoring and tPOD derivation linking transcriptomic response
  to apical-level concern

Built in R with `tidyverse` conventions and a reproducible RNA-seq
QC and normalization pipeline.
