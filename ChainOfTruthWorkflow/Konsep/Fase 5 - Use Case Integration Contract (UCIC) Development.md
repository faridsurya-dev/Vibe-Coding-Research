
Setelah User Flow dan Data Model tervalidasi, tahap berikutnya adalah menyusun **Use Case Integration Contract (UCIC)**. Fase ini bertujuan menerjemahkan kebutuhan bisnis, alur pengguna, dan struktur data menjadi kontrak integrasi yang dapat digunakan bersama oleh frontend, backend, QA, dan AI coding assistant.

Dalam banyak proyek, masalah tidak muncul karena requirement yang salah, tetapi karena frontend dan backend memiliki interpretasi yang berbeda terhadap requirement yang sama. Frontend mengharapkan format data tertentu, sementara backend mengembalikan format yang berbeda. Frontend menganggap suatu proses hanya membutuhkan satu API, sementara backend membaginya menjadi beberapa endpoint.

UCIC dibuat untuk menghilangkan asumsi-asumsi tersebut.

### Apa itu UCIC?

UCIC adalah kontrak implementasi pada level use case.

Jika User Flow menjelaskan:

> Apa yang dilakukan pengguna.

Dan Data Model menjelaskan:

> Data apa yang digunakan sistem.

Maka UCIC menjelaskan:

> Bagaimana frontend, backend, API, dan database bekerja bersama untuk mewujudkan use case tersebut.

UCIC menjadi bahasa bersama yang digunakan seluruh tim sebelum implementasi dimulai.

### Input UCIC

UCIC dibangun dari dua Source of Truth utama:

- SoT #4 — Validated User Flows    
- SoT #6 — Validated Data Model    

```text
User Flow
      +
Data Model
      ↓
     UCIC
```

User Flow memberikan konteks proses bisnis, sedangkan Data Model memberikan konteks struktur data yang digunakan selama proses berlangsung.

### Apa yang Dibangun?

Setiap use case memiliki satu UCIC tersendiri.

Minimal isi UCIC meliputi:

- Use Case Reference    
- Related Screens    
- Related Entities    
- Sequence Diagram    
- API Contract    
- Request Payload    
- Response Payload    
- Status Codes    
- Validation Rules    
- Data Mapping    
- Error Handling    

Dengan adanya UCIC, seluruh detail integrasi sudah didefinisikan sebelum frontend dan backend mulai dikembangkan.

### Contoh Sederhana

Misalkan terdapat use case:

**UC-001 — Login**

User Flow menjelaskan:

```text
User memasukkan email dan password
↓
Sistem memverifikasi kredensial
↓
Sistem mengembalikan token
↓
User masuk ke dashboard
```

UCIC kemudian mendefinisikan:

- Endpoint: POST /auth/login    
- Request Body    
- Response Body    
- Error Response    
- Validasi Input    
- Sequence Diagram    
- Mapping ke entitas User    

Dengan demikian frontend dan backend memiliki pemahaman yang sama mengenai bagaimana use case tersebut harus diimplementasikan.

### Mengapa UCIC Penting?

Tanpa kontrak integrasi yang jelas, frontend dan backend sering berkembang secara terpisah berdasarkan asumsi masing-masing.

Akibatnya muncul masalah seperti:

- Endpoint tidak sesuai kebutuhan UI    
- Payload berbeda dari yang diharapkan    
- Status code tidak konsisten    
- Error handling berbeda    
- Integrasi terlambat ditemukan bermasalah    

UCIC mengurangi risiko tersebut dengan menjadikan integrasi sebagai artefak yang tervalidasi sebelum implementasi dimulai.

### Validasi UCIC

Sebelum menjadi Source of Truth, UCIC perlu ditinjau untuk memastikan:

- Mendukung seluruh langkah dalam User Flow.    
- Menggunakan Data Model yang benar.    
- API Contract sudah lengkap.    
- Data Mapping sudah jelas.    
- Error Handling sudah terdefinisi.    
- Frontend dan backend memiliki pemahaman yang sama.    

Jika ditemukan ketidaksesuaian, revisi dilakukan pada User Flow, Data Model, atau UCIC sesuai sumber masalahnya.

### Output Fase 5

Fase ini menghasilkan:

|Source of Truth|Deskripsi|
|---|---|
|SoT #7|Validated UCIC|

UCIC yang telah divalidasi menjadi acuan utama untuk:

- Frontend implementation    
- Backend implementation    
- API development    
- Frontend-backend integration    
- Contract testing    
- Integration testing    

### Prinsip Utama Fase 5

Fokus fase ini bukan membangun API, melainkan membangun **kesepakatan integrasi** sebelum kode ditulis.

Dengan adanya UCIC, frontend dan backend tidak lagi bekerja berdasarkan interpretasi masing-masing, tetapi berdasarkan kontrak yang sama. Hal ini membuat implementasi lebih konsisten, mengurangi integration mismatch, dan memberikan konteks yang jauh lebih jelas bagi AI coding assistant saat menghasilkan kode.