# Chapter 19: Training and Deploying at Scale

## 1. Tantangan Skala Besar
- Dataset besar → perlu efisiensi IO dan GPU
- Model besar → butuh memori efisien & distribusi training

## 2. `tf.data` for Performance
- `.prefetch()` dan `.cache()` untuk efisiensi loading
- `.interleave()` untuk paralel baca multi file

## 3. Mixed Precision
- Kombinasi float16 & float32
- Mempercepat training dengan GPU modern (NVIDIA TensorCore)
- Harus hati-hati untuk layer output dan numerik stabilitas

## 4. Distributed Training
### a. `MirroredStrategy`
- Train di banyak GPU
### b. `MultiWorkerMirroredStrategy`
- Train di banyak mesin
### c. `TPUStrategy`
- Train di TPU

## 5. Deployment
### a. TensorFlow SavedModel
- Format model diserialisasi → `.pb`, `assets/`, `variables/`

### b. TensorFlow Serving
- Gunakan `tensorflow_model_server` untuk REST/gRPC API
- Sangat cocok untuk deployment real-time di produksi

## 6. Deployment Alternatif
- TFLite: untuk edge device/mobile
- TF.js: untuk browser
- TF Hub: untuk berbagi model

## 7. Alur Produksi
1. Latih model
2. Evaluasi & simpan model
3. Sajikan dengan REST API (TF Serving / Flask)
4. Pantau performa → retrain bila perlu
