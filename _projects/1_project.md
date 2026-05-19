---
layout: page
title: Multi-Species tPOD Bootstrapping Pipeline
description: with background image
img: assets/img/12.jpg
importance: 1
category: Methods & Computational Tools
related_publications: true
github: https://github.com/pankley/tpod-bootstrap
---

An R-based framework for deriving transcriptomic points of departure (tPODs) from concentration-response RNA-seq data, with explicit decomposition of uncertainty into gene-resampling (L1) and BMD-estimation (L2) components. The pipeline spans four aquatic species and supports five tPOD derivation methods, enabling systematic cross-method and cross-species comparison.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/tpod_forest_plot.png" title="tPOD forest plot" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/tpod_uncertainty.png" title="Uncertainty decomposition" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: tPOD estimates with bootstrap confidence intervals across methods.
    Right: variance partitioned into L1 (gene resampling) and L2 (BMD estimation).
</div>

**Key features**

- Five derivation methods compared in a unified framework: r25th, p10th,
  first_mode, LCRD, and PODAccum
- Two-level bootstrap separating L1 and L2 variance components
- Parallelized execution with reproducible seeding
- Stability classification anchored to interpretable fold-change benchmarks
- Containerized for reproducible deployment

Built with `tidyverse` conventions and `tcplfit2` for concentration-response modeling. See the [repository]({{ "https://github.com/pankley/tpod-bootstrap" }})
for documentation and a worked example.
