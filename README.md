# projectcapstone-CC26-PSU013-dashboard
# ♻️ Trashkara — Dashboard Analisis Data Sampah Rumah Tangga

Dashboard interaktif untuk menganalisis data klasifikasi sampah rumah tangga Indonesia, dibangun menggunakan **Python** dan **Streamlit**.

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://your-app-link.streamlit.app)
&nbsp;
![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.35.0-FF4B4B?logo=streamlit&logoColor=white)

---

## 📌 Deskripsi Proyek

**Trashkara** adalah proyek Data Science yang berfokus pada analisis dan klasifikasi sampah rumah tangga di Indonesia. Dashboard interaktif ini menyajikan eksplorasi data, analisis statistik, serta feature engineering terhadap dataset sampah yang mencakup kategori **Organik**, **Anorganik**, dan **B3 (Bahan Berbahaya & Beracun)**.

Dataset berisi **14.100 baris data** dari **47 jenis sampah** unik, dilengkapi informasi emisi karbon, waktu urai, potensi daur ulang, dan nilai ekonomi masing-masing komoditas.

### ❓ Pertanyaan Bisnis yang Dijawab

1. **Emisi CO₂e** — Kategori sampah mana yang menyumbang rata-rata emisi tertinggi, dan apakah tingkat kesulitan daur ulang berkorelasi signifikan dengan besarnya emisi? *(Uji Spearman, α=0.05)*
2. **Beban Biaya** — Apakah ada pola struktural dalam beban biaya operasional pengelolaan sampah antar kategori?
3. **A/B Testing** — Apakah metode pengumpulan terstruktur (Bank Sampah / TPS 3R) menghasilkan cost burden yang lebih rendah secara signifikan dibanding metode konvensional? *(Uji Mann-Whitney U, α=0.05)*

---

## 🖥️ Preview Dashboard

| Halaman | Isi |
|---|---|
| 🏠 **Overview** | KPI cards, distribusi kategori, proporsi urai & daur ulang |
| 🌿 **Q1 — Emisi CO₂e** | Box plot, bar chart ±SE, violin plot, uji Spearman, top 15 sampah |
| 💰 **Q2 — Beban Biaya** | Stacked bar, heatmap, scatter plot, tabel high-cost burden |
| 🔬 **Feature Engineering** | Radar chart, bubble chart, histogram fitur komposit |
| 🧪 **A/B Testing** | Histogram & boxplot perbandingan grup, uji Mann-Whitney U |

---

## 📊 Fitur Dashboard

- 🔍 **Filter Interaktif** — Filter berdasarkan kategori, tingkat kesulitan, metode pengumpulan, dan rentang emisi CO₂e
- 🌿 **Analisis Emisi** — Distribusi dan korelasi emisi CO₂e dengan kesulitan daur ulang
- 💰 **Struktur Biaya** — Pola beban biaya operasional per kategori dan jenis sampah
- 🔬 **Fitur Komposit** — Skor `env_impact_score`, `econ_burden_score`, dan `recyclability_index`
- 🧪 **Uji Hipotesis** — A/B Testing efektivitas metode pengumpulan sampah
- 📋 **Data Dictionary** — Kamus data lengkap seluruh kolom dataset

---

## 🧰 Library yang Digunakan

| Library | Versi | Kegunaan |
|---|---|---|
| `streamlit` | 1.35.0 | Framework dashboard interaktif |
| `pandas` | 2.0.0 | Manipulasi dan analisis data |
| `numpy` | 1.24.0 | Komputasi numerik |
| `plotly` | 5.15.0 | Visualisasi interaktif |
| `matplotlib` | 3.7.0 | Visualisasi statis |
| `seaborn` | 0.12.0 | Visualisasi statistik |
| `scipy` | 1.11.0 | Uji statistik (Spearman, Mann-Whitney) |
| `scikit-learn` | 1.3.0 | Feature engineering & preprocessing |
| `openpyxl` | 3.1.0 | Baca/tulis file Excel |

---

## 📂 Struktur Proyek

```
Trashkara_DataScience/
│
├── dashboard_trashkara/
│   ├── dashboard.py                          # Aplikasi utama Streamlit
│   └── data/
│       ├── dataset_trashkara_dirty.xlsx      # Dataset mentah (raw)
│       ├── dataset_trashkara_dirty.csv       # Dataset mentah (CSV)
│       ├── dataset_trashkara_clean.csv       # Setelah data cleaning
│       ├── dataset_trashkara_transformed.csv # Setelah transformasi
│       ├── dataset_trashkara_model_ready.csv # Siap modeling (fitur komposit)
│       └── data_dictionary.csv              # Kamus data
│
├── data/                                    # Salinan dataset untuk notebook
├── trashkara_data_science_notebook.ipynb    # Notebook analisis lengkap
├── requirements.txt                         # Dependensi Python
└── README.md
```

---

## ▶️ Cara Menjalankan

**1. Clone repository**
```bash
git clone https://github.com/<username>/Trashkara_DataScience.git
cd Trashkara_DataScience
```

**2. Install dependensi**
```bash
pip install -r requirements.txt
```

**3. Jalankan dashboard**
```bash
cd dashboard_trashkara
streamlit run dashboard.py
```

Dashboard akan terbuka otomatis di browser pada `http://localhost:8501`

---

## 👥 Tim

**CC26-PSU013** — Data Science Track 2026
