# TUGAS   Visualisasi Data dan Informasi

Nama : Virdio Samuel Saragih

NIM : 122450124

Dosen Pengampu : Ahmad Luky Ramdani S.Komp., M.Kom 

---

# Making data visualization more efficient and effective: a survey

## Introduction
Visualisasi data sangat penting dalam dunia bisnis yang didukung oleh data saat ini, yang telah banyak digunakan untuk membantu pengambilan keputusan yang terkait erat dengan pendapatan utama banyak perusahaan. Visualisasi Data sejatinya berfungsi untuk mengubah data abstrak menjadi bentuk visual fisik yang dapat dipahami dengan mudah. Visualisasi data juga bertujuan untuk menjelaskan data dalam bentuk cerita (storytelling)

<img src="https://github.com/user-attachments/assets/bdff4a88-788a-4736-bf45-e1aa14750bff" width=1000/>

Dibawah ini adalah alur pembuatan visualisasi data 
1. Impor Data berguna untuk mengambil data yang diperlukan dari sumber data yang diinginkan.
2. Data Preparation untuk mempersiapkan data yang diimpor untuk visualisasi, misalnya dengan menormalkan nilai, memperbaiki entri yang salah, dan menginterpolasi nilai yang hilang.
3. Data Manipulation adalah untuk memilih data yang akan divisualisasikan (dikenal juga sebagai penyaringan dalam komunitas visualisasi) dan mungkin juga dengan operasi umum lainnya seperti penggabungan dan pengelompokan.
4. Mapping adalah untuk memetakan data yang diperoleh dari proses di atas ke bentuk geometris (misalnya, titik dan garis), bersama dengan atributnya (misalnya, warna, posisi, dan ukuran).
5. Rendering adalah untuk mengubah data geometris di atas menjadi representasi visual.

Berdasarkan alur, ada 3 hal penting yang membuat visualisasi data lebih efektif dan efisien, yaitu
- Visualization Specifications
  - **Self-completeness** Penting bagi pembaca untuk mengetahui cara menghasilkan visualisasi data.
  - **Language design perspective** pengguna harus menentukan bagaimana memetakan informasi berbeda kedalam visual.
- **Efficient Approaches for Data Visualization** Untuk melibatkan pengguna secara efektif dalam alur, proses pembuatan visualisasi data harus efisien dan skalabel, terutama untuk dua komponen dalam alur, Manipulasi Data dan Pemetaan.

- **Data Visualization Recommendation**
Menentukan visualisasi dengan tepat sangat sulit, karena pemahaman tentang data yang akan divisualisasikan, cerita yang akan disampaikan, dan cara memvisualisasikan harus dilakukan uji pemahaman langsung kepada pengguna. Oleh karena itu, penting agar sistem visualisasi dapat secara cerdas membimbing pengguna dengan memberikan rekomendasi.

## Visualization specifications

Secara umum, visualisasi data terdiri dari tiga spesifikasi: data, visual, dan pemetaan antara keduanya.

Data terdiri dari Records dan Transformation
  - Records: data yang perlu divisualisasikan.
  - Transformation: operasi pada pengolahan data seperti grup, bin, filter, dan sort.

Visual terdiri dari Type, Size, Legend, Miscellaneous

  - Type: representasi visual untuk catatan data, seperti batang, garis, atau titik.
  - Size: lebar, tinggi dari visualisasi.
  - Legend: informasi legenda.
  - Miscellaneous: properti lain, seperti lebar dan warna dari batang.

Untuk pemetaan berfungsi memetakan data ke visual yang sesuai.

## Kategori Visualisasi Data
Secara teori ada 4 kategori, low-level language, high-level language, gui-based tools dan terakhir underspecified language

<img src="https://github.com/user-attachments/assets/5410a273-6e01-43c9-aec7-f0f7b0dafaa4" width=1000/>

- Low-level Languages adalah bahasa tingkat rendah yang mengharuskan pengguna untuk menentukan semua elemen pemetaan.
- High-level Languages adalah bahasa tingkat tinggi yang mengenkapsulasi detail proses pembuatan visualisasi, seperti fungsi pemetaan, serta beberapa properti untuk tanda-tanda seperti ukuran kanvas, legenda, dan properti lainnya.
- GUI-Based tools adalah kependekan dari Graphical User Interface yang mana pengguna dapat membuat visualisasi data langsung menggunakan fitur dan menu yang "tampak" seperti drag an drop, dan lain-lain. Contoh software GUI seperti Qlik, Excel, Google Sheet, PowerBI dan lain-lain
- Underspecified language
Visualisasi data di mana pengguna memberikan rincian yang tidak lengkap tentang kebutuhan visualisasi mereka dan menjadi tanggung jawab software visualisasi untuk menerjemahkan input yang tidak lengkap ini dengan berbagai cara. Ini juga termasuk petunjuk seperti visualisasi referensi, di mana pengguna memberikan visualisasi awal untuk sistem agar dapat menyarankan visualisasi serupa berdasarkan referensi tersebut.

## Efficient approaches for data visualization
<img src="https://github.com/user-attachments/assets/97e2de36-ecb1-4885-929d-a95cc13e3edf" width=1000/>

Dalam pembuatan visualisasi data dibutuhkan pengambilan dan integrasi data yang efisien agar mempermudah pembuatan visualisasi, ada beberapa cara untuk membuat visualisasi yang efisien, seperti
- **Query Translation**
  Contoh pada software DeepEye, Polaris, dan SeeDB mendapatkan data dengan kode SQL ke database.

- **Integrating Visualization Systems with DBMS**
  Kekurangan query translation adalah 
- Column Store
Dalam manajemen data, data diatur seperti tampilan baris atau kolom, hal ini dapat mempengaruhi kinerja secara signifikan. Dalam visualisasi data, pengguna biasanya hanya membutuhkan beberapa kolom. Oleh karena itu, penyimpanan data berbasis kolom memberikan kinerja yang lebih baik dibandingkan dengan penyimpanan berbasis baris, seperti yang digunakan dalam software SeeDB.

- **Indexes**
Indeks digunakan untuk meningkatkan kinerja pencarian dengan cara mengurangi jumlah catatan/baris dalam tabel yang perlu diperiksa.

- **Parallel Computation**
Komputasi ini mempertahankan satu thread aplikasi utama untuk menangkap permintaan interaksi pengguna dan beberapa thread visualisasi untuk setiap visualisasi untuk memproses visualisasi tersebut. Selain itu, thread utama dan thread visualisasi bersifat asinkron atau sinkron tergantung pada kebutuhan pengguna

- **Prediction and Prefetching**
Prediksi dan Prefetching merujuk pada teknik yang digunakan dalam visualisasi data untuk meningkatkan proses eksplorasi dengan mencoba untuk meramal kebutuhan pengguna. Metode ini melibatkan prediksi visualisasi atau data berikutnya yang mungkin menarik bagi pengguna berdasarkan interaksi mereka saat ini dan eksplorasi sebelumnya. Dengan menyimpan data yang diperkirakan, sistem dapat mempercepat proses visualisasi.

## Visualization recommendation
Proses visualisasi data bersifat iteratif, dan banyak contoh visualisasi yang mungkin untuk dibuat. 
Berikut adalah cara untuk memilih mana visualisasi yang cocok dan bagus pada masalah tertentu:

- **Perankingan**
Sistem rekomendasi visualisasi perlu terlebih dahulu membuat daftar semua visualisasi yang mungkin, lalu merekomendasikan visualisasi dengan peringkat tertinggi. Tetapi sebagai pengguna harus mempertimbangkan kombinasi beberapa faktor, seperti memilih kolom yang akan divisualisasikan, mengubah data dan lain-lain karena pilihan bentuk visualisasi data yang banyak

- **Pruning Meaningless Visualizations**
Pruning Meaningless Visualizations merujuk pada proses menghilangkan visualisasi yang buruk dengan menerapkan berbagai batasan, baik dari pengguna maupun aturan yang ditentukan oleh ahli. Proses ini melibatkan pembuatan kandidat visualisasi yang cocok dengan mempertimbangkan kombinasi variabel, transformasi, dan pengkodean visual, lalu mengenali makna visualisasi berdasarkan metrik atau aturan yang telah ditetapkan. Beberapa sistem juga dapat memberi peringkat visualisasi yang menarik atau merekomendasikan visualisasi terbaik kepada pengguna setelah proses pemangkasan ini. Pengguna juga dapat menentukan elemen visualisasi yang diminati.

- **Expert provided constraints**
Beberapa kombinasi variabel, transformasi, dan visual mungkin tidak menghasilkan visualisasi yang valid. Misalnya, visualisasi pie tidak dapat digabungkan dengan jenis variabel height. Batasan ini biasanya diberikan oleh para ahli.

## Other research directions
### Data preparation for data visualization
Data dunia nyata sering kali masih kotor dan berantakan, dan memvisualisasikan data yang belum bersih dapat membuat pengguna tidak paham akan insight dari visualisasi tersebut. Fenomena ini dikenal sebagai salah satu jenis visualisasi yang bias. Misalnya, dataset yang diintegrasikan dari berbagai sumber data yang mengandung duplikat. Data yang akan divisualisasikan harus dibersihkan dengan teknik-teknik tertentu, seperti melakukan normalisasi nilai, penghapusan duplikat, imputasi nilai yang hilang, dan deteksi outlier. Contoh software Tableau telah mengintegrasikan Trifacta untuk melakukan data preparation pada dataset.

### Data visualization for database-related applications
Contoh software visualisasi data yang terintegrasi dengan sistem database
- Excel
- Google Sheets
- Oracle Data Visualization Desktop
- IBM Db2
- Amazon Quicksight
- Microsoft Power BI
