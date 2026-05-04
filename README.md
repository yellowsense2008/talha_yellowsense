# 🟡 Talha Nagina — Work at YellowSense Technologies

**Backend AI/ML Developer · YellowSense Technologies Pvt. Ltd.**
Bengaluru | Dec 2025 – Apr 2026

---

> YellowSense Technologies is a deep tech AI startup incubated at **IIIT Bangalore Innovation Centre**, recipient of the **MeitY TIDE 2.0 grant**, and an **STPI Nurtured Startup**. This repository is a collection of all projects built by Talha Nagina during his tenure, spanning financial fraud prevention, biometric authentication, healthcare AI, and industrial compliance.

---

## 📁 Repository Structure

This repo uses **Git submodules**. Each folder points to an independent project repository.

```
talha_yellowsense/
├── rbi-track2/                    → AppGuard AI (RBI HaRBInger 2025)
├── Track-B-contactless-fingerprint/  → CFAS Track B: Image Enhancement
├── Track-C-contactless-fingerprint/  → CFAS Track C: Siamese Matching
├── contactless-fingerprint-demo/     → Fingerprint Demo (v0 → v2, HuggingFace Space)
├── yellowsense-compliance-demo/      → GPCB Industrial Compliance Demo (HuggingFace Space)
├── RWE-analytics/                    → OphthoRWE / Real-World Evidence Analytics
└── ayush-healthcare/                 → VaidyaAI (AYUSH Healthcare / IndiaAI PS3)
```

---

## 🔴 1. AppGuard AI — Fake Banking App Detection

**Repo:** [`rbi-track2`](https://github.com/yellowsense2008/rbi-track2)
**Challenge:** RBI HaRBInger 2025 Innovation Challenge — Sub-Problem 2 (Prize Pool: ₹40 Lakh)

A **Regulatory Triangulation Engine** that detects unauthorized digital lending and banking apps targeting Indian consumers. Combines deterministic regulatory signals with probabilistic ML scoring.

**Key Features:**
- RBI NBFC registry cross-reference (9,185 entities) + DLA list (1,368 entities)
- **ARC Kill Switch** — hard CRITICAL override for Asset Reconstruction Companies
- AssetLinks cryptographic domain verification (SHA-256 certificate binding)
- Ghost App detection via Play Store lookup
- Permission compliance audit against **RBI Digital Lending Directions 2025** (18 prohibited permissions)
- **IndicSBERT** multilingual NLP brand impersonation detection (10 Indian languages)
- **MobSF** dynamic sandbox detonation + Chinese infrastructure cartel detection
- KFS runtime NLP compliance check (APR, grievance officer, cooling-off period)
- **CERT-In formatted PDF** investigation reports with RBI clause citations
- React.js + D3.js cartel threat network graph dashboard

**Stack:** Python 3.10, FastAPI, XGBoost, IndicSBERT, Androguard, MobSF, ReportLab, React.js, D3.js, GCP, Docker, Nginx

**Results:** 12/12 fake apps correctly flagged · 0 false positives on licensed banks · Live on GCP

---

## 🔵 2. CFAS — Contactless Fingerprint Authentication System

**Challenge:** UIDAI SITAA Challenge — Shortlisted for SEC (Subject Expert Committee) Screening

A 4-track on-device biometric pipeline for contactless fingerprint authentication deployable on standard Android smartphones with no specialised hardware.

### Track B — Image Enhancement
**Repo:** [`Track-B-contactless-fingerprint`](https://github.com/TalhaNagina/Track-B-contactless-fingerprint)

Classical + AI-based image enhancement pipeline for contactless fingerprint images.

- **CLAHE** (Contrast Limited AHE) for illumination correction
- **Gabor Filter Bank** (6 orientations, 2 scales) for ridge-valley frequency amplification
- PSNR improved: 24.3 → **28.7 dB** (+4.4 dB)
- SSIM improved: 0.68 → **0.81**
- Downstream matching accuracy: **+5%**
- Processing: **32 ms/frame**

**Stack:** Python, OpenCV, NumPy, scikit-image

---

### Track C — Siamese Fingerprint Matching
**Repo:** [`Track-C-contactless-fingerprint`](https://github.com/TalhaNagina/Track-C-contactless-fingerprint)

Contactless-to-contact fingerprint verification using a Siamese Neural Network.

- Backbone: **MobileNetV2** with contrastive loss
- Dataset: **HKPU** Contactless Fingerprint (450 test pairs)
- Accuracy: **82%** @ threshold 0.80 · F1: 0.78 · FAR: 18% · FRR: 27%
- Model: 45.2 MB (.h5) → **11.3 MB TFLite** (on-device)
- Inference: **412 ms** on-device

**Stack:** Python, TensorFlow 2.14, TFLite, MobileNetV2, NumPy

---

### Contactless Fingerprint Demo (v0 → v2)
**Space:** [`contactless-fingerprint-demo`](https://huggingface.co/spaces/talha-yellowsense/contactless-fingerprint-demo) *(HuggingFace Space)*

Iterative demo application built across three versions (v0, v1, v2) showcasing the end-to-end contactless fingerprint pipeline:

- **v0** — Basic minutiae extraction and quality assessment prototype
- **v1** — CLAHE + Gabor enhancement integrated, real-time camera feed
- **v2** — Full pipeline: quality → enhancement → Siamese matching → liveness; WebSocket streaming; 711 ms end-to-end

**Stack:** Python, Gradio, OpenCV, TensorFlow, MediaPipe, WebSocket

---

## 🟢 3. GPCB Industrial Compliance Demo

**Space:** [`yellowsense-compliance-demo`](https://huggingface.co/spaces/talha-yellowsense/yellowsense-compliance-demo) *(HuggingFace Space)*
**Challenge:** NASSCOM / GPCB AI Innovation Challenge (Grant: ₹8.5L against ₹10L ceiling)

An industrial effluent and emission monitoring system for the **Gujarat Pollution Control Board (GPCB)** with AI-driven anomaly detection and automated evidence generation.

**Key Features:**
- **Isolation Forest** for unsupervised anomaly detection in sensor streams
- **LSTM Autoencoder** for temporal anomaly detection (model drift aware)
- **XGBoost** for inspection prioritization scoring
- Behavioral forensics: evasion pattern detection (weekend violations, midnight dumping, threshold gaming)
- Automated legal evidence generation with audit trail
- Adaptive learning architecture for regulatory change resilience

**Stack:** Python, FastAPI, Scikit-learn, TensorFlow, XGBoost, Gradio

---

## 🟣 4. VaidyaAI — AYUSH Healthcare AI

**Repo:** [`ayush-healthcare`](https://github.com/TalhaNagina/ayush-healthcare)
**Challenge:** AYUSH PS3 / IndiaAI Mission Health Innovation Challenge

AI-powered healthcare platform integrating traditional AYUSH medicine knowledge with modern NLP and voice AI.

**Key Features:**
- Multilingual symptom analysis and AYUSH remedy recommendation
- FastAPI REST backend with Gemini LLM integration
- React.js frontend with voice input support
- Deployed on GCP with Nginx reverse proxy

**Stack:** Python, FastAPI, Gemini LLM, React.js, GCP, Nginx

---

## 🔵 5. RWE Analytics — OphthoRWE Platform

**Repo:** [`RWE-analytics`](https://github.com/TalhaNagina/RWE-analytics)
**Challenge:** Roche Drishti HealthTech Challenge (Grant target: ₹35L)

Real-World Evidence analytics platform for ophthalmology, targeting privacy-preserving clinical data analysis.

**Key Features:**
- HL7/FHIR connector for EHR interoperability
- K-anonymity implementation for patient privacy
- AMD SEV-SNP Trusted Execution Environment (TEE) integration
- DPDP Act 2023 compliance (Data Processor positioning)
- Statistical RWE pipelines for ophthalmic outcomes research

**Stack:** Python, FastAPI, PostgreSQL, HL7/FHIR, TEE/AMD SEV-SNP

---

## 🏆 Challenges & Recognition

| Challenge | Organisation | Status |
|-----------|-------------|--------|
| RBI HaRBInger 2025 — Sub-Problem 2 | Reserve Bank of India | Submitted (₹40L Prize Pool) |
| UIDAI SITAA Challenge | UIDAI | **Shortlisted for SEC Screening** |
| NASSCOM / GPCB AI Innovation | NASSCOM + GPCB | Proposal Submitted |
| AYUSH PS3 / IndiaAI Mission | IndiaAI + AYUSH Ministry | Submitted |
| Roche Drishti HealthTech | Roche India | Pitch Completed |
| India AI Impact Summit 2026 | STPI | **Exhibited** (Bharat Mandapam, New Delhi) |

---

## 🛠 Tech Stack Overview

| Category | Technologies |
|----------|-------------|
| **Languages** | Python 3.10, JavaScript |
| **Frameworks** | FastAPI, React.js |
| **ML / DL** | TensorFlow 2.14, TFLite, XGBoost, Scikit-learn |
| **NLP** | IndicSBERT, Gemini LLM, Sentence-Transformers |
| **Computer Vision** | OpenCV, MediaPipe, Gabor Filters, CLAHE |
| **APK Analysis** | Androguard, MobSF, apktool |
| **Infrastructure** | GCP, Docker, Nginx, WebSocket |
| **Demos** | HuggingFace Spaces, Gradio |
| **Data / Reports** | PostgreSQL, ReportLab, HL7/FHIR |

---

## 👤 About

**Talha Asif Nagina** · Backend AI/ML Developer
YellowSense Technologies Pvt. Ltd. · Bengaluru
[GitHub: @TalhaNagina](https://github.com/TalhaNagina)

---

*YellowSense Technologies Pvt. Ltd. · IIIT Bangalore Innovation Centre · MeitY TIDE 2.0 · STPI Nurtured Startup · CIN: U-62099-KA-2023-PTC-174648*
