## Apa itu SRS?

Software Requirements Specification (SRS) adalah dokumen yang mendefinisikan kebutuhan perangkat lunak secara terstruktur, lengkap, dan dapat diverifikasi.

SRS bukan konsep baru yang muncul karena AI atau metode Chain of Truth. SRS merupakan artefak yang telah lama digunakan dalam disiplin Software Engineering dan memiliki standar yang diterbitkan oleh **Institute of Electrical and Electronics Engineers (IEEE)** melalui standar **IEEE Recommended Practice for Software Requirements Specifications (IEEE 830)** dan kemudian diperbarui dalam **ISO/IEC/IEEE 29148** untuk Requirements Engineering.

Tujuan utama SRS adalah mengubah kebutuhan bisnis, kebutuhan pengguna, dan tujuan produk menjadi spesifikasi yang jelas sehingga dapat dipahami, diimplementasikan, diuji, dan dipelihara oleh tim pengembang.

Dalam praktik modern, format SRS tidak harus mengikuti template IEEE secara kaku. Banyak organisasi menggunakan versi yang lebih ringan sesuai kebutuhan proyek. Namun prinsip dasarnya tetap sama:

- Requirement harus eksplisit.
- Requirement harus dapat divalidasi.
- Requirement harus dapat ditelusuri (traceable).
- Requirement harus menjadi dasar desain, implementasi, dan pengujian.

Dalam Chain of Truth, SRS berperan sebagai **Source of Truth pertama (SoT #1)**. SRS menjadi titik awal yang mengubah ide produk menjadi artefak rekayasa perangkat lunak yang dapat digunakan untuk menghasilkan User Flow, Information Architecture, Design System, Data Model, dan artefak lainnya.

### SRS vs PRD

Banyak orang menggunakan istilah PRD (Product Requirements Document) dan SRS (Software Requirements Specification) secara bergantian. Padahal keduanya memiliki fokus yang berbeda.

|Aspek|PRD|SRS|
|---|---|---|
|Fokus|Produk|Sistem Perangkat Lunak|
|Tujuan|Menjelaskan apa yang ingin dibangun dan mengapa|Menjelaskan secara rinci bagaimana kebutuhan sistem didefinisikan|
|Audiens Utama|Product Manager, Business Stakeholder|Developer, Architect, QA, AI Coding Assistant|
|Isi Utama|Problem, Vision, User Needs, Success Metrics|Functional Requirements, Non-Functional Requirements, Business Rules, Constraints|
|Tingkat Detail|Menengah|Tinggi|
|Orientasi|Business dan Product|Engineering dan Implementation|

Secara sederhana, **PRD menjawab:**  _"Produk apa yang ingin kita bangun dan mengapa?"_. Sedangkan **SRS menjawab:**  _"Kebutuhan perangkat lunak apa yang harus dipenuhi agar produk tersebut dapat diwujudkan?"_

## Fungsi SRS dalam Pengembangan

SRS berfungsi sebagai fondasi pengembangan perangkat lunak.

1. Menyamakan Pemahaman:  SRS memastikan seluruh stakeholder memiliki pemahaman yang sama mengenai tujuan produk, ruang lingkup, kebutuhan pengguna, dan fitur yang akan dibangun.

2. Mengurangi Ambiguitas: Banyak kegagalan proyek berasal dari kebutuhan yang tidak jelas atau hanya tersimpan dalam percakapan. SRS mengubah kebutuhan tersebut menjadi spesifikasi yang eksplisit dan terdokumentasi.

3. Menjadi Acuan Pengembangan: Semua artefak downstream dibangun berdasarkan SRS yang telah divalidasi. Dengan demikian, AI maupun developer tidak bekerja berdasarkan asumsi atau interpretasi pribadi.

4. Mendukung Traceability: Setiap User Flow, Data Model, API Contract, implementasi, dan test case dapat ditelusuri kembali ke requirement yang mendasarinya.

5. Mengendalikan Perubahan: Ketika terjadi perubahan kebutuhan, tim dapat memperbarui SRS terlebih dahulu, kemudian menurunkan perubahan tersebut ke artefak lain secara sistematis.

## Bagaimana Membangun SRS

Tujuan utama fase ini adalah mengubah ide produk menjadi requirement yang jelas dan dapat digunakan sebagai dasar pengembangan.

### Langkah 1 — Memahami Masalah

Kumpulkan informasi dari:

- Product vision    
- Business goals    
- Stakeholder interview    
- User research    
- Existing process    
- Technical constraints    

Fokus utama pada pertanyaan:

- Masalah apa yang ingin diselesaikan?    
- Siapa pengguna sistem?    
- Nilai apa yang ingin diberikan?    
- Batasan apa yang harus dipatuhi?    

### Langkah 2 — Mendefinisikan Scope

Tentukan:

- In Scope    
- Out of Scope    
- Asumsi    
- Constraint    

Tahap ini penting untuk mencegah scope creep sejak awal.

### Langkah 3 — Mengidentifikasi Aktor dan Tujuan

Untuk setiap jenis pengguna:

- Siapa mereka?    
- Apa tujuan mereka?    
- Aktivitas apa yang ingin mereka lakukan?    

Output tahap ini biasanya berupa daftar user roles dan user goals.

### Langkah 4 — Mendefinisikan Fitur

Setiap fitur dijelaskan dalam bentuk:

- Nama fitur    
- Deskripsi    
- Functional requirements    
- Business rules    

Contoh:

**Fitur: Registrasi Akun**

Requirements:

- Sistem harus memungkinkan pengguna membuat akun.    
- Sistem harus memverifikasi email pengguna.    
- Sistem harus menolak email yang sudah terdaftar.    

### Langkah 5 — Mendefinisikan Kebutuhan Non-Fungsional

Contohnya:

- Performance    
- Security    
- Availability    
- Scalability    
- Maintainability    
- Usability    

Requirement non-fungsional sering menjadi sumber masalah jika tidak didefinisikan sejak awal.

### Langkah 6 — Review dan Validasi

SRS belum menjadi Source of Truth sebelum divalidasi.

Validasi dilakukan untuk memastikan:

- Requirement benar    
- Requirement lengkap    
- Scope sesuai    
- Tidak ada kontradiksi    
- Dapat diimplementasikan    

Setelah disetujui stakeholder, dokumen berubah status menjadi **Validated SRS (SoT #1)** dan dapat digunakan untuk menghasilkan artefak berikutnya.

## Struktur SRS

Struktur SRS yang digunakan dalam Chain of Truth dibuat cukup ringan agar mudah digunakan oleh manusia maupun AI.

### 1. Introduction

Berisi:

- Purpose    
- Scope    
- Stakeholders    
- Definitions    
- References    

### 2. Product Overview

Berisi:

- Product Summary    
- User Types    
- User Goals    
- Operating Environment    
- Assumptions    
- Constraints    

### 3. System Features

Untuk setiap fitur:

- Feature ID    
- Feature Name    
- Description    
- Functional Requirements    
- Business Rules    

### 4. Data Requirements

Berisi:

- Core Business Objects    
- Ownership Rules    
- Data Retention Rules    
- Data Validation Rules    

### 5. External Interfaces

Berisi:

- UI Requirements    
- External Systems    
- Communication Requirements    

### 6. Non-Functional Requirements

Berisi:

- Performance    
- Security    
- Availability    
- Reliability    
- Scalability    
- Maintainability    
- Usability    

### 7. Permissions and Access Control

Menjelaskan hak akses setiap role.

### 8. Feature Inventory

Daftar seluruh fitur dan prioritasnya.

### 9. Open Questions

Hal-hal yang masih perlu diklarifikasi.

### 10. Future Considerations

Ide atau kebutuhan yang belum masuk scope saat ini.

### 11. Revision History

Riwayat perubahan dokumen untuk menjaga traceability.

**Output fase SRS Development:**  
**Validated SRS (Source of Truth #1)** yang menjadi dasar pembuatan Information Architecture, Design System, dan User Flows pada fase berikutnya dalam Chain of Truth.