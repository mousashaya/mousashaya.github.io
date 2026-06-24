---
layout: single
title: "Resume"
permalink: /resume/
author_profile: false
classes: wide
---

<style>
/* ── Print styles ─────────────────────────────────────────── */
@media print {
  .masthead, .page__footer, .page__related,
  .author__urls-wrapper, .btn, .toc,
  .page__hero, nav, .breadcrumbs,
  .js-notice, .notice--info { display: none !important; }
  .page { padding: 0; margin: 0; }
  .page__content { font-size: 11pt; line-height: 1.45; }
  h1 { font-size: 18pt; margin-bottom: 2pt; }
  h2 { font-size: 13pt; border-bottom: 1pt solid #999; margin-top: 14pt; margin-bottom: 4pt; }
  h3 { font-size: 11pt; margin-bottom: 2pt; }
  a { color: inherit; text-decoration: none; }
  .resume-header { text-align: center; margin-bottom: 12pt; }
  .resume-contact { font-size: 10pt; color: #444; }
  ul { margin-top: 2pt; margin-bottom: 4pt; padding-left: 18pt; }
  li { margin-bottom: 1pt; }
  .job-header { display: flex; justify-content: space-between; }
  .no-print { display: none !important; }
}

/* ── Screen layout ────────────────────────────────────────── */
@media screen {
  .resume-header { text-align: center; margin-bottom: 1.5em; }
  .resume-contact { color: #555; font-size: 0.9em; margin-top: 0.3em; }
  .job-header { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.25em; }
  .job-header strong { font-size: 1.02em; }
  .job-header span { color: #666; font-size: 0.92em; }
  .section-divider { border: none; border-top: 1px solid #e0e0e0; margin: 1.2em 0; }
  .earlier { background: #f8f8f8; border-left: 3px solid #ccc; padding: 0.6em 1em; margin: 0.8em 0; font-size: 0.96em; }
  .print-btn { float: right; margin-bottom: 1em; }
}
</style>

<div class="resume-header">
<h1 style="margin-bottom:0.1em">Mousa Shaya</h1>
<div class="resume-contact">
Acton, Massachusetts &nbsp;|&nbsp;
<a href="mailto:mshaya01.ml@gmail.com">mshaya01.ml@gmail.com</a> &nbsp;|&nbsp;
<a href="https://linkedin.com/in/mousashaya">linkedin.com/in/mousashaya</a> &nbsp;|&nbsp;
<a href="https://github.com/mousashaya">github.com/mousashaya</a>
</div>
</div>

<button class="btn btn--primary print-btn no-print" onclick="window.print()">Print / Save PDF</button>

---

## Summary

Senior software architect and ML researcher with 45+ years of depth across real-time embedded systems,
enterprise Java/cloud platforms, and modern deep learning pipelines. Seven patents in deployed
biosignal pattern recognition (HP/Agilent, ICU deployment worldwide). Current work spans SAR remote
sensing, biosignal ML, biodiversity informatics, and security operations tooling. Founder,
Shaya Software and Systems LLC.

---

## Skills

**ML & Data Science:** Python, PyTorch, scikit-learn, XGBoost, SHAP, DINOv2, BioCLIP, ViT,
UMAP, HDBSCAN, SAR/remote sensing (Sentinel-1 SLC/GRD), PSG/EEG/ECG signal processing,
HuBERT, Wav2Vec 2.0, MAFFT, IQ-TREE2, phylogenetic inference

**Security & Infrastructure:** OpenSearch/Elasticsearch, Wazuh SIEM, MITRE ATT&CK,
NIST 800-171, CMMC, Python/Starlette, REST APIs

**Enterprise Java & Cloud:** Java, Spring Boot, AWS (DynamoDB, RDS, ElastiCache), JPA, Hibernate,
MyBatis, Tomcat, JMS, SOAP/REST, JSON, JDBC

**Databases:** PostgreSQL, MySQL, SQL Server, DynamoDB, HSQL, SQLAnywhere

**Methods & Tools:** Git, Maven, Scrum, Kanban, UML, Root Cause Analysis, API governance,
microservices architecture, database design (Erwin)

---

## Experience

<div class="job-header">
<strong>Shaya Software and Systems LLC</strong>
<span>2023 – Present &nbsp;·&nbsp; Acton, MA</span>
</div>
*Founder & Principal Consultant*

**ML Research**

- **SAR Automatic Target Recognition** — systematic generalization study across depression angles,
  sensor configs, and datasets (ATRNet-STAR, MSTAR). Six contributions including +30 pp accuracy
  improvement from multi-angle training, 98%+ few-shot accuracy with 5 reference images per class.
  Under review, IEEE Geoscience and Remote Sensing Letters.

- **SAR Ship Classification** — ship type classification from Sentinel-1 SLC imagery with a
  multi-signal AIS label resolver (AIS type, ship length, GFW classification, name keywords)
  resolving 87% of 2,088 vessels without manual annotation. DINOv2 ViT-S/14 classifier on
  resolved labels. Under review, IEEE.

- **PhysioNet 2026 Challenge** — open-source algorithms for cognitive impairment screening from
  polysomnography (PSG) — EEG, ECG, and other physiological signals. Training data from five
  US academic medical centers.

- **Lichen Image Classification** — BioCLIP ViT-L/14 + ArcFace metric learning classifier for
  species-level lichen identification. Two-stage training on iNaturalist and expert-labeled
  Lichen Consortium data (~15,000 images, ~10,000 species). ~95% top-1 accuracy.
  Collaboration with Dr. Frank Bungartz, Arizona State University.

**Security Operations Tooling**

- Designed and developed a browser-based SOC dashboard for Wazuh/OpenSearch SIEM environments:
  MITRE ATT&CK kill chain timeline visualization, NIST 800-171 and CMMC compliance gap
  detection, SCA policy assessment, vulnerability management, geo-IP enrichment, multi-source
  log normalization (Wazuh 4/5, Elastic Security ECS), multi-tenant architecture, and scheduled
  PDF reporting. Python/Starlette backend, OpenSearch, single-file HTML/CSS/JS frontend.

**Biodiversity Database Engineering** *(ASU Lichenology Consortium, Nov 2024–Present)*

- Cleaned the Consortium database: removed 35,000 non-lichen taxa, added 60,000 validated taxa
  from Mycobank and Index Fungorum, updated 200,000 records with external source references.
  Implemented cross-source correlator (LIAS, Mycobank, Index Fungorum) with lichen filter and
  taxonomic hierarchy validation. Contributor to Symbiota open-source platform.

- Phylogenetic analysis: parsed ~51K GenBank DNA records (8 loci), MAFFT alignment,
  trimAl trimming, IQ-TREE2 maximum likelihood inference, LIAS trait mapping onto trees.

- UMAP + HDBSCAN clustering over LIAS DELTA morphological data (10,709 species,
  880 chemical compounds); interactive three-panel cluster browser.

<hr class="section-divider"/>

<div class="job-header">
<strong>ALKU Consulting</strong>
<span>2023 – 2025</span>
</div>
*Independent Consultant*

- **COOP FCL — UKG/JDE Integration (2024–2025):** Integrated UKG Activities module with Oracle
  JD Edwards Orchestrator APIs for employee activity tracking in a refinery environment.
  Built all UKG Activity structures and bidirectional sync; Java application deployed on-premise.

- **COOP FCL — Automated Testing (2025):** Developed UKG API test harness using UAT environment
  to punch in/out employees across scenarios (daily OT, weekly OT, stat pay, lunch deduct, RBS,
  stat holiday). Automated hourly comparison to expected hours; production config verification.

- **BJs — Workforce Management (2023):** Application consulting: Wi-Fi automation, clock
  configuration, dataviews, attestation, TestAssured, business structure, employee groups.
  UAT refresh and UAT-to-PRD configuration transfer via SDM.

<hr class="section-divider"/>

<div class="job-header">
<strong>Kronos / UKG</strong>
<span>2018 – 2023 &nbsp;·&nbsp; Lowell, MA</span>
</div>
*Principal Architect*

- One of two architect leads directing 11 teams (~110 engineers, testers, team leads) across
  Belarus and Lowell to migrate on-premise Activity product to cloud-based Dimensions platform.

- Lead architect for the Kiosk product: secure, limited Dimensions access via badge ID, full
  authentication, and federated login. Led three teams across Noida and Lowell.

- Lead architect for production SQL performance remediation across 1,000+ customer clusters;
  reduced database CPU utilization significantly through query plan analysis and index redesign.

- Responsibilities across all projects: stakeholder and product owner requirements, high-level
  architecture and database design, API governance, UX standards, security reviews, production
  incident response, microservices migration.

<hr class="section-divider"/>

<div class="job-header">
<strong>MicroFocus</strong>
<span>2017 – 2018</span>
</div>
*Team Lead & Scrum Master*

Team lead and Scrum Master for Control Point releases. Backlog grooming, SQL Server normalization,
and data flow optimization.

<hr class="section-divider"/>

<div class="job-header">
<strong>Hewlett Packard Enterprise</strong>
<span>2016 – 2017</span>
</div>
*Principal Software Development*

- Scaled legacy SQL Server solution to several hundred million documents using file groups,
  partitioned tables, index optimization, and execution plan analysis.

- Designed and prototyped a federated PostgreSQL + HSQL distributed document analysis system
  for scanning billions of documents; Java Spring Boot, Tika, OpenNLP, REST architecture.

<hr class="section-divider"/>

<div class="job-header">
<strong>Kayak</strong>
<span>2014 – 2016 &nbsp;·&nbsp; Concord, MA</span>
</div>
*Software Architect, Hotel Search*

Extended hotel search with 12+ new providers (SOAP/JSON/XML); booking/cancellation for two new
providers. Aggregated Hadoop/Hive performance metrics into MySQL for monitoring. Created public
REST APIs; implemented AES encryption of sensitive data; optimized inventory priming for faster
user searches.

<hr class="section-divider"/>

<div class="job-header">
<strong>Nokia Digital Commerce</strong>
<span>2012 – 2014 &nbsp;·&nbsp; Burlington, MA</span>
</div>
*Principal Software Development Engineer / Project Lead*

- Architected and delivered payment policy service for Nokia mobile commerce: credit card and
  150 operator billing methods worldwide. Delivered in 4.5 months with limited resources.
  AWS, Spring, REST, JSON, JPA, Amazon RDS.

- Designed NextGen in-app purchasing for all Nokia devices: simplified payment API, improved
  UX and throughput on high-latency networks, Spring/JBoss, MySQL.

- Product restoration service for purchased content across devices; DynamoDB with global indices
  and ElastiCache for eventual consistency.

<hr class="section-divider"/>

<div class="earlier">

**Earlier career (pre-2012)**

**MathWorks** *(2006–2012, Natick MA) — Principal Software Dev / DB Architect:*
Designed build-and-test control systems using DAG-based job scheduling (JGraphT, PriorityQueue,
JMS/ActiveMQ). Created database migration tooling to minimize deployment downtime. Led
Perl-to-Java transition for server-side infrastructure.

**Nokia Internet Communications** *(2000–2006, Burlington MA) — Principal Software Dev:*
Designed persistence layer for network configuration management (NHM 2.0). Implemented
distributed database replication using MobiLink session-based engine, including a conflict
resolution strategy adopted by Sybase. Swing-based graphical database access tool.

**HP / Agilent Technologies** *(1979–2000, Andover MA) — Software Development Engineer:*
Designed real-time ECG pattern recognition algorithms deployed in ICUs worldwide — the first
product in the industry to successfully monitor patients with pacemakers. Seven patents awarded.
Project lead for AIM (Arrhythmia Information Management): real-time ECG/blood pressure waveform
capture and review system. Lead for distributed database and patient data acquisition subsystem.

</div>

---

## Education

**Northeastern University** — Boston, MA  
BSEE / MSEE — Communications Systems and Digital Signal Processing

---

## Patents (HP / Agilent Technologies)

1. US 4,664,116 — Pace Pulse Identification Apparatus
2. US 4,832,041 — Pace Pulse Eliminator
3. US 4,539,999 — Method and Device for Subtracting a Pacer Signal from an ECG Signal
4. US 4,838,278 — Paced QRS Complex Classifier
5. US 5,447,164 — Interactive Medical Information Display System and Method for Displaying
   User-Definable Patient Events
6. A61B5/7264 — Classification of Physiological Signals Using Neural Networks, Statistical
   Classifiers, and Expert Systems

---

## Affiliations

- ASU Research Affiliate — Arizona State University
- Member — AFCEA Lexington-Concord Chapter
- SAM.gov Registered Vendor — UEI YK29WQZ22EM3
- Registered Expert — GLG Expert Network / Catalant
- Member — American Bryological and Lichenological Society (ABLS)
- Contributor — Consortium of North American Lichen Herbaria (CNALH) / Symbiota
