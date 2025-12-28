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
Kompetisi ini berfokus pada pembangunan model **link prediction** untuk memprediksi hubungan kutipan antar-paper dalam sebuah **citation network**. Tantangan utama terletak pada **ketidakseimbangan label** serta kebutuhan menangkap relasi semantik antar-dokumen secara akurat untuk mendukung sistem rekomendasi literatur ilmiah. Evaluasi model menggunakan **Matthews Correlation Coefficient (MCC)**.

**Approach & Methodology**  
Kami merancang pipeline berbasis **document representation + feature engineering + gradient boosting classifier**:

- **Document Embedding:**  
  Doc2Vec untuk *Full-Text*, serta **FastText & SPECTER (BERT-based)** untuk *Title & Concepts* agar makna semantik akademik dapat ditangkap lebih baik.
- **Vector & Similarity Features:**  
  Cosine / Euclidean / Manhattan / Pearson similarity, ditambah **vector-difference statistics & angular projection** untuk merepresentasikan relasi antar-dokumen.
- **Temporal Feature Engineering:**  
  Menambahkan **selisih tahun publikasi** sebagai fitur kronologis pola sitasi.
- **Modeling:**  
  Eksperimen multi-model dan menetapkan **CatBoost (tuned)** dengan kombinasi  
  **Doc2Vec + FastText + SPECTER + FE Metadata + FE Vector Embeddings** sebagai model terbaik.

**Results & Insights**
- Model terbaik mencapai **MCC = 0.568** pada dataset yang **highly-imbalanced**.
- Kombinasi **embedding + engineered similarity features** memberi peningkatan signifikan dibanding baseline TF-IDF.
- Pipeline terbukti **komputasi-efisien**, namun tetap membuka peluang pengembangan lanjutan menggunakan **Graph Neural Networks (GNN)** untuk memanfaatkan struktur jaringan sitasi secara lebih komprehensif.

🔗 **Links**
| 📒 Notebook | 📄 Paper (PDF) | 🎥 Presentation (Slides) |
| :---: | :---: | :---: |
| [Notebook](main.ipynb) | [Competition Report](DSC25125_Manusia%20Pojok_Laporan.pdf) | [Presentation Slides](DSC25125_Manusia%20Pojok_Presentasi.pdf) |

--

### 2. [Nama Lomba/Kompetisi] - [Judul Proyek]
> **Pencapaian:** *[Misal: Finalis Nasional]*

* **Deskripsi Masalah:**
    [Tulis deskripsi singkat di sini...]
* **Pendekatan/Metode:**
    [Tulis metode/algoritma yang digunakan di sini...]
* **Hasil/Insight:**
    [Tulis hasil akurasi atau insight bisnis di sini...]

🔗 **Links:**
- [📒 Jupyter Notebook](./path/to/notebook.ipynb)
- [📄 Makalah Lengkap (PDF)](./path/to/paper.pdf)

---

## 📚 Academic & Personal Projects (Tugas/Mandiri)

Berikut adalah proyek terpilih dari tugas kuliah dan eksplorasi mandiri.

### [Nama Mata Kuliah/Topik] - [Judul Tugas]
* **Deskripsi:** Penjelasan singkat tentang tugas atau objektif analisis.
* **Metode:** Algoritma atau teknik statistik yang digunakan.
* **Tech Stack:** Python (Pandas, Matplotlib).
* **Akses File:**
    * [Link ke Code/Notebook](./tugas1/analysis.ipynb)
    * [Link ke Laporan PDF](./tugas1/report.pdf)

---

## 📫 Contact Me

Jika Anda ingin berdiskusi tentang proyek ini atau peluang kolaborasi, silakan hubungi saya:

* **LinkedIn:** [Link LinkedIn Kamu]
* **Email:** [Email Kamu]
* **Portfolio Website:** [Link jika ada]

---
*Repository ini diperbarui secara berkala.*
