# Hi, I'm Evans Kizito 👋
## Data Science & Analytics Portfolio

Selamat datang di repositori portofolio saya! Di sini saya mendokumentasikan perjalanan saya dalam Data Science, mencakup proyek kompetisi (lomba), riset, dan tugas akademis.

Saya memiliki ketertarikan khusus pada Machine Learning, NLP, Time Series, Computer Vision dan berpengalaman menggunakan **Python & R**.

---

## 🛠️ Tech Stack & Tools

* **Languages:** Python, R, SQL
* **Libraries:** Pandas, NumPy, Scikit-learn, TensorFlow/PyTorch, Matplotlib, Seaborn
* **Tools:** Jupyter Notebook, Google Colab, Tableau/PowerBI, LaTeX

---

### 1. ANFORCOM DDSC 2025 - Hybrid Low-Parameter Models for Asta Cita Topics
> **Pencapaian:** 🥉 Juara 3 (3rd Place)

* **Deskripsi Masalah:**
    Membangun model klasifikasi teks multi-kelas untuk mengategorikan opini publik terkait "Asta Cita" (8 pilar pembangunan Indonesia Emas 2045) dari media sosial[cite: 3, 12]. Tantangan utama adalah dataset yang sangat *imbalanced* (kelas minoritas seperti 'Hilirisasi' hanya 3.6%) dan *noisy* (bahasa tidak baku, campuran bahasa daerah, dan *truncated text*)[cite: 70, 71, 73, 104].

* **Pendekatan/Metode:**
    Kami menerapkan pendekatan *Data-Centric AI* dan *Hybrid Modeling*:
    * **Data Cleaning:** Menggunakan **Cleanlab (Confidence Learning)** untuk mendeteksi dan membersihkan label yang salah (noisy labels) pada data latih secara otomatis.
    * **Augmentation:** Menerapkan **Pseudo-Labeling** pada data tes dengan *confidence* tinggi untuk memperkaya data latih[cite: 45, 322].
    * **Modeling:** Menggunakan arsitektur Hybrid **IndoBERT-Tweet (Fine-tuned)** yang di-ensemble dengan Logistic Regression (Weighted Average 0.7:0.3)[cite: 60, 315].
    * **Imbalance Handling:** Menggunakan **Focal Loss** dan **Stratified K-Fold** untuk meningkatkan performa pada kelas minoritas[cite: 53, 356].

* **Hasil/Insight:**
    * [cite_start]Model berhasil meningkatkan **Balanced Accuracy** secara drastis dari **55.3% (Baseline)** menjadi **95.1% (Final Model)**[cite: 395].
    * [cite_start]Macro F1-Score mencapai **0.954**, membuktikan model mampu mengenali topik minoritas (seperti Hilirisasi dan Pemerataan) dengan sangat baik meskipun datanya sedikit[cite: 395, 487].
    * [cite_start]Sistem ini dapat digunakan pemerintah untuk monitoring isu prioritas secara *real-time*[cite: 501].

🔗 **Links:**
| 📒 Notebook | 📄 Makalah/Slide (PDF) | 📂 Dataset |
| :---: | :---: | :---: |
| [View Notebook]([mode_pesawat_UniversitasIndonesia.ipynb](https://colab.research.google.com/drive/1XyMuCd5p3tSz7D6tsvoMZsDvFjM5TJbs?usp=sharing)) | [View Presentation](./ANFORCOM_2025/modepesawat_ppt.pdf) | [Dataset Source](link_jika_ada) |

---

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
