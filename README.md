# Context
The key to success in any organization is attracting and retaining top talent. I’m an HR analyst at my company, and one of my tasks is to determine which factors keep employees at my company and which prompt others to leave. I need to know what factors I can change to prevent the loss of good people. Watson Analytics is going to help.

## Problem 
Berdasarkan data terdapat 16.1% yang memutuskan untuk keluar sedangakn 83.9% sisanya memilih untuk bertahan, hal ini bisa meningkatkan cost yang berlebih jika terus dibiarkan.

## Data Descrition
Data ini terdiri dari :
- 35 kolom
- 1470 baris
  
## Analysist
Insight yang bisa didapatkan setelah melakukan analisa adalaha sebagai berikut :
- Secara jumlah, jenis kelamin laki-laki lebih banyak yang memutuskan keluar, diperjelas juga dengan proporsi pada masing-masing jenis kelamin, meski begitu selisihnya tidak terlalu jauh hanya sekitar >2% untuk yang memutuskan keluar
- Jika diperhatikan, dep R&D lebih banyak yang keluar, namun jika dibandingkan ternyata secara proporsi dep Sales lebih banyak yang keluar.
- Setelah di bedah lagi, ternyata dep Sales yang paling banyak keluar ada pada role job sebagai Sales Representative, sedangkan untuk R&D ada pada Laboratory Technician
- Rata-rata jarak dari rumah menuju ke kantor ternyata berpengaruh terhdapa keputusan untuk keluar dari perushaan
- Lamanya bekerja karywana yang keluar rata-rata sekitar > 5tahun
- Pada tahun 0-5 tahun, karyawan paling banyak yang keluar, dan pada tahun pertama ternyata sudah banyak karywana baru yang memutuskan untuk langsung resign
- Jarak rumah setiap karyawan yang memutuskan keluar lumayan bervariasi, jarak 1-2 KM paling banyak yang keluar.
- Kenyamaan karyawan berpengaruh disini, bisa dilihat bahwa semakin kecil rating yang dipilih maka makin besar kecendrungan karyawan untuk memutuskan keluar dari perusahaan
- Karyawan yang memilih rating 1 untuk enviromentsatisfaction cenderung lebih banyak untuk memutuskan keluar dari perusahaan
- Karaywan yang mendapatkan jam tambahan kerja/lembur cenderung memutuskan untuk resign, hal ini berpengaruh terhadap worklifebalance para karyawan
- Dari jumlah karyawan yang terlibat dalam suatu pekerjaan, yang tingkat keterlibatannya paling rendah (1) cenderung lebih banyak yang memutuskan keluar sekitar 33.27%
- Karywana dengan level rendah cendrung lebih banyak yang keluar, mungkin hal ini bisa terjadi karena adanya tawaran yang lebih menaraik dari perusahaan lain disamping mereka juga ingin meningkatkan jenjang karir
- Karyawan dengan gaji di bawah $4200 lebih banyak yang memutuskan untuk keluar

## Modelling & Prediction
Pada tahap ini, metrix evaluasi yang digunakan adalah "Recal", dimana mempertimbangkan untuk meminimalkan false negative yang artinya meminimalkan setiap karyawan yang diprediksi tidak keluar ternyata ingin keluar. Sehingga dengan begitu bisa dilakukan treatment kepada karywana yang di prediksi keluar.

### Model yang digunakan
- k-Nearest Neighbor
- Decision Tree
- RandomForest
- AdaBoost
- XGBoost

Dari ke-5 model yang digunakan, kami membandingkan Recall sebelum dan sesudah hyperparameter tuning
![image](https://github.com/jalikarani/employee-attrition/assets/79077525/50b1185b-f2b3-497a-806f-59a5f1a73d72)

![image](https://github.com/jalikarani/employee-attrition/assets/79077525/d4ddf7e5-008f-41ad-bd35-a90a1403b59a)


### Features Important
Dari hasil di atas, maka diputuskan model yang paling optimal adalah Adaboost dengan features important model adalah:
![image](https://github.com/jalikarani/employee-attrition/assets/79077525/db158e98-7cd1-48b1-bf3e-528dd7891686)

### Evaluation Metric
![image](https://github.com/jalikarani/employee-attrition/assets/79077525/54f0e3eb-6737-43b4-a5d7-f013b466783d)

## Business Simulation
- Attrition rate mengalami penurunan
- ![image](https://github.com/jalikarani/employee-attrition/assets/79077525/61f34a84-a4d5-4ace-b8ee-6c8dc3297ced)


- Menekan cost
  ![image](https://github.com/jalikarani/employee-attrition/assets/79077525/36793734-1ae5-43fa-b8c9-8648def95b47)

# Business Recommendation
1. Melakukan performance appraisal secara rutin/berkala: Ini adalah praktik di mana perusahaan secara teratur mengevaluasi kinerja karyawan, biasanya setiap tahun. Penilaian ini membantu dalam memahami sejauh mana karyawan telah mencapai tujuan mereka dan memberikan umpan balik untuk perbaikan.

2. Memberikan reward atau bonus bagi karyawan yang memiliki performa baik dan loyal kepada perusahaan: Dalam hal ini, perusahaan memberikan penghargaan berupa bonus atau insentif kepada karyawan yang telah menunjukkan performa yang luar biasa dan loyalitas terhadap perusahaan.

3. Mengurangi jam lembur bagi karyawan sehingga meminimalkan kemungkinan karyawan untuk keluar: Langkah ini dapat diambil untuk menghindari kelelahan dan memungkinkan keseimbangan kerja-hidup yang lebih baik bagi karyawan. Ini dapat membantu mempertahankan karyawan yang lebih puas.

4. Melakukan analisis ulang terhadap beban kerja karyawan: Perusahaan harus secara rutin mengevaluasi beban kerja karyawan untuk memastikan bahwa tugas dan tanggung jawab yang diberikan sesuai dengan kapasitas mereka. Ini dapat membantu mencegah stres berlebihan dan kelelahan.

5. Pengembangan potensi karyawan melalui pelatihan yang dibutuhkan: Memberikan pelatihan dan pengembangan yang sesuai untuk karyawan adalah cara untuk meningkatkan kompetensi mereka. Ini membantu karyawan merasa dihargai dan dapat meningkatkan kualitas kerja mereka.

6. Mempertimbangkan penerapan Employee Wellness Program guna meningkatkan tingkat produktivitas karyawan: Program kesejahteraan karyawan dapat mencakup berbagai inisiatif seperti program kesehatan, dukungan psikologis, dan manajemen stres. Ini bertujuan untuk meningkatkan kesejahteraan karyawan, yang pada gilirannya dapat meningkatkan produktivitas mereka.

Semua praktik ini penting dalam membangun lingkungan kerja yang sehat, memotivasi karyawan, dan meminimalkan turnover karyawan. Dengan demikian, organisasi dapat mencapai kinerja yang lebih baik dan tetap kompetitif di pasar.




