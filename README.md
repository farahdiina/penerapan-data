# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding
Jaya Jaya Institut adalah sebuah lembaga pendidikan tinggi yang telah beroperasi sejak tahun 2000 dan telah menghasilkan lulusan berkualitas yang berkontribusi di berbagai industri. Namun, dalam beberapa tahun terakhir, mereka menghadapi tantangan serius berupa tingginya tingkat dropout mahasiswa. Fenomena ini tidak hanya berdampak pada reputasi institusi, tetapi juga mempengaruhi stabilitas keuangan dan efektivitas program akademik. Salah satu faktor utama yang menyebabkan dropout adalah kesulitan akademik, masalah finansial, serta kurangnya keterlibatan mahasiswa dalam kegiatan akademik. Jika dropout tidak segera diidentifikasi dan dicegah, institusi akan kehilangan lebih banyak mahasiswa potensial, yang pada akhirnya dapat menurunkan tingkat kelulusan dan daya saing di dunia pendidikan. Untuk mengatasi permasalahan ini, Jaya Jaya Institut berupaya menerapkan pendekatan berbasis data dengan menggunakan model machine learning untuk memprediksi mahasiswa yang berisiko tinggi mengalami dropout. Dengan sistem prediksi ini, institusi dapat memberikan intervensi lebih awal, seperti bimbingan akademik, dukungan finansial, atau konseling untuk membantu mahasiswa tetap berada di jalur pendidikan mereka. Selain itu, dashboard analisis juga akan dikembangkan agar pihak administrasi dapat dengan mudah memantau dan memahami tren performa mahasiswa serta mengambil langkah strategis untuk meningkatkan retensi mahasiswa. Proyek ini bertujuan untuk mengembangkan sistem prediksi dropout yang akurat serta dashboard interaktif yang dapat membantu pihak manajemen dalam membuat keputusan berbasis data. Dengan solusi ini, diharapkan tingkat dropout dapat ditekan, sehingga lebih banyak mahasiswa dapat menyelesaikan pendidikan mereka dengan sukses.

### Permasalahan Bisnis
1. Berapa jumlah total mahasiswa yang terdaftar, dan bagaimana tingkat kelulusan mereka?
2. Bagaimana hubungan antara pendidikan sebelumnya dengan status mahasiswa (Graduate, Dropout, Enrolled)?
3. Sejauh mana biaya kuliah mempengaruhi status mahasiswa?
4. Bagaimana tingkat kehadiran mahasiswa di semester awal berkorelasi dengan status akademik mereka?
5. Bagaimana pengaruh beasiswa terhadap kemungkinan mahasiswa lulus, dropout, atau tetap terdaftar?
6. Bagaimana hubungan antara jumlah mata kuliah yang diambil di semester awal dengan nilai masuk mahasiswa?
7. Faktor apa saja yang paling mempengaruhi mahasiswa untuk bertahan hingga lulus dibandingkan dengan mereka yang dropout?

### Cakupan Proyek
1. Pengumpulan dan Pemahaman Data
   - Dataset tersedia dalam file data.csv.
   - Memahami struktur dan karakteristik data, termasuk tipe variabel, jumlah data, serta nilai yang hilang atau tidak valid.
2. Eksplorasi Data (Exploratory Data Analysis - EDA)
   - Melakukan analisis awal untuk mengidentifikasi pola, tren, dan distribusi data.
   - Visualisasi data menggunakan seaborn, matplotlib, dan plotly untuk memahami hubungan antar variabel serta mendeteksi anomali atau outlier.
3. Pembersihan dan Persiapan Data
   - Menangani nilai yang hilang dengan SimpleImputer menggunakan strategi yang sesuai.
   - Menghapus duplikasi data untuk memastikan keakuratan analisis.
   - Menggunakan Label Encoding untuk variabel kategorikal dan StandardScaler untuk menormalisasi data numerik.
4. Penanganan Ketidakseimbangan Data
   - Menggunakan teknik SMOTETomek untuk menangani ketidakseimbangan kelas dan meningkatkan kualitas model prediksi.
5. Seleksi Fitur
   - Menggunakan SelectFromModel dengan RandomForestClassifier untuk memilih fitur yang paling berpengaruh terhadap prediksi.
   - Menghapus fitur yang tidak memiliki kontribusi signifikan dalam meningkatkan akurasi model.
6. Pengembangan Model Prediksi
   - Membagi dataset menjadi data latih (train) dan data uji (validation) dengan train_test_split.
   - Menggunakan teknik Pipeline dan ColumnTransformer untuk preprocessing sebelum model dijalankan.
   - Membangun dan melatih model prediksi dengan algoritma Random Forest, Gradient Boosting, AdaBoost, SVM, dan SGDClassifier.
   - Menggunakan VotingClassifier untuk membangun model ensemble guna meningkatkan akurasi prediksi.
   - Menyimpan model terbaik dalam format .pkl menggunakan pickle atau joblib.
7. Implementasi Aplikasi Prediksi
   - Mengembangkan aplikasi berbasis Streamlit untuk mempermudah pengguna dalam melakukan prediksi.
   - Menyediakan fitur upload dataset, visualisasi data, prediksi dropout mahasiswa, serta unduhan hasil prediksi dalam format CSV.
8. Evaluasi dan Optimasi Model
   - Menggunakan cross-validation untuk mengevaluasi performa model dengan metrik accuracy, precision, recall, dan F1-score.
   - Menganalisis confusion matrix untuk memahami kesalahan prediksi.

### Persiapan

Sumber data: https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv

Setup Environment - Anaconda
```
conda create --name main-ds python=3.9  
conda activate main-ds  
pip install -r requirements.txt  
```
Setup Environment - Shell/Terminal
```
mkdir proyek_analisis_data  
cd proyek_analisis_data  
pipenv install  
pipenv shell  
pip install -r requirements.txt  
 
```

## Business Dashboard
Business dashboard yang telah dibuat berfungsi sebagai alat pemantauan kinerja akademik mahasiswa di Jaya Jaya Institut, dengan fokus pada tingkat kelulusan, dropout, dan faktor-faktor yang memengaruhi keberhasilan studi. Dashboard ini menyajikan visualisasi data yang mencakup jumlah total mahasiswa, tingkat kelulusan, serta analisis terhadap faktor seperti biaya kuliah, pendidikan sebelumnya, beasiswa, dan kehadiran di semester awal. Selain itu, terdapat analisis hubungan antara jumlah mata kuliah yang diambil dengan nilai masuk mahasiswa. Dengan tampilan yang interaktif dan informatif, dashboard ini membantu pihak akademik dalam mengidentifikasi pola dropout serta mengambil langkah strategis untuk meningkatkan retensi dan keberhasilan mahasiswa. Jika tersedia, dashboard ini dapat diakses melalui link berikut: https://lookerstudio.google.com/reporting/39a8d8b5-e939-4393-8ea9-265bac9e0ccd

![Untitled_Report (6)_page-0001](https://github.com/user-attachments/assets/7de93ead-37e5-4700-9e76-a2678f10ff3b)


## Menjalankan Sistem Machine Learning

```
streamlit run prediction.py
```

## Conclusion
Jelaskan konklusi dari proyek yang dikerjakan.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- action item 1
- action item 2
