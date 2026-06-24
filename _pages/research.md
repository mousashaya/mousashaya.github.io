---
layout: single
title: "Research"
permalink: /research/
---

## SAR Automatic Target Recognition — Generalization Study

**2025–2026 · Under Review, IEEE Geoscience and Remote Sensing Letters**

Systematic study of SAR ATR generalization across depression angles, sensor configurations,
and datasets using the ATRNet-STAR dataset (40 vehicle classes, 4 depression angles)
and the MSTAR benchmark (10 military vehicle classes).

Six contributions:
- Depression angle ablation: adding a single 60° view to a 15°-only baseline improves
  EOC accuracy by +30.4 percentage points
- Data efficiency: multi-angle training with as few as 25 images per vehicle per angle
  surpasses models trained on thousands of single-angle images
- Neither angle-weighted sampling nor test-time augmentation improves EOC performance —
  TTA reduces accuracy by 24.3 pp — confirming angle invariance requires real multi-angle data
- Few-shot prototypical classifier achieving 98%+ accuracy with only 5 reference images per class
- Cross-dataset transfer revealing a 38 pp SAR-to-SAR domain gap
- DINOv2 optical pretrained features achieve only 6.1% on SAR ATR —
  directly motivating domain-specific SAR backbone development

**Preprint:** [https://doi.org/10.5281/zenodo.20492213](https://doi.org/10.5281/zenodo.20492213)

---

## SAR Ship Type Classification from Sentinel-1 SLC Imagery

**2025–2026 · Under Review, IEEE**

Ship type classification from SAR imagery addressing two underappreciated problems:
noisy AIS vessel type codes used as ground truth, and predominant reliance on GRD
products when free SLC data with finer resolution is available from the same sensor.

Key contributions:
- Multi-signal label resolver combining AIS type code, ship length, Global Fishing Watch
  classification, and vessel name keywords into a confidence-weighted vote —
  resolving 87.3% of 2,088 vessels to reliable type labels without manual annotation
- DINOv2 ViT-S/14 classifier trained on resolved labels comparing SLC and GRD chips
  under identical experimental conditions
- Public release of pipeline, labels, and 4,306 dual-polarisation SLC chips covering
  2,088 unique vessels in the Gulf of Mexico

**Preprint:** [https://doi.org/10.5281/zenodo.20492437](https://doi.org/10.5281/zenodo.20492437)

---

## ShayaSAR — General SAR Foundation Model (Deprioritized)

**2026 · Explored, not pursued**

Investigated DINOv2 fine-tuning on the Sentinel-1 SAR channel of SSL4EO-S12 v1.1.
Investigation concluded that the approach did not offer sufficient benefit over existing
methods to warrant continued development.

---

## George B. Moody PhysioNet Challenge 2026 (Active)

**2026 · Screening for Cognitive Impairment During Sleep Studies**

Developing open-source algorithms using polysomnography (PSG) recordings —
including EEG, ECG, and other physiological signals — to predict future diagnoses
of cognitive impairment. Training data from five US institutions: Beth Israel Deaconess
Medical Center, Emory University, Kaiser Permanente, Massachusetts General Brigham,
and Stanford University.

Directly extends HP/Agilent ECG signal processing background to modern
multi-signal biosignal ML in a clinical research context.

**Challenge site:** [https://moody-challenge.physionet.org/2026/](https://moody-challenge.physionet.org/2026/)

---

## MIMIC-IV Cardiac Readmission Prediction (In Progress)

**2026 · Credentialing in Progress**

Planned: 30-day readmission prediction for heart failure patients using MIMIC-IV
clinical data. XGBoost classifier with SHAP feature-level explainability for
clinical risk stratification. Targeting medRxiv preprint and GitHub reproducible release.
Relevant to CMS/HHS priorities and MITRE Health FFRDC work.

---

## Lichen Biodiversity Informatics & ML Classification

**Nov 2024 – Present · Arizona State University Research Affiliate**

Collaborating with Dr. Frank Bungartz, Collections Manager of Lichens at Arizona
State University, on a multi-component research program spanning database engineering,
phylogenetics, and deep learning image classification.

### ML Image Classification Pipeline

BioCLIP ViT-L/14 + ArcFace metric learning classifier for species-level lichen
identification from images. Two-stage training: large-scale noisy pretraining on
iNaturalist aggregated imagery, followed by fine-tuning on expert-labeled Lichen
Consortium data (~15,000 images across ~10,000 species). Approximately 95% top-1
accuracy. Pending publication with Dr. Frank Bungartz.

- UMAP + HDBSCAN clustering pipeline over LIAS DELTA morphological data
  (10,709 species, 880 chemical compounds)
- Interactive three-panel browser-based cluster viewer for exploratory analysis
- Clustering analysis revealed clean photobiont-type separation
- Embedding ensemble: BioCLIP / DINOv2 / CLIP

### Phylogenetic Analysis Pipeline

- Parsed ~51K GenBank DNA records (8 loci: ITS, 18S, 28S, RPB2, and others)
- MAFFT alignment, trimAl trimming, IQ-TREE2 maximum likelihood inference
- Mapping LIAS morphological and chemical trait data onto inferred phylogenetic trees

### Database Engineering & Taxonomy Cleanup

PostgreSQL database (fungix schema) integrating LIAS DELTA, Mycobank,
and Index Fungorum:
- Removed 35,000 non-lichen taxa from the Consortium database
- Added 60,000 new validated taxa from Mycobank and Index Fungorum
- Updated all 200,000 taxa records with external source references
- Contributor to Symbiota open-source platform

### PCG Heart Sound Classification (Investigating)

Investigation of phonocardiogram classification using mel-spectrogram + Vision
Transformer architectures and pretrained audio foundation models (HuBERT, Wav2Vec 2.0)
— extending ECG signal processing expertise to acoustic cardiac signals.

---

## Security Operations Tooling

**2026 · In Development**

Browser-based security operations center (SOC) dashboard for open-source SIEM environments,
addressing the usability gap between raw Wazuh deployments and what SOC analysts and
compliance auditors actually need. Full-stack: Python/Starlette async backend, OpenSearch
as the query engine, and a single-file HTML/CSS/JS frontend deployable with no external
dependencies.

Key capabilities built:

- **Kill chain timeline visualization** — multi-agent event timeline with MITRE ATT&CK
  tactic and technique annotation, derived from Wazuh rule group analysis when explicit
  ATT&CK fields are absent. Three-tier layout: heatmap, per-agent timeline lanes, and
  pinned alert detail. Phase coloring (Recon / Initial Access / Lateral Movement /
  Exfiltration) derived from rule group membership at render time.
- **Compliance posture dashboard** — rule coverage mapped to NIST 800-171 and CMMC
  control domains. Three states per domain: monitoring active and clean, monitoring
  active with incidents, and no monitoring configured — the gap. Designed for auditors,
  not just analysts.
- **SCA policy visualization** — Security Configuration Assessment results across all
  monitored agents, with pass/fail/not-applicable drill-down per policy check and
  per-agent comparison.
- **Vulnerability management** — CVE inventory per agent with severity bucketing and
  cross-agent trend tracking.
- **Geo-IP enrichment** — source IP country resolution using a bundled IP database;
  no external API dependency, no vendor registration required.
- **Multi-source normalization** — canonical internal alert model mapping Wazuh 4.x,
  Wazuh 5.x, and Elastic Security (ECS) schemas, selectable by config without UI changes.
  Opens the same interface to Suricata, Zeek, and Filebeat sources.
- **Multi-tenant architecture** — per-customer data isolation for MSSP deployments.
- **Scheduled reporting** — configurable PDF summary delivery; designed for managers who
  cannot monitor a live dashboard.
- **File Integrity Monitoring view** — FIM event log with expandable rows showing before/after
  file hashes, change type, and owning agent.

---

## Affiliations

- ASU Research Affiliate — Arizona State University
- Member — AFCEA Lexington-Concord Chapter
- Registered Expert — GLG Expert Network
- Registered Consultant — Catalant
- SAM.gov Registered Vendor — UEI YK29WQZ22EM3
- Participant — George B. Moody PhysioNet Challenge 2026
- Member — American Bryological and Lichenological Society (ABLS)
- Contributor — Consortium of North American Lichen Herbaria (CNALH) / Symbiota
- Registered — ODSC AI East 2026, Boston MA

---
