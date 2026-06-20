**Chain of Truth (CoT)** adalah workflow pengembangan perangkat lunak berbantuan AI yang menggunakan **validated artifacts sebagai Source of Truth (SoT)** di setiap tahap pengembangan.

Chain of Truth membangun serangkaian artefak yang saling terhubung dan tervalidasi, mulai dari requirement, user flow, data model, hingga implementation dan testing. Setiap artefak menjadi acuan resmi bagi proses berikutnya.

Dengan pendekatan ini, AI tetap digunakan untuk mempercepat pekerjaan, tetapi keputusan pengembangan tetap dikendalikan oleh artefak yang jelas, dapat ditelusuri, dan dapat divalidasi.

Tujuan utama Chain of Truth adalah meningkatkan **traceability, consistency, reproducibility, dan integration quality** dalam AI-assisted software development.

## Fase-Fase Chain of Truth

Chain of Truth terdiri dari tujuh fase utama yang membentuk rantai Source of Truth dari ide hingga perangkat lunak yang siap dirilis.

![CoT Method](https://raw.githubusercontent.com/faridsurya-dev/public-images/refs/heads/main/Chain%20of%20Truth%20Software%20Dev%20Method-Page-1.drawio.png)


### 1. Software Requirements Specification (SRS)

[[Fase 1 - Pengembangan SRS]] menerjemahkan ide produk, kebutuhan bisnis, dan kebutuhan pengguna menjadi dokumen requirement yang terstruktur.

Output dari fase ini adalah **Validated SRS (SoT #1)** yang menjadi dasar bagi seluruh artefak berikutnya.

**Tujuan:** memastikan seluruh tim memiliki pemahaman yang sama tentang apa yang akan dibangun.

### 2. Product Structure Development

Pada [[Fase 2 - Product Structure Development]], SRS dipecah menjadi tiga artefak utama:

- Information Architecture (IA)
- Design System
- User Flows

Ketiganya dikembangkan dan divalidasi secara terpisah.

Output fase ini adalah:

- **Validated Information Architecture (SoT #2)**    
- **Validated Design System (SoT #3)**    
- **Validated User Flows (SoT #4)**    

**Tujuan:** mendefinisikan struktur produk, pengalaman pengguna, dan aturan desain sebelum implementasi dimulai.

### 3. High Fidelity Prototype Development

User Flow, IA, dan Design System digunakan untuk menghasilkan prototype yang menyerupai produk akhir. Tiga SoT itu digunakan untuk pengembangan [[Fase 3 - High-Fidelity Prototype Development]].

Prototype digunakan untuk memvalidasi alur penggunaan dan pengalaman pengguna sebelum proses coding dimulai.

Output fase ini adalah **Validated HiFi Prototype (SoT #5)**.

**Tujuan:** memvalidasi desain dan perilaku sistem lebih awal sehingga biaya perubahan menjadi lebih rendah.

### 4. Data Model Development

Fase [[Fase 4 - Data Model Development]] menghasilkan model data berdasarkan User Flow yang telah divalidasi.

Data Model mendefinisikan:

- Entity    
- Attribute    
- Relationship    
- Business Rules    
- Validation Rules    

Output fase ini adalah **Validated Data Model (SoT #6)**.

**Tujuan:** memastikan struktur data mendukung seluruh proses bisnis yang telah didefinisikan dalam User Flow.

### 5. Use Case Integration Contract (UCIC) Development

[[Fase 5 - Use Case Integration Contract (UCIC) Development]] adalah fase untuk pengembangan artefak integrasi sistem. UCIC adalah kontrak integrasi pada level use case yang menyelaraskan frontend, backend, API, dan testing.

Setiap UCIC mendefinisikan:

- Sequence Diagram    
- API Contract    
- Request & Response Structure    
- Validation Rules    
- Error Handling    

Output fase ini adalah **Validated UCIC (SoT #7)**.

**Tujuan:** menghilangkan asumsi yang berbeda antara frontend dan backend sebelum implementasi dilakukan.

### 6. Implementation

[[Fase 6 - Implementation]] mengubah seluruh Source of Truth menjadi perangkat lunak yang berjalan.

- Frontend dibangun berdasarkan HiFi Prototype dan UCIC.    
- Backend dibangun berdasarkan Data Model dan UCIC.    
- Integrasi dilakukan berdasarkan kontrak yang telah disepakati.    

**Tujuan:** memastikan implementasi mengikuti artefak yang telah divalidasi, bukan berdasarkan interpretasi masing-masing developer.

### 7. Testing

[[Fase 7 - Testing and Validation]] memverifikasi bahwa implementasi sesuai dengan seluruh Source of Truth.

Testing dibuat berdasarkan:

- User Flow    
- UCIC    
- Acceptance Criteria    

Jika ditemukan masalah, perbaikan dilakukan pada artefak yang menjadi sumber masalah, bukan langsung melakukan patch pada kode.

**Tujuan:** memastikan perangkat lunak yang dihasilkan benar-benar sesuai dengan kebutuhan pengguna dan spesifikasi yang telah disepakati.

## Source of Truth Chain

```text
SRS
 ↓
Information Architecture
Design System
User Flows
 ↓
HiFi Prototype
 ↓
Data Model
 ↓
Use Case Integration Contract
 ↓
Implementation
 ↓
Testing
```

Setiap fase menghasilkan artefak yang tervalidasi dan menjadi **Source of Truth** bagi fase berikutnya. Dengan cara ini, perubahan dapat ditelusuri, keputusan dapat diaudit, dan AI dapat bekerja menggunakan konteks yang lebih jelas dan konsisten.

## Publikasi

Workflow versi artikel ilmiah ini dapat diakses melalui repositori preprint berikut ini:

```
Suryanto, F., & Ibnu, A. (2026). Chain of Truth: A Source-of-Truth Workflow for AI-Assisted Software Development. Zenodo. https://doi.org/10.5281/zenodo.20767965
```

