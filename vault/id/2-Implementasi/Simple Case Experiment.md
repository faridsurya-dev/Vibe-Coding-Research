# Chain of Truth in Practice #1

## Membangun Aplikasi Web Frontend dari Source of Truth

> **Dengan Chain of Truth, AI tidak lagi bergantung pada prompt. Ia bergantung pada Source of Truth.**

## 🚀 Coba Sendiri

Studi kasus implementasi ini sepenuhnya dapat direproduksi.

Artefak Source of Truth yang digunakan dalam eksperimen ini tersedia di sini:

Repository:
https://github.com/faridsurya-dev/vibe_coding_simple_case

Anda dapat memeriksa dokumen-dokumen tersebut, menggunakannya dengan AI coding assistant pilihan Anda, dan membandingkan hasilnya sendiri. Gambar di bawah ini adalah hasil menggunakan model Bigpickle, sebuah model open source yang diakses dengan opencode.

![aplikasi kasir](https://raw.githubusercontent.com/faridsurya-dev/public-images/refs/heads/main/Screenshot%202026-06-21%20133741.png)

# Pendahuluan

Salah satu tantangan terbesar dalam pengembangan perangkat lunak berbantuan AI adalah konsistensi.

Sebagian besar alur kerja vibe coding sangat bergantung pada prompt. Requirement, aturan bisnis, keputusan UI, dan detail implementasi secara bertahap terakumulasi di dalam percakapan.

Pendekatan ini berhasil untuk eksperimen kecil, tetapi masalah muncul seiring pertumbuhan proyek:

* Requirement tersebar di berbagai chat.
* AI dapat menginterpretasikan fitur yang sama secara berbeda dari waktu ke waktu.
* Konteks hilang saat memulai sesi baru.
* Model yang berbeda dapat menghasilkan implementasi yang berbeda.
* Validasi menjadi subjektif.

Chain of Truth (CoT) diciptakan untuk mengatasi masalah ini.

Alih-alih menyimpan pengetahuan proyek di dalam prompt, CoT memindahkan pengetahuan ke dalam artefak terstruktur yang disebut **Sources of Truth (SoT)**.

Studi kasus ini mendemonstrasikan bagaimana CoT digunakan untuk membangun aplikasi web frontend yang lengkap dengan integrasi API dummy, sambil menjaga prompt tetap minimal dan implementasi tetap konsisten.

# Tujuan

Tujuan dari implementasi ini bukan untuk membangun aplikasi POS.

Tujuannya adalah untuk memvalidasi hipotesis berikut:

> Source of Truth yang cukup detail dapat memandu AI coding assistant untuk mengimplementasikan aplikasi tanpa memerlukan prompt khusus fitur.

Aplikasi yang dihasilkan hanya berfungsi sebagai kendaraan untuk menguji alur kerja.

# Gambaran Proyek

## Aplikasi

Point of Sale (POS) Berbasis Web

## Domain

Ritel

## Peran Pengguna

Kasir

## Fitur Utama

### Transaksi Penjualan

* Login
* Menelusuri produk
* Manajemen keranjang
* Checkout
* Cetak struk

### Manajemen Inventaris

* Tambah produk
* Pemantauan stok

### Pelaporan

* Laporan penjualan harian
* Laporan penjualan bulanan

# Alur Kerja Chain of Truth

Alur kerja Chain of Truth yang lengkap dimulai dengan SRS.

```text
SRS
 ↓
Information Architecture
 ↓
Design System
 ↓
User Flows
 ↓
UCIC / System Logics
 ↓
Implementation
```

Namun, selama implementasi, coding assistant tidak langsung menggunakan SRS.

Fase implementasi hanya mengonsumsi artefak operasional:

* Information Architecture
* Design System
* User Flows
* UCIC (System Logics)

Artefak-artefak ini bertindak sebagai Source of Truth tingkat implementasi.

# Artefak Source of Truth

## 1. Information Architecture (IA)

IA mendefinisikan:

* Halaman
* Hierarki navigasi
* Struktur routing
* Hubungan antar layar

IA menjawab:

> Halaman apa saja yang ada dalam aplikasi?

## 2. Design System

Design System mendefinisikan:

* Bahasa visual
* Komponen
* Aturan tata letak
* Standar konsistensi UI

Design System menjawab:

> Bagaimana tampilan aplikasi?

## 3. User Flows

User Flows mendefinisikan:

* Interaksi pengguna
* Alur utama
* Alur alternatif
* Alur pengecualian

User Flows menjawab:

> Bagaimana perilaku aplikasi?

## 4. UCIC (System Logics)

UCIC mendefinisikan:

* Perilaku sistem
* Kontrak interaksi
* Logika aplikasi
* Ekspektasi API

UCIC menjawab:

> Apa yang seharusnya terjadi di balik antarmuka?

# Lingkungan Pengembangan

## IDE

OpenCode

## Model

* Bigpickle
* DeepSeek V4 Flash

## Strategi Sesi

Sesi tunggal.

Seluruh implementasi diselesaikan dalam satu sesi pengembangan.

# Prompt-nya

Salah satu hasil yang paling mengejutkan dari eksperimen ini adalah kesederhanaan prompt.

Hanya tiga prompt pengguna yang digunakan.

## Prompt 1

```text
Create a blank starter app using latest nextjs in 'pos_simple_[model_name]' folder.
```

## Prompt 2

```text
Based on @docs/design_system.md and @docs/information_architecture.md, create the application's pages and navigations structure.
```

## Prompt 3

```text
Implement the application's functionality in detail based on docs/user_flows/* and docs/system_logics/*, using dummy API calls where needed.
```

Perhatikan apa yang tidak ada.

Prompt tersebut tidak mengandung:

* requirement bisnis
* deskripsi fitur
* aturan validasi
* spesifikasi UI
* logika aplikasi

Detail-detail itu sudah ada di dalam Source of Truth.

Prompt hanya menginstruksikan AI untuk mengeksekusi.

# Dari Pengembangan Berbasis Prompt ke Pengembangan Berbasis Source of Truth

Vibe coding tradisional sering terlihat seperti ini:

```text
Requirement
 ↓
Prompt
 ↓
AI
 ↓
Revisi Prompt
 ↓
AI
 ↓
Prompt Lainnya
 ↓
AI
```

Seiring waktu, pengetahuan proyek tersebar di berbagai percakapan.

Chain of Truth mengubah alur kerja:

```text
Requirement
 ↓
Source of Truth
 ↓
AI
```

Source of Truth menjadi pembawa pengetahuan.

Prompt menjadi instruksi eksekusi.

Pergeseran ini adalah inti dari Chain of Truth.

# Hasil Pengembangan

AI coding assistant berhasil menghasilkan:

* Aplikasi frontend yang lengkap
* Navigasi aplikasi
* Layar UI
* Interaksi pengguna
* Integrasi API dummy
* Alur kerja ujung-ke-ujung

Aplikasi yang dihasilkan sepenuhnya dapat dinavigasi dan berfungsi dalam ruang lingkup yang ditentukan.

# Intervensi Manusia

Pengamatan penting selama eksperimen adalah sifat intervensi pengguna.

Pesan tambahan hanya diperlukan ketika terjadi masalah teknis eksekusi, seperti:

* kegagalan pembuatan file
* masalah akses model sementara
* gangguan konektivitas

Perbaikannya hanya dengan menyalin dan menempelkan pesan error.

Tidak ada prompt tambahan yang diperlukan untuk menjelaskan:

* fitur
* aturan bisnis
* alur kerja
* persyaratan validasi

Ini menunjukkan bahwa Source of Truth menyediakan konteks implementasi yang memadai.

# Strategi Validasi

Validasi tidak dilakukan hanya melalui inspeksi visual.

Sebaliknya, test case diturunkan dari:

```text
SRS
 ↓
User Flows
 ↓
Test Cases
```

Ini menciptakan lapisan validasi yang independen.

Implementasi dievaluasi terhadap ekspektasi yang telah ditentukan sebelumnya, bukan berdasarkan penilaian subjektif.

# Hasil Pengujian

## Total Test Case

30

## Lulus

100% test case frontend yang berlaku

## Gagal

0

## Dikecualikan

Test case yang memerlukan implementasi backend nyata

Hasilnya menunjukkan bahwa aplikasi yang dihasilkan konsisten dengan kebutuhan yang tertangkap di Source of Truth.

# Temuan Utama

## Temuan #1 — Manfaat Terbesar Adalah Konsistensi

Manfaat paling signifikan yang diamati bukanlah kecepatan.

Melainkan konsistensi.

Sebelum Chain of Truth:

* requirement berada dalam percakapan
* pergeseran konteks sering terjadi
* implementasi fitur menjadi tidak konsisten

Setelah Chain of Truth:

* requirement berada dalam artefak
* implementasi menjadi dapat dilacak
* konteks tetap stabil
* perilaku AI menjadi lebih dapat diprediksi

## Temuan #2 — Prompt Menjadi Lebih Kecil

Pengurangan kompleksitas prompt adalah efek samping.

Pencapaian sesungguhnya adalah memindahkan pengetahuan proyek keluar dari prompt dan ke dalam artefak.

Hasilnya:

* prompt menjadi lebih pendek
* sesi menjadi dapat direproduksi
* model menjadi dapat dipertukarkan

## Temuan #3 — Validasi Menjadi Objektif

Tanpa Source of Truth:

```text
Apakah tampilan aplikasi sudah benar?
```

Dengan Source of Truth:

```text
Apakah implementasi memenuhi test case?
```

Ini adalah model validasi yang fundamentally berbeda.

# Mengapa Ini Penting

Banyak alur kerja pengembangan berbantuan AI mengoptimalkan prompt.

Chain of Truth mengoptimalkan konteks.

Prompt engineering berusaha meningkatkan komunikasi dengan AI.

Chain of Truth berusaha meningkatkan kualitas dan struktur pengetahuan yang diberikan kepada AI.

Perbedaannya halus namun penting.

Ketika konteks dapat diandalkan, prompt menjadi sederhana.

Ketika konteks tidak dapat diandalkan, prompt engineering menjadi tidak ada habisnya.

# Kesimpulan

Eksperimen ini mendemonstrasikan bahwa aplikasi web frontend dapat diimplementasikan dengan sukses menggunakan Chain of Truth dengan prompt yang minimal.

Coding assistant hanya menerima tiga prompt yang berorientasi pada eksekusi dan mengandalkan artefak Source of Truth untuk semua keputusan fungsional dan perilaku.

Aplikasi yang dihasilkan:

* sepenuhnya dapat dinavigasi
* mengimplementasikan alur kerja yang dimaksudkan
* mengintegrasikan API dummy
* lulus semua test case frontend yang berlaku

Yang terpenting, eksperimen menunjukkan bahwa:

> **Dengan Chain of Truth, AI tidak lagi bergantung pada prompt. Ia bergantung pada Source of Truth.**

# Dukung Penelitian

Chain of Truth adalah inisiatif penelitian independen yang berfokus pada peningkatan pengembangan perangkat lunak berbantuan AI.

Jika karya ini membantu Anda, pertimbangkan untuk mendukung penelitian dan eksperimen di masa depan:

https://saweria.co/faridsurya

Setiap kontribusi membantu mendanai eksperimen tambahan, dokumentasi, perangkat, dan sumber daya open source untuk komunitas.
