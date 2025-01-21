# Deteksi-Dini-Depresi-dengan-4-Model-ML

## Latar Belakang
Depresi merupakan gangguan mental yang memengaruhi sekitar 280 juta orang di dunia pada tahun 2021, berdasarkan laporan WHO. Dampak dari depresi mencakup penurunan produktivitas, gangguan hubungan sosial, kesehatan fisik yang memburuk, dan bahkan risiko bunuh diri. Sayangnya, deteksi dini sering kali terhambat oleh stigma, subjektivitas dalam diagnosis klinis, dan akses terbatas ke layanan kesehatan mental.

Proyek ini bertujuan untuk mengatasi tantangan tersebut dengan menggunakan model klasifikasi berbasis kecerdasan buatan (AI) untuk mendeteksi dini gejala depresi. Dengan bantuan machine learning, solusi otomatis dapat memberikan skrining awal yang akurat dan mendukung sistem kesehatan mental, terutama di daerah dengan akses terbatas.

## Dataset
- **Sumber Data:** Kaggle ([Link Dataset](https://www.kaggle.com/datasets/anthonytherrien/depression-dataset))
- **Waktu Pengambilan:** 2023
- **Label Kolom:**
  - Age: 
  - Marital Status
  - Education Level
  - Number of Children
  - Smoking Status
  - Physical Activity Level
  - Employment Status
  - Income
  - Alcohol Consumption
  - Dietary Habits
  - Sleep Patterns
  - History of Substance Abuse
  - Family History of Depression
  - Chronic Medical Conditions
- **Persiapan Data:**
  - Memeriksa tipe data dan membersihkan nilai null.
  - Melakukan imputasi untuk nilai yang hilang (median untuk numerik dan modus untuk kategori).
  - Mengganti nama kolom agar lebih deskriptif.
  - Menampilkan matriks korelasi untuk menentukan hubungan antar variabel.

## Pemilihan Fitur
Berdasarkan analisis korelasi dan exploratory data analysis (EDA), fitur-fitur berikut dipilih sebagai input utama untuk model:
- `Age`: Usia memengaruhi kerentanan terhadap depresi.
- `Gender`: Faktor demografi ini memiliki hubungan dengan prevalensi depresi.
- `Education`: Tingkat pendidikan memengaruhi kemampuan seseorang dalam menghadapi tekanan hidup.
- `Mental_Health_History`: Faktor utama dalam mendeteksi risiko depresi.

Fitur-fitur ini menunjukkan relevansi yang signifikan terhadap `Depression_Score` dan dapat meningkatkan performa model dalam mendeteksi gejala depresi.

## Model Machine Learning
Proyek ini mengimplementasikan empat algoritma machine learning:
1. **Random Forest**
   - Model baseline untuk evaluasi awal.
   - Memiliki kemampuan menangani data dengan banyak variabel kategori dan numerik.

2. **Gradient Boosted Tree**
   - Memberikan performa terbaik dengan akurasi 91% setelah hyperparameter tuning.
   - Cocok untuk data dengan pola kompleks.

3. **Logistic Regression**
   - Algoritma klasik yang digunakan sebagai perbandingan dasar.

4. **Support Vector Machine (SVM)**
   - Efektif untuk dataset kecil dengan klasifikasi yang jelas.

### Evaluasi Model
Model dievaluasi menggunakan metrik berikut:
- **Silhouette Score:** valuasi seberapa baik hasil pengelompokan data.
- **Accuracy:** Seberapa baik akurasi tingkat depresi yang di tebak.

### Hyperparameter Tuning
Dua model terbaik, Random Forest dan Gradient Boosted Tree, dilakukan tuning untuk meningkatkan performa. Hasil tuning menunjukkan bahwa Gradient Boosted Tree adalah model terbaik dengan akurasi, dan Silhouette Score.

### Hasil Akhir
Random Forest : Accuracy = 0.69
Gradient Boosted Tree : Accuracy = 0.69 
K-Means : Silhouette Score = 0.79
Gaussian Mixture : Silhouette Score = 0.16

## Kesimpulan
Gradient Boosted Tree dan K-means dipilih sebagai solusi terbaik untuk mendeteksi dini gejala depresi dari dua kategori yaitu klasifikasi dan clustering. Model ini mampu menangkap pola kompleks dalam data dan memberikan akurasi tinggi. Proyek ini menunjukkan bahwa machine learning dapat berkontribusi signifikan dalam mendukung sistem kesehatan mental dengan menyediakan solusi deteksi dini yang praktis dan efisien.

