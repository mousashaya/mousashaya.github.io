---
title: "SAR Automatic Target Recognition"
layout: single
permalink: /research/projects/sar-atr/
author_profile: true
toc: true
toc_label: "On This Page"
toc_icon: "satellite"
---

**ATRNet-STAR: Depression Angle Diversity, Few-Shot Recognition, and Cross-Dataset Generalization in SAR Automatic Target Recognition**  
Mousa Shaya · Shaya Software and Systems LLC \| Arizona State University  
*arXiv preprint, May 2026*

[Paper (arXiv) →](https://arxiv.org/abs/2506.XXXXX){: .btn .btn--primary}
[Code →](https://github.com/mousashaya/sar-atr-ship){: .btn .btn--inverse}

---

### Overview

Synthetic Aperture Radar (SAR) enables all-weather, day/night target recognition — a critical capability for defense and intelligence applications. This study systematically evaluates SAR ATR generalization across three axes that matter operationally but are rarely studied together: depression angle variation, data scarcity (few-shot), and cross-dataset transfer.

The work uses two benchmarks: **ATRNet-STAR** (40 vehicle classes across 4 depression angles: 15°, 30°, 45°, 60°) and **MSTAR** (10 vehicle classes, standard operating conditions and extended operating conditions).

---

### Key Results

| Experiment | Accuracy |
|------------|----------|
| SOC baseline (ConvNeXt-Small) | 97.2% |
| EOC — 15° only model, tested at other angles | 43.7% |
| EOC — adding 60° to training | **74.1%** (+30.4 pp) |
| Prototypical (5 shots per class) | **98.2%** |
| MSTAR (cross-dataset transfer) | 99.1% |
| Cross-dataset transfer (ATRNet→MSTAR) | 61.1% |
| DINOv2 optical features on SAR | 6.1% (near-chance) |
| Test-time augmentation (TTA) | −24.3 pp vs. baseline |

**Key finding:** Depression angle is the dominant challenge in operational SAR ATR. A model trained on a single angle collapses to 43.7% at other angles. Adding multi-angle training data is more effective than any architectural improvement. Optical foundation model features (DINOv2) are near-useless on SAR — SAR requires SAR-trained features.

---

### Feature Space Analysis (UMAP)

The figures below show the 768-dimensional ConvNeXt feature space projected to 2D via UMAP, color-coded by vehicle class.

*(UMAP figures will appear here — images in `/assets/images/projects/sar-atr/`)*

---

### Methods

**Backbone:** ConvNeXt-Small pretrained on ImageNet-1k, fine-tuned on single-channel SAR chips (64×64 px, log-amplitude normalized).

**Few-shot:** Prototypical networks — class prototypes computed as mean of support embeddings; test samples classified by nearest prototype in embedding space.

**Evaluation:** Standard Operating Conditions (SOC) follow the MSTAR convention. Extended Operating Conditions (EOC) test across depression angles not seen during training.

**Cross-dataset:** Model trained on ATRNet-STAR, evaluated zero-shot on MSTAR (no MSTAR training data used).

---

### Datasets

| Dataset | Classes | Angles | Resolution | Size |
|---------|---------|--------|------------|------|
| ATRNet-STAR | 40 | 15°, 30°, 45°, 60° | ~0.3m | ~100K chips |
| MSTAR | 10 | 15°, 17° | ~0.3m | ~5K chips |

---

### Citation

```
@article{shaya2026atrnetstar,
  title={ATRNet-STAR: Depression Angle Diversity, Few-Shot Recognition,
         and Cross-Dataset Generalization in SAR Automatic Target Recognition},
  author={Shaya, Mousa},
  journal={arXiv preprint arXiv:2506.XXXXX},
  year={2026}
}
```
