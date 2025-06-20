
# 🏡 California Housing Price Prediction

Proyek ini bertujuan membangun model prediksi harga rumah di California berdasarkan data demografis dan geografis. Model yang digunakan adalah **XGBoost Regressor** yang telah dituning dan dilengkapi dengan fitur polinomial derajat 3 untuk meningkatkan akurasi prediksi.

---

## 🔍 Tujuan Proyek

- Memprediksi harga rumah berdasarkan fitur seperti `median_income`, `longitude`, `latitude`, dan `ocean_proximity`.
- Menemukan fitur paling berpengaruh terhadap harga rumah.
- Memberikan **insight bisnis** bagi developer dan agen properti untuk pengambilan keputusan strategis.

---

## 📁 Struktur File

```
.
├── Capstone Module 3_California Housing Price.ipynb  # Notebook utama
├── Model_California_XGB.sav                          # Model XGBoost awal
├── Model_California_XGB_Tuned.sav                    # Model setelah tuning
├── data_california_house.csv                         # Dataset mentah
├── california_housing_cleaned.csv                    # Dataset hasil pembersihan
├── README.md                                         # Dokumentasi proyek
```

---

## ⚙️ Model & Metodologi

- **Algoritma**: XGBoost Regressor  
- **Feature Engineering**:
  - Encoding untuk `ocean_proximity`
  - Scaling data numerik
  - Penambahan fitur interaksi dan polinomial derajat 3
- **Hyperparameter Tuning**: `RandomizedSearchCV`

### Evaluasi Model

- **MAE** (Mean Absolute Error): ± **$32.500**
- **R² Score**: ± **81%**
- Gap error kecil antara data latih dan uji → **Model tidak overfitting**

---

## 🔑 Fitur Paling Berpengaruh

- `median_income`
- Interaksi `longitude × median_income`
- `ocean_proximity`
- `longitude`, `latitude`

---

## 💡 Insight Bisnis

- 📌 **Penetapan Harga Akurat**  
  Prediksi harga berbasis data membantu menetapkan harga jual rumah yang kompetitif dan realistis.

- 📍 **Identifikasi Lokasi Strategis**  
  Menemukan wilayah dengan potensi harga tinggi, khususnya di pesisir barat seperti Los Angeles & San Francisco.

- 🎯 **Segmentasi Pasar Tepat Sasaran**  
  Produk properti dapat disesuaikan dengan daya beli konsumen di berbagai wilayah.

- 🚧 **Mitigasi Risiko Investasi**  
  Mencegah pembangunan di lokasi dengan mismatch harga dan pendapatan penduduk.

- 📢 **Optimasi Strategi Pemasaran**  
  Promosi bisa diarahkan ke segmen dan lokasi yang paling potensial.

---

## 📦 Cara Menjalankan Proyek

### 1. Clone Repository
```bash
git clone https://github.com/username/nama-repo.git
cd nama-repo
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Jalankan Notebook
```bash
jupyter notebook Capstone\ Module\ 3_California\ Housing\ Price.ipynb
```

---

## 🧠 Referensi

- Dataset: [California Housing — sklearn.datasets](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)  
- XGBoost Documentation: [https://xgboost.readthedocs.io](https://xgboost.readthedocs.io)  
- Scikit-learn: [https://scikit-learn.org](https://scikit-learn.org)
