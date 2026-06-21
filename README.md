# Sistem Case-Based Reasoning (CBR) untuk Analisis Putusan Tindak Pidana Korupsi

## Deskripsi Proyek

Proyek ini bertujuan membangun sistem Case-Based Reasoning (CBR) sederhana untuk membantu pencarian putusan tindak pidana korupsi yang memiliki kemiripan dengan kasus baru.

Data yang digunakan berasal dari Direktori Putusan Mahkamah Agung Republik Indonesia dengan domain perkara Tindak Pidana Korupsi (Tipikor).

Sistem mengikuti siklus Case-Based Reasoning (CBR), yaitu:

1. Membangun Case Base
2. Case Representation
3. Case Retrieval
4. Case Solution Reuse
5. Model Evaluation

---

## Dataset

- Domain Perkara: Tindak Pidana Korupsi (Tipikor)
- Jumlah Putusan: 40 Putusan
- Sumber Data: Direktori Putusan Mahkamah Agung Republik Indonesia

---

## Struktur Repository

```text
CBR-Putusan-Korupsi/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   ├── case_001.txt
│   │   ├── case_002.txt
│   │   ├── case_003.txt
│   │   └── ...
│   │
│   ├── processed/
│   │   └── cases.csv
│   │
│   ├── eval/
│   │   ├── queries.json
│   │   ├── retrieval_metrics.csv
│   │   └── prediction_metrics.csv
│   │
│   └── results/
│       └── predictions.csv
│
├── logs/
│   └── cleaning.log
│
└── notebooks/
    ├── 01_case_base.ipynb
    ├── 02_case_representation.ipynb
    ├── 03_case_retrieval.ipynb
    ├── 04_predict.ipynb
    └── 05_evaluation.ipynb
```

## Instalasi

1. Clone repository:

```bash
git clone <url_repository>
cd CBR-Putusan-Korupsi
```

2. Install dependensi:

```bash
pip install -r requirements.txt
```

## Tahapan Pengerjaan

### 1. Membangun Case Base

Melakukan:
- Konversi PDF ke TXT
- Pembersihan teks
- Normalisasi dokumen

Output:

```text
data/raw/
```

### 2. Case Representation

Ekstraksi informasi penting:

- Nomor perkara
- Pasal
- Terdakwa
- Amar putusan
- Teks putusan

Output:

```text
data/processed/cases.csv
```

### 3. Case Retrieval

Menggunakan:
- TF-IDF Vectorizer
- Cosine Similarity

Untuk menemukan putusan yang paling mirip dengan query kasus baru.

### 4. Case Solution Reuse

Mengambil amar putusan dari kasus-kasus yang paling mirip sebagai rekomendasi solusi.

### 5. Evaluasi Model

Metrik evaluasi:

- Accuracy
- Precision
- Recall
- F1-Score

Output:
```text
data/eval/retrieval_metrics.csv
data/eval/prediction_metrics.csv
```

## Cara Menjalankan

Jalankan notebook secara berurutan:

```text
01_case_base.ipynb
↓
02_case_representation.ipynb
↓
03_case_retrieval.ipynb
↓
04_predict.ipynb
↓
05_evaluation.ipynb
```
