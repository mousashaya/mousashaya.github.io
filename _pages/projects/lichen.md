---
title: "Lichen Biodiversity Informatics"
layout: single
permalink: /research/projects/lichen/
author_profile: true
toc: true
toc_label: "On This Page"
toc_icon: "leaf"
---

*Nov 2024 – Present · Arizona State University Research Affiliate*  
*Paused — resuming end of summer 2026*

---

### Overview

Collaboration with Dr. Frank Bungartz, Collections Manager of Lichens at Arizona State University and domain authority on lichen taxonomy. A multi-component research program spanning database engineering, phylogenetics, and deep learning image classification for the Consortium of Lichen Herbaria (CNALH).

---

### ML Image Classification Pipeline

BioCLIP ViT-L/14 + ArcFace metric learning classifier for species-level lichen identification from photographs.

* Two-stage training: large-scale noisy pretraining on iNaturalist aggregated imagery → fine-tuning on expert-labeled Consortium data (~15,000 images, ~10,000 species)
* UMAP + HDBSCAN clustering over LIAS DELTA morphological data (10,709 species, 880 chemical compounds)
* Clustering revealed clean photobiont-type separation — validating signal in morphological feature space
* Embedding ensemble: BioCLIP / DINOv2 / CLIP

---

### Phylogenetic Analysis Pipeline

End-to-end pipeline from raw GenBank HTML-wrapped flat files through maximum likelihood phylogenetic inference:

* Parsed ~51K GenBank DNA records (8 loci: ITS, 18S, 28S, RPB2, and others) — 49,610 valid records
* MAFFT alignment, trimAl trimming, IQ-TREE2 maximum likelihood inference
* Primary focus on Lecanoromycetes phylogeny (ITS, 18S, 28S loci)
* Mapping LIAS morphological and chemical trait data onto inferred trees

---

### Database Engineering & Taxonomy Cleanup

PostgreSQL database (fungix schema) integrating LIAS DELTA, Mycobank, and Index Fungorum:

* Removed 38,753 non-lichen taxa from the Consortium database
* Added 68,717 new validated taxa from Mycobank and Index Fungorum
* Updated 162,465 taxa records with external source references and protolog data
* Contributor to Symbiota open-source platform — sourceIdentifiers across all taxonomic tree explorers

---

### Presentations

**Taxonomic Data Enhancement of the Consortium of Lichen Herbaria (Symbiota)**  
ABLS Consortium Meeting · April 2026

[View Presentation →](/research/lichen-presentation/){: .btn .btn--primary}
