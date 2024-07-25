Sistem Rekomendasi Pekerjaan Menggunakan Cosine Similarity
1. Ringkasan dan Tujuan Proyek
Proyek ini adalah sistem rekomendasi pekerjaan yang menggunakan metode Cosine Similarity untuk mencocokkan keterampilan pelamar dengan persyaratan pekerjaan. Sistem ini bertujuan untuk:

Memudahkan pelamar menemukan pekerjaan yang sesuai dengan keterampilan mereka.
Membantu perusahaan dalam menemukan kandidat yang tepat.
Implementasi dilakukan dalam Python menggunakan Jupyter Notebook, dengan memanfaatkan pustaka seperti pandas, numpy, dan scikit-learn.
2. Model / Alur Penyelesaian
Sistem ini mengikuti alur penyelesaian berikut:

Pembersihan dan Praproses Data Teks: Membersihkan data teks untuk memastikan data dalam format yang konsisten dan siap dianalisis.
Penggunaan TF-IDF Vectorization: Mengonversi teks menjadi vektor numerik yang memungkinkan perbandingan antara keterampilan pelamar dan deskripsi pekerjaan.
Penghitungan Cosine Similarity: Mengukur kesamaan antara keterampilan pelamar dan persyaratan pekerjaan.
Penyajian Hasil Rekomendasi: Menampilkan rekomendasi pekerjaan yang relevan untuk setiap pelamar.
3. Datasets
jobs.csv
Dataset ini berisi informasi mengenai pekerjaan, dengan kolom-kolom sebagai berikut:

job_id: ID pekerjaan
title: Judul pekerjaan
description: Deskripsi pekerjaan
requirements: Persyaratan pekerjaan
Contoh isi:

plaintext
Copy code
job_id,title,description,requirements
1,Data Scientist,Analyze data and build models using Python,Python, Machine Learning, Data Analysis, Statistics
2,Software Engineer,Develop software solutions using Java,Java, Spring Boot, Software Development, Problem Solving
applicants.csv
Dataset ini berisi informasi mengenai pelamar, dengan kolom-kolom sebagai berikut:

applicant_id: ID pelamar
name: Nama pelamar
skills: Keterampilan pelamar
experience: Pengalaman kerja pelamar
Contoh isi:

plaintext
Copy code
applicant_id,name,skills,experience
1,John Doe,Python, Machine Learning, Data Analysis,3 years
2,Jane Smith,Java, Spring Boot, Software Development,5 years
4. Model
Pembersihan Data
Data teks dibersihkan dengan:

Menghapus karakter non-alfabet
Mengonversi teks menjadi huruf kecil
Menghilangkan spasi berlebih
Model TF-IDF
TF-IDF (Term Frequency-Inverse Document Frequency) digunakan untuk mengukur kepentingan kata dalam sebuah dokumen relatif terhadap seluruh korpus. Ini membantu dalam menangkap pentingnya kata kunci dalam deskripsi pekerjaan dan keterampilan pelamar.

Cosine Similarity
Cosine Similarity mengukur kesamaan antara dua vektor berdasarkan sudut di antara mereka. Ini digunakan untuk membandingkan vektor keterampilan pelamar dengan vektor persyaratan pekerjaan, memberikan nilai kesamaan antara 0 hingga 1, di mana 1 berarti kesamaan sempurna.

5. Kesimpulan
Sistem rekomendasi ini efektif dalam mencocokkan keterampilan pelamar dengan persyaratan pekerjaan menggunakan metode Cosine Similarity. Dengan mengimplementasikan TF-IDF Vectorization dan Cosine Similarity, sistem ini dapat memberikan rekomendasi pekerjaan yang relevan berdasarkan keterampilan pelamar. Proyek ini dapat diperluas dan disesuaikan lebih lanjut untuk meningkatkan akurasi rekomendasi atau menambahkan fitur baru sesuai kebutuhan.
