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
...
```

## Instalasi

Install seluruh dependensi:

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

---

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
