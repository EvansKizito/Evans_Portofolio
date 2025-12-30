# Hi, I'm Evans Kizito 👋
## Data Science & Analytics Portfolio

Welcome to my portfolio repository! Here, I document my journey in Data Science, covering data competitions, research, and academic projects.

I have a strong interest in **Machine Learning, NLP, Time Series, and Computer Vision**, with hands-on experience using **Python & R**.

---

## 🛠️ Tech Stack & Tools

* **Languages:** Python, R, SQL
* **Libraries:** Pandas, NumPy, Scikit-learn, TensorFlow/PyTorch, Matplotlib, Seaborn
* **Tools:** Jupyter Notebook, Google Colab, Tableau/PowerBI, LaTeX

---

### 1. ANFORCOM DDSC 2025 - Hybrid Low-Parameter Models for Asta Cita Topics
> **Achievement:** 🥉 3rd Place Winner

* **Problem Description:**
    Developed a multi-class text classification model to analyze public sentiment regarding "Asta Cita" (the 8 development pillars of Indonesia's Golden Era 2045) on social media. The primary challenges were a highly **imbalanced dataset** (minority classes like 'Hilirisasi' accounted for only 3.6%) and **noisy data** (slang, mixed local languages, and truncated text).

* **Approach & Methodology:**
    We adopted a **Data-Centric AI** and **Hybrid Modeling** strategy to address data scarcity and noise:
    * **Data Cleaning:** Implemented **Cleanlab (Confidence Learning)** to automatically detect and correct noisy labels in the training set.
    * **Augmentation:** Applied **Pseudo-Labeling** to high-confidence test samples to expand the training data.
    * **Modeling:** Engineered a Hybrid Architecture combining a **Fine-tuned IndoBERT-Tweet** model with Logistic Regression (Weighted Ensemble 0.7:0.3).
    * **Imbalance Handling:** Utilized **Focal Loss** and **Stratified K-Fold Cross-Validation** to optimize performance on minority classes.

* **Results & Insights:**
    * Successfully improved **Balanced Accuracy** from a baseline of **55.3%** to **95.1%** in the final model.
    * Achieved a **Macro F1-Score of 0.954**, proving the model's robustness in detecting minority topics (e.g., Downstreaming/Hilirisasi) despite limited data.
    * The solution provides a reliable tool for the government to monitor strategic issues in real-time.

🔗 **Links:**
| 📒 Notebook | 📄 Paper/Slides (PDF) | 📂 Dataset |
| :---: | :---: | :---: |
| [View Notebook](https://colab.research.google.com/drive/1XyMuCd5p3tSz7D6tsvoMZsDvFjM5TJbs?usp=sharing) | [View Presentation](DDSCUNDIP.pdf) | [Dataset Source](https://www.kaggle.com/competitions/penyisihan-ddsc25/data) |

---

### 2. Gelar Rasa 2025 - FMCG Sales Forecasting & Cannibalization Analysis
> **Achievement:** *Top 10*

* **Problem Description:**
    Addressed the challenge of forecasting sales for FMCG Personal Care products while analyzing market dynamics. The primary goal was to predict future sales trends and investigate **product cannibalization**—determining if new product launches negatively impacted the sales of existing products in the same category.

* **Approach & Methodology:**
    Developed a robust Multivariate Time Series pipeline using **VAR (Vector Autoregression)** and **VECM (Vector Error Correction Model)** to capture interdependencies between products.
    * **Feature Engineering:** Aggregated daily revenue and integrated **Sentiment Analysis (VADER)** from customer reviews as exogenous variables.
    * **Rigorous Statistical Testing:** Conducted Stationarity tests (ADF & KPSS), Lag Length selection (AIC/BIC), and **Johansen Cointegration Test** to determine the optimal model (VAR vs. VECM).
    * **Causal Inference:** Applied **Granger Causality** tests to statistically validate cannibalization effects between new and old products.
    * **Dynamic Analysis:** Utilized **Impulse Response Functions (IRF)** and **Forecast Error Variance Decomposition (FEVD)** to simulate market shocks and understand variance contributions.

* **Results & Insights:**
    * Successfully built a forecasting engine capable of predicting sales for the next 30 days with stability checks (Eigenvalue analysis).
    * Identified significant causal relationships suggesting cannibalization, providing actionable insights for portfolio optimization.
    * The model offered a strategic "Innovation Radar" to pinpoint high-growth products versus those in decline.

🔗 **Links:**
| 📒 Notebook | 📄 Case Booklet | 📂 Dataset |
| :---: | :---: | :---: |
| [View Code](RQ2_VAR_VECM_Complete_Implementation.ipynb) | [Read Case Study](STUDYCASEGELAR.pdf) | [Dataset Source](bit.ly/DatasetDSCGelarRasa2025) |

---

### 3. GammaFest IPB 2025 – Citation Network Link Prediction  
> **Achievement:** 🏅 Top 5 Finalist

**Problem Description**  
This competition focused on building a **link prediction model** to identify citation relationships between research papers within a **citation network**. The main challenges included **highly-imbalanced labels** and the need to capture **semantic similarity across documents** to support an intelligent scientific literature recommendation system. Model performance was evaluated using the **Matthews Correlation Coefficient (MCC)**.

**Approach & Methodology**  
We designed a pipeline integrating **document representation, similarity-based feature engineering, and gradient-boosting classifiers**:

- **Document Embedding:**  
  Doc2Vec for *full-text documents*, and **FastText & SPECTER (BERT-based)** for *titles and concepts* to capture academic semantic meaning more effectively.
- **Vector & Similarity Features:**  
  Cosine / Euclidean / Manhattan / Pearson similarity, enriched with **vector-difference statistics and angular projection features** to represent inter-document relationships.
- **Temporal Feature Engineering:**  
  Publication-year difference was added to model **chronological citation dynamics**.
- **Modeling:**  
  We conducted multi-model experiments and selected **CatBoost (tuned)** with the combined feature set  
  **Doc2Vec + FastText + SPECTER + FE Metadata + FE Vector Embeddings** as the best-performing model.

**Results & Insights**
- The final model achieved **MCC = 0.568** on a highly-imbalanced dataset.
- The combination of **semantic embeddings and engineered similarity features** provided a significant improvement over TF-IDF baselines.
- The pipeline is **computationally efficient**, while still opening opportunities for future enhancements using **Graph Neural Networks (GNNs)** to better exploit global citation-graph structure.

🔗 **Links**
| 📒 Notebook | 📄 Paper (PDF) | 🎥 Presentation (Slides) |
| :---: | :---: | :---: |
| [Notebook](main.ipynb) | [Competition Report](DSC25125_Manusia%20Pojok_Laporan.pdf) | [Presentation Slides](DSC25125_Manusia%20Pojok_Presentasi.pdf) |

---

### 4. DSC LOGIKA UI 2025 – Nusantara Traditional House Image Classification  
> **Achievement:** 🥇 Ranked #1 in Qualification Round (Highest Macro F1-Score)  
> *(Did not place in the final round due to an incomplete submission report — valuable learning experience in competition delivery & documentation.)*

**Problem Description**  
This competition challenged participants to build a **computer vision model** capable of classifying images of Indonesian traditional houses across multiple cultural regions. The dataset contained thousands of images with variations in lighting, viewpoint, occlusion, and class imbalance. Models were evaluated using **Macro F1-Score**, prioritizing balanced performance across all classes.

**Approach & Methodology**  
Our solution adopted a **Deep Learning + data-centric pipeline** with strong emphasis on dataset integrity and robustness:

- **Pre-processing & Data Cleaning:**  
  Near-duplicate removal using **Perceptual Hashing (pHash)**, cross-class conflict filtering, and **train–test leakage prevention** to ensure fair generalization.  
- **Augmentation & Regularization:**  
  Albumentations pipeline, **MixUp**, Label Smoothing, and **class-balanced sampling** to improve minority-class representation.  
- **Modeling:**  
  Fine-tuning **EVA-02 (Vision Transformer family, ViT-based)** with **Focal Loss**, Stratified 5-Fold Cross-Validation, and **mean-ensemble inference**.
- **Why EVA-02?**  
  Strong global feature representation, robustness to visual variation, and superior performance compared to CNN baselines (EfficientNet, ConvNeXt, Swin).

**Results & Insights**
- Achieved **the highest Macro F1-Score in the qualification round**, ranking **1st place on the leaderboard**.
- Demonstrated significant improvement over baseline CNN models through **smart cleaning + transformer-based modeling**.
- The final round submission did not score due to an **incomplete report file**, highlighting the importance of **end-to-end competition rigor (model + documentation + delivery)** — a key professional takeaway.

🔗 **Links**
| 📒 Notebook / Code | 📄 Qualification Report (PDF) | 🎥 Presentation Slides |
| :---: | :---: | :---: |
| [Notebook](DSC0075_wets%20belom%20dicoba_Notebook.ipynb) | [Technical Report](DSC0075_wets%20belom%20dicoba_LaporanAkhir(1).pdf) | [Final Presentation](DSC0075_wets%20belom%20dicoba_Presentasi%20(1).pdf) |

---

## 📫 Contact Me

Jika Anda ingin berdiskusi tentang proyek ini atau peluang kolaborasi, silakan hubungi saya:

* **LinkedIn:** [Link LinkedIn Kamu]
* **Email:** [Email Kamu]
* **Portfolio Website:** [Link jika ada]

---
*Repository ini diperbarui secara berkala.*
