---
title: "Hyperspectral Image Classification"
layout: single
permalink: /research/projects/hyperspectral/
author_profile: true
toc: true
toc_label: "On This Page"
toc_icon: "layer-group"
---

*In Progress — May 2026*

---

### Overview

Hyperspectral sensors capture hundreds of narrow spectral bands per pixel, producing a full reflectance spectrum at every spatial location. This rich spectral signature enables fine-grained material identification — distinguishing vegetation types, soil composition, building materials, and camouflaged targets that appear identical in optical or even multispectral imagery.

Each pixel is fundamentally a 200-band spectral signal. Viewed this way, hyperspectral classification is a signal classification problem directly analogous to SAR ATR: the spatial context provides spatial structure, but the discriminative information lives in the spectral dimension.

**Defense relevance:** Hyperspectral imaging from UAV and satellite platforms is a key capability for target identification, camouflage detection, and materials intelligence. The methodology developed here extends naturally to sensor fusion with SAR.

---

### Research Progression

| Phase | Dataset | Spatial Size | Bands | Classes | Status |
|-------|---------|--------------|-------|---------|--------|
| 1 | Indian Pines | 145×145 px | 200 | 16 | In Progress |
| 2 | Pavia University | 610×340 px | 103 | 9 | Planned |
| 3 | Houston 2018 | Large | 48 | 20 | Planned |
| 4 | SAR + Hyperspectral Fusion (SEN12MS) | — | — | — | Planned |

**Indian Pines** (AVIRIS sensor, northwest Indiana) — The standard benchmark. 16 agricultural land cover classes. Small enough to run in seconds on a laptop, establishing and validating the full pipeline.

**Pavia University** (ROSIS sensor, urban scene) — More defense-relevant. 9 classes distinguishing urban materials: asphalt, meadows, gravel, trees, painted metal, bare soil, bitumen, brick, shadows.

**Houston 2018** (IEEE GRSS Data Fusion Contest) — Real-world complexity. Airborne hyperspectral over Houston urban area. Standard benchmark for the remote sensing community.

**SAR + Hyperspectral Fusion** — The unique angle. Combining Sentinel-1 SAR (weather-independent, structure) with Sentinel-2 multispectral (spectral discrimination) for joint classification using SEN12MS dataset.

---

### Methods

ConvNeXt backbone adapted for spectral input; spatial patches treated as image crops. Prototypical networks for few-shot evaluation (methodology transferred from SAR ATR work). UMAP analysis of spectral embeddings for every dataset and training phase.

Spatial-block train/test splits (never random pixel splits) to prevent spatial autocorrelation leakage — the same rigor applied in the SAR ship classification work.

---

### Feature Space Visualizations

UMAP projections of learned spectral embeddings will appear here as results accumulate.

*(Figures will be added — images in `/assets/images/projects/hyperspectral/`)*

---

### Results

*(Results will be added as experiments complete)*

---

### Code

[GitHub →](https://github.com/mousashaya/hyperspectral){: .btn .btn--inverse}
