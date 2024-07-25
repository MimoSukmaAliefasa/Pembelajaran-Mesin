## SISTEM REKOMENDASI PADA JOB RECOMMENDATION MENGGUNAKAN COSINE SIMILARITY

## Nama : Mimo Sukma Aliefasa
## NIM  : A11.2022.14592
## Kelp : A11.4412

## Ringkasan dan Tujuan Proyek

Proyek ini adalah sistem rekomendasi pekerjaan yang menggunakan metode Cosine Similarity untuk mencocokkan keterampilan pelamar dengan persyaratan pekerjaan. Sistem ini bertujuan untuk:

- Memudahkan pelamar menemukan pekerjaan yang sesuai dengan keterampilan mereka.
- Membantu perusahaan dalam menemukan kandidat yang tepat.
- Implementasi dilakukan dalam Python menggunakan Jupyter Notebook, dengan memanfaatkan pustaka seperti pandas, numpy, dan scikit-learn.

      +-----------------------+
      |         Mulai         |
      +-----------------------+
                |
                v
      +-----------------------+
      |     Muat Dataset      |
      +-----------------------+
                |
                v
      +-----------------------+
      |   Pembersihan Data    |
      +-----------------------+
                |
                v
      +-----------------------+
      |   Praproses Data      |
      +-----------------------+
                |
                v
      +-----------------------+
      | TF-IDF Vectorization  |
      +-----------------------+
                |
                v
      +-----------------------+
      | Hitung Cosine Similarity|
      +-----------------------+
                |
                v
      +-----------------+----------------+
      |                                  |
      v                                  v
      +--------------------+       +--------------------+
      | Filter dan Sortir  |       | Visualisasi Data   |
      +--------------------+       +--------------------+
                \                     /
                 v                   v
                +-----------------------+
                |  Tampilkan Rekomendasi |
                +-----------------------+
                /             \
               v               v
      +-----------------------+  +-----------------------+
      | Feedback dan Penyesuaian |  |     Selesai         |
      +-----------------------+  +-----------------------+


## Model / Alur Penyelesaian

Sistem ini mengikuti alur penyelesaian berikut:

1. Pembersihan dan Praproses Data Teks: Membersihkan data teks untuk memastikan data dalam format yang konsisten dan siap dianalisis.
2. Penggunaan TF-IDF Vectorization: Mengonversi teks menjadi vektor numerik yang memungkinkan perbandingan antara keterampilan pelamar dan deskripsi pekerjaan.
3. Penghitungan Cosine Similarity: Mengukur kesamaan antara keterampilan pelamar dan persyaratan pekerjaan.
4. Penyajian Hasil Rekomendasi: Menampilkan rekomendasi pekerjaan yang relevan untuk setiap pelamar.

## Datasets

##'jobs.csv'
Dataset ini berisi informasi mengenai pekerjaan, dengan kolom-kolom sebagai berikut:

- 'job_id': ID pekerjaan
- 'title': Judul pekerjaan
- 'description': Deskripsi pekerjaan
- 'requirements': Persyaratan pekerjaan

## 'applicants.csv'
Dataset ini berisi informasi mengenai pelamar, dengan kolom-kolom sebagai berikut:

- 'applicant_id': ID pelamar
- 'name': Nama pelamar
- 'skills': Keterampilan pelamar
- 'experience': Pengalaman kerja pelamar

## Model
## Pembersihan Data
Data teks dibersihkan dengan:

- Menghapus karakter non-alfabet
- Mengonversi teks menjadi huruf kecil
- Menghilangkan spasi berlebih

## Model TF-IDF
TF-IDF (Term Frequency-Inverse Document Frequency) digunakan untuk mengukur kepentingan 
kata dalam sebuah dokumen relatif terhadap seluruh korpus. Ini membantu dalam menangkap 
pentingnya kata kunci dalam deskripsi pekerjaan dan keterampilan pelamar.

##Cosine Similarity
Cosine Similarity mengukur kesamaan antara dua vektor berdasarkan sudut di antara mereka. Ini 
digunakan untuk membandingkan vektor keterampilan pelamar dengan vektor persyaratan pekerjaan, 
memberikan nilai kesamaan antara 0 hingga 1, di mana 1 berarti kesamaan sempurna.

## Kesimpulan
Sistem rekomendasi ini efektif dalam mencocokkan keterampilan pelamar dengan persyaratan 
pekerjaan menggunakan metode Cosine Similarity. Dengan mengimplementasikan TF-IDF 
Vectorization dan Cosine Similarity, sistem ini dapat memberikan rekomendasi pekerjaan yang
relevan berdasarkan keterampilan pelamar. Proyek ini dapat diperluas dan disesuaikan lebih lanjut 
untuk meningkatkan akurasi rekomendasi atau menambahkan fitur baru sesuai kebutuhan.

