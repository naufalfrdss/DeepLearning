# 🧠 UTS Deep Learning - Telkom University

Repositori ini berisi tugas Ujian Tengah Semester (UTS) untuk mata kuliah Deep Learning. Di dalamnya terdapat dua bagian utama:

## 📁 Folder: `RegresiUTSTelkom`

Berisi proyek **regresi dan klasifikasi tabular** menggunakan Multi-Layer Perceptron (MLP). Terdapat dua notebook utama:

### 1. `Regresi_MLP_Model.ipynb`
- Fokus pada **model regresi** menggunakan arsitektur deep learning (MLP).
- Dataset terdiri dari data tabular dengan target numerik.
- Proses:
  - Pra-pemrosesan data: filter varian rendah, scaling, outlier removal.
  - Model MLP dengan evaluasi MSE, RMSE, dan R².
- Output:
  - Model untuk prediksi nilai kontinu.
  - Visualisasi prediksi vs aktual.

### 2. `Regresi(MLP)_dan_Klasifikasi.ipynb`
- Kombinasi **regresi** dan **klasifikasi**.
- Proses:
  - Target regresi dibagi ke dalam target klasifikasi biner (binerisasi).
  - Digunakan **SMOTE** untuk menangani data imbalance.
  - Hyperparameter tuning dengan **Keras Tuner (Hyperband)** untuk model klasifikasi.
- Evaluasi:
  - Regresi: MSE, RMSE, R².
  - Klasifikasi: Accuracy, Precision, Recall, F1-Score.

---

## 📁 Folder: `FishImageDataset`

Berisi model klasifikasi **gambar ikan** menggunakan CNN.

### 1. `CNN_Model_Klasifikasi.ipynb`
- Dataset berupa gambar berbagai jenis ikan.
- Arsitektur menggunakan Convolutional Neural Network (CNN).
- Proses:
  - Preprocessing gambar.
  - Data Augmentation.
  - CNN training dan evaluasi.
- Evaluasi:
  - Akurasi per kelas.
  - Confusion matrix dan visualisasi prediksi.
