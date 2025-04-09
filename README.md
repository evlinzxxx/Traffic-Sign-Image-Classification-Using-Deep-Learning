# Traffic Sign Image Classification Using CNN

#### 1. **Pengambilan Dataset**
- Dataset: [GTSRB (German Traffic Sign Recognition Benchmark)](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign) dari Kaggle  
- Total: **>50.000 gambar** dari **43 kelas rambu lalu lintas**
- Dataset memenuhi syarat **jumlah minimal 1.000 gambar** dan **belum pernah digunakan di latihan sebelumnya**

#### 2. **Pra-Pemrosesan Gambar**
- Gambar dikonversi ke ukuran **30x30 piksel**
- Dataset dibagi menjadi **Training (80%)** dan **Testing (20%)**
- Label dikonversi menjadi **one-hot encoding** untuk klasifikasi multi-kelas

#### 3. **Membangun Model CNN**
- Menggunakan arsitektur **Sequential**, terdiri dari:
  - **Conv2D**
  - **MaxPooling2D**
  - **Dropout**
  - **Dense Layer**
- Model dikompilasi dengan `categorical_crossentropy` dan optimizer **Adam**

#### 4. **Training Model**
- Model dilatih selama maksimum 35 epoch
- Dihentikan lebih awal otomatis setelah mencapai **akurasi 96% pada training**
- Visualisasi training dan validation: **akurasi & loss** ditampilkan dalam grafik

#### 5. **Evaluasi Model**
- Model diuji pada dataset testing dari GTSRB (`Test.csv`)
- Akurasi akhir pada test set: **95.87%**

#### 6. **Menyimpan Model**
Model disimpan dalam **tiga format**:
- `SavedModel` → Untuk deployment di server/cloud
- `TF-Lite` → Untuk perangkat mobile
- `TFJS` → Untuk digunakan di web dengan TensorFlow.js

###  Kesimpulan
Model CNN yang dibangun mampu mengklasifikasikan rambu lalu lintas dengan akurasi tinggi. Proyek ini menunjukkan penerapan Computer Vision dalam domain lalu lintas yang potensial untuk dikembangkan ke sistem navigasi, edukasi pengemudi, dan kendaraan otonom.

##### Proyek Final Belajar Pengembangan Machine Learning
