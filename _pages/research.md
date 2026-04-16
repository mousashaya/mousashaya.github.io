---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Lichen Biodiversity Informatics & ML Classification

**Nov 2024 – Present · Arizona State University Research Affiliate**

Collaborating with Dr. Frank Bungartz, Collections Manager of Lichens at Arizona State University and domain authority on lichen taxonomy, on a multi-component research program spanning database engineering, phylogenetics, and deep learning image classification.

### ML Image Classification Pipeline

Developing a BioCLIP ViT-L/14 + ArcFace metric learning classifier for species-level lichen identification from images. Two-stage training design: large-scale noisy pretraining on iNaturalist aggregated imagery, followed by fine-tuning on expert-labeled Lichen Consortium data (~15,000 images across ~10,000 species).

- UMAP + HDBSCAN clustering pipeline built over LIAS DELTA morphological data (10,709 species, 880 chemical compounds)
- Interactive three-panel browser-based cluster viewer for exploratory analysis
- Clustering analysis revealed clean photobiont-type separation — validating signal in morphological feature space
- Embedding ensemble strategy: BioCLIP / DINOv2 / CLIP for robust representation

### Phylogenetic Analysis Pipeline

End-to-end pipeline from raw GenBank HTML-wrapped flat files through aligned multi-locus phylogenetic inference:

- Parsed ~51K GenBank DNA records (8 loci: ITS, 18S, 28S, RPB2, and others) producing 49,610 valid records
- MAFFT alignment, trimAl trimming, IQ-TREE2 maximum likelihood inference
- Primary focus on ITS, 18S, and 28S loci for Lecanoromycetes phylogeny
- Mapping LIAS morphological and chemical trait data onto inferred phylogenetic trees

### Database Engineering & Taxonomy Cleanup

PostgreSQL database (fungix schema) integrating LIAS DELTA, Mycobank, and Index Fungorum data sources:

- Removed 35,000 non-lichen taxa from the Consortium database
- Added 60,000 new validated taxa from Mycobank and Index Fungorum
- Updated all 200,000 taxa records with external source references and protolog data
- Contributor to Symbiota open-source platform — sourceIdentifiers across all taxonomic tree explorers

### Parallel Investigation: PCG Classification

Active investigation of heart sound (phonocardiogram) classification using mel-spectrogram + Vision Transformer architectures and pretrained audio foundation models (HuBERT, Wav2Vec 2.0) — directly extending ECG signal processing expertise to acoustic cardiac signals.

### Affiliations

- ASU Research Affiliate — Arizona State University
- Member — American Bryological and Lichenological Society (ABLS)
- Contributor — Consortium of North American Lichen Herbaria (CNALH) / Symbiota
- Registered — ODSC AI East 2026, Boston MA
