# Chapter 7: Ensemble Learning and Random Forests

## 1. Apa itu Ensemble?
Menggabungkan beberapa model lemah → satu model kuat.  
Dasar: agregasi prediksi = hasil lebih baik dari prediksi tunggal.

## 2. Voting Classifier
### a. Hard Voting
- Mayoritas suara
### b. Soft Voting
- Rata-rata probabilitas (butuh classifier dengan `predict_proba()`)

## 3. Bagging (Bootstrap Aggregating)
- Melatih model di subset data yang di-*resample*
- Tujuan: mengurangi *variance* model
- **Out-of-Bag (OOB)**: evaluasi model pada data yang tidak ikut dilatih

## 4. Random Forest
- Ensemble dari Decision Tree
- Subset acak fitur di tiap split → dekorrelasi antar tree
- **Feature importance**: digunakan untuk seleksi fitur

## 5. Boosting
### a. AdaBoost
- Fokus pada instance yang salah diklasifikasikan sebelumnya
- Memberi bobot lebih tinggi pada error instance

### b. Gradient Boosting
- Setiap model baru dilatih untuk mengurangi residual kesalahan dari model sebelumnya

## 6. Stacking
- Meta-learner dilatih untuk menggabungkan prediksi dari base-learner
- Biasanya base: berbagai algoritma; meta: regresi/logistic/regressor/tree ringan

## 7. Ringkasan
| Teknik      | Tujuan         | Risiko         |
|-------------|----------------|----------------|
| Bagging     | Reduce variance | Bias bisa tinggi |
| Boosting    | Reduce bias     | Overfitting (high variance) |
| Random Forest | Reduce variance & decorrelate | Model besar |
