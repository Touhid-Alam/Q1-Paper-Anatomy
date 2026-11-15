# 📐 Q1-Paper-Anatomy: How to Write Justified Research Papers (Teaching Editions)

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Annotations](https://img.shields.io/badge/Margin%20Annotations-476%20Total-success.svg)](#the-4-teaching-editions-recommended-reading-order)
[![Domain](https://img.shields.io/badge/Domain-AI%20%7C%20Medical%20ML%20%7C%20CV%20%7C%20NLP-orange.svg)](#the-4-teaching-editions-recommended-reading-order)
[![PRs Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](#contributing--feedback)

> **"Most junior researchers don’t get rejected because their code is bad. They get rejected because they *describe* what they did instead of *justifying* why they did it."**

Welcome to **`Q1-Paper-Anatomy`** (Teaching Editions). When you are new to academic research, you are often told to *"go read 20 papers"* to learn how to write. The problem is that published papers show you the **finished product**, not the **hidden engineering and rhetorical decisions** behind every paragraph.

To bridge this gap, this repository provides **4 full-length research papers** (published across *Scientific Reports*, *Discover Artificial Intelligence*, and *Elsevier*) converted into **line-by-line "Teaching Editions"** with **476 static margin annotations**. 

Nothing needs to be clicked: every highlight on the manuscript is connected by a vector line to a margin note beside it, making these PDFs ideal for reading on a tablet, laptop, or printed out on your desk.

---

## 🎨 The 5-Category Colour Taxonomy

Every annotation in these four papers is colour-coded by what it teaches you to do:

| Category | Colour | What It Teaches You |
| :--- | :--- | :--- |
| **`SECTION ROLE`** | 🟦 **Blue** | What a section or subsection is for, and where it sits in the paper's macro-argument. |
| **`WRITING MOVE`** | 🟪 **Purple** | Standard rhetorical moves: context, problem, gap, aim, contribution, claim, and take-home. |
| **`JUSTIFICATION / RIGOR`** | 🟩 **Green** | Why a technical choice was made (dataset, split, scaler, baseline, metric) and how the text defends it *before* a reviewer asks. |
| **`RESULTS & INTERPRETATION`** | 🟧 **Orange** | How results are reported, compared, and clinically/mechanistically interpreted—not just repeated from tables. |
| **`HOW IT IS WRITTEN`** | 🩵 **Teal** | Sentence-level craft: signposting, transitions, hedging, defining notation, captions, and honest self-critique where our own text could be sharper. |

---

## 📚 The 4 Teaching Editions (Recommended Reading Order)

To get the most out of this repository, read the papers in the order below—progressing from foundational tabular pipelines to complex multi-stage, neuro-symbolic, and mathematical generative frameworks.

### Level 1: Foundational Tabular ML, Leakage Control & Feature Ablation
📄 **File:** [`1_Glioma_Ensemble_TEACHING_EDITION.pdf`](./1_Glioma_Ensemble_TEACHING_EDITION.pdf)  
* **Paper:** *A precise ensemble machine learning framework for improved glioma grading and classification with explainable AI* (*Computer Methods and Programs in Biomedicine Update*, Elsevier, 2026)
* **Total Annotations:** 113 marks
* **What You Will Learn:**
  * How to write a 5-move Abstract and a funnel-style Introduction ending in verb-first bulleted contributions.
  * How to turn a chronological Literature Review into a **Critical Synthesis (Section 2.3)** that directly motivates your methodology.
  * How to prove **zero data leakage** across text, figures, and pseudocode (fitting scalers exclusively on training data, stratified splits, and out-of-fold stacking predictions).
  * How to use Exploratory Data Analysis (EDA) to justify later design choices (e.g., class imbalance $\rightarrow$ MCC metric; racial skew $\rightarrow$ Section 5 fairness limitations).
  * How to validate XAI (SHAP/LIME) against established domain biology (WHO pathology guidelines) rather than just showing plots as decoration.

---

### Level 2: Data-Centric Multi-Stage Pipelines & Quantitative XAI Validation
📄 **File:** [`4_GANA-SkinAI_TEACHING_EDITION.pdf`](./5_GANA-SkinAI_TEACHING_EDITION.pdf)  
* **Paper:** *GANA-SkinAI: A Multi-Stage Generative Framework for Explainable and Interpretable Skin Cancer Classification* (*Elsevier Preprint*)
* **Total Annotations:** 133 marks
* **What You Will Learn:**
  * How to frame **4 numbered research gaps** in the Introduction and map your contributions 1-to-1 to answer them.
  * How to prevent patient/lesion data leakage on multi-image medical datasets (`lesion_id` `GroupKFold`) and prove it with a verification table (Table 3).
  * How to argue a **data-centric vs. model-centric** thesis by benchmarking 15 diverse CNN and Vision-Transformer architectures across 3 conditions (Baseline vs. Standard Augmentation vs. Proposed Pipeline) plus a 5-step component ablation.
  * How to move beyond visual FID scores to **statistical feature preservation** (paired $t$-tests on LBP/GLCM texture and ABCD morphological features) and **quantitative XAI spatial overlap** (IoU, Dice, and NDCG against segmentation masks).
  * How to write a dedicated **Failure Mode & Hallucination Analysis** (Table 24) to build reviewer trust.

---

### Level 3: Hybrid / Neuro-Symbolic Architectures, Fair Baselines & Clinical Safety Metrics
📄 **File:** [`2_MH-EABERT_TEACHING_EDITION.pdf`](./2_MH-EABERT_TEACHING_EDITION.pdf)  
* **Paper:** *MH-EABERT: an adaptive fusion approach with emotion knowledge-enhanced BERT for explainable mental health sentiment analysis from social media* (*Scientific Reports*, Nature Portfolio, 2026)
* **Total Annotations:** 113 marks
* **What You Will Learn:**
  * How to open an Abstract and Introduction with a **two-sided tension** (*deep learning is accurate but opaque vs. symbolic rules are interpretable but rigid*) to naturally set up a hybrid architecture.
  * How to build a Literature Review positioning table (Table 1) that maps each competitor's **Core Limitation** to your **Specific Improvement**.
  * How to anchor a handcrafted module (MHEL lexicon) in established domain theory (Beck's Cognitive Triad & PHQ-9/GAD-7) so it isn't dismissed as arbitrary.
  * How to include an **Architectural & Clinical Justification column** right inside your model specification table (Table 9).
  * How to pre-empt the #1 NLP reviewer rejection (*unfair baselines*) by enforcing a unified hyperparameter/hardware setup across 5-fold CV $\times$ 5 random seeds (25 runs) with parametric ($t$-test) and non-parametric (Wilcoxon) significance testing.
  * How to prioritize **error costs** for the end user (reducing False Negative Rates on suicidal ideation) and present a **Qualitative Error Analysis** table (Table 19).
  * *Bonus Self-Critique:* Spot where our own prose used too many intensifiers (*"heavily," "flawlessly"*) and learn why cutting unmeasurable adjectives makes your paper stronger.

---

### Level 4: Generative Mathematical Formulation, Ablations & Compute Democratization
📄 **File:** [`3_DR-LDS_TEACHING_EDITION.pdf`](./3_DR-LDS_TEACHING_EDITION.pdf)  
* **Paper:** *Class balanced diabetic retinopathy image synthesis using a latent diffusion framework (DR-LDS)* (*Discover Artificial Intelligence*, Springer Nature, 2026)
* **Total Annotations:** 117 marks
* **What You Will Learn:**
  * How to write a formal **Problem Formulation (Section 3.1)** that mathematically explains *why* cross-entropy loss fails under severe class imbalance.
  * How to justify every preprocessing step by its physical/signal principle (e.g., why Ben Graham’s Gaussian blur subtraction separates low-frequency lighting drift from high-frequency microaneurysms).
  * How to defend domain-adapted fine-tuning (why natural-image VAEs smooth away microscopic medical lesions).
  * How to design the **essential control experiment for any generative augmentation paper**: comparing your synthesizer not just against an unaugmented baseline, but against **Classical Augmentation at the exact same target dataset size ($N = 2000$ per class)**.
  * How to frame results along a multi-dimensional **Pareto front** (generation fidelity via FID/KID + parameter budget + time per epoch + VRAM footprint) and rank your study's limitations honestly in the Discussion.

---

## ✅ The Master Pre-Submission Checklist (Distilled from 476 Marks)

Before submitting your next paper, verify that your manuscript passes these 6 structural checks:

### 1. The "Gap $\rightarrow$ Fix $\rightarrow$ Verify" Chain
- [ ] Does your Literature Review end with a critical synthesis of *methodological weaknesses* rather than just stopping after the last summarized paper?
- [ ] Does every numbered gap in your Introduction map 1-to-1 to a methodological component in Section 3?
- [ ] Does every bulleted contribution in your Introduction map to a specific table, figure, or ablation experiment in Section 4?

### 2. Data Provenance & Zero-Leakage Proof
- [ ] Did you state *why* you chose your dataset(s) and include a "Primary Utility" or "Dataset Card" table?
- [ ] Was the train/validation/test split performed **before** any preprocessing, scaling, oversampling, VAE fine-tuning, or generative augmentation?
- [ ] If using multi-image clinical data, did you split by **patient/lesion ID** (`GroupKFold`) rather than randomly by image?
- [ ] Were all scalers (`Fit` vs. `Transform`), hyperparameter grids, and threshold sweeps confined strictly to the training/validation folds?

### 3. Defensive Table & Figure Design
- [ ] Does your **Literature Review Table** include columns for `Validation Strategy` and `Major Limitations`?
- [ ] Does your **Architecture / Hyperparameter Table** include a `Justification` column explaining *why* each module or baseline was chosen?
- [ ] Do your **Figure Captions** state the takeaway message and walk through the stages (so a skimming reviewer can understand the paper from the figures and tables alone)?
- [ ] Does the order of subsections in Section 3 (Methodology) match the exact visual flow of Figure 1?

### 4. Fair Baselines & Controls
- [ ] Were competing baselines trained and evaluated under the **exact same data splits, random seeds, and preprocessing** (whenever comparing dataset-dependent metrics like FID or accuracy)?
- [ ] If proposing a generative data augmentation method, did you include an **equal-volume classical augmentation baseline** to prove gains come from generative diversity rather than sheer sample count?
- [ ] Did you report both **general metrics** (Accuracy, F1, AUC) and **imbalance/clinical-cost metrics** (MCC, AUPRC, QWK, False Negative Rate, or raw FP/FN counts)?

### 5. Interpretability (XAI) & Error Analysis
- [ ] Did you report what XAI **found** in the Abstract, rather than just stating that SHAP/LIME/Grad-CAM was used?
- [ ] Did you validate XAI outputs against **domain knowledge** (e.g., WHO guidelines, clinical biomarkers, or quantitative IoU/Dice overlap with lesion masks)?
- [ ] Did you include a **Failure Mode / Qualitative Error Analysis** explaining *why* and *where* the model fails?

### 6. Calibrated Tone & Reproducibility
- [ ] Did you remove unbacked, hyperbolic adjectives (*"flawlessly," "unprecedented," "massively"*) and hedge priority claims (*"To the best of our knowledge..."*)?
- [ ] Are your Limitations specific to your data and architecture (e.g., demographic skew, 2D vs. 3D, inference latency, single-split variance) rather than generic?
- [ ] Are your random seeds, hardware profile, dataset links, and source code/weights publicly archived?

---

## 📖 Citation

If you find these Teaching Editions or the underlying frameworks helpful in your research or lab training, please consider citing the original papers:

```bibtex
@article{alam2026glioma,
  title={A precise ensemble machine learning framework for improved glioma grading and classification with explainable AI},
  author={Alam, Touhid and Rahman, Md Mahmudur and Shimla, Sumaiya Sarkar and Uddin, Jalal and Rahman, Mahfujur and Mridha, M. F.},
  journal={Computer Methods and Programs in Biomedicine Update},
  volume={10},
  pages={100265},
  year={2026},
  publisher={Elsevier},
  doi={10.1016/j.cmpbup.2026.100265}
}

@article{rahman2026mheabert,
  title={MH-EABERT: an adaptive fusion approach with emotion knowledge-enhanced BERT for explainable mental health sentiment analysis from social media},
  author={Rahman, Sayedur and Alam, Touhid and Morol, Md Kishor and Nandi, Dip and Liew, Tze Hui},
  journal={Scientific Reports},
  year={2026},
  publisher={Nature Publishing Group},
  doi={10.1038/s41598-026-78247-1}
}

@article{alam2026drlds,
  title={Class balanced diabetic retinopathy image synthesis using a latent diffusion framework},
  author={Alam, Touhid and Liew, Tze Hui and Morol, Md. Kishor and Nandi, Dip and Jubair, Md. Abdullah-Al and Rahman, Mashiour},
  journal={Discover Artificial Intelligence},
  volume={6},
  pages={1205},
  year={2026},
  publisher={Springer Nature},
  doi={10.1007/s44163-026-02184-1}
}

@article{alam2026ganaskinai,
  title={GANA-SkinAI: A Multi-Stage Generative Framework for Explainable and Interpretable Skin Cancer Classification},
  author={Alam, Touhid and Hamim, Sultanul A. and Hossen, Md. Jakir and Mridha, M. F.},
  journal={Preprint submitted to Elsevier},
  year={2026}
}
