
Setelah seluruh artefak utama tervalidasi, tahap berikutnya adalah mengubah spesifikasi menjadi perangkat lunak yang dapat dijalankan. Pada fase ini, tim mulai membangun frontend, backend, database, dan integrasi berdasarkan Source of Truth yang telah disepakati sebelumnya.

Berbeda dengan pendekatan prompt-to-code yang sering langsung menghasilkan kode dari instruksi natural language, dalam Chain of Truth implementasi dilakukan berdasarkan artefak yang telah divalidasi. Dengan demikian, AI maupun developer bekerja menggunakan konteks yang jelas, terdokumentasi, dan dapat ditelusuri.

### Tujuan Fase Implementasi

Tujuan fase ini bukan sekadar menghasilkan kode, tetapi memastikan bahwa implementasi sesuai dengan kebutuhan yang telah didefinisikan pada fase-fase sebelumnya.

Setiap bagian sistem memiliki sumber referensi yang jelas:

- Frontend mengacu pada HiFi Prototype dan UCIC.    
- Backend mengacu pada Data Model dan UCIC.    
- Integrasi mengacu pada UCIC.    

Dengan pendekatan ini, implementasi menjadi proses menerjemahkan Source of Truth menjadi kode, bukan proses menafsirkan ulang requirement.

### Frontend Implementation

Pengembangan frontend menggunakan dua artefak utama:

- SoT #5 — Validated HiFi Prototype    
- SoT #7 — Validated UCIC    

Frontend bertanggung jawab untuk mengimplementasikan:

- Halaman dan navigasi    
- Komponen UI    
- Form dan validasi    
- State management    
- Integrasi API    
- Error handling    
- User interactions    

HiFi Prototype menjadi referensi tampilan dan pengalaman pengguna, sedangkan UCIC menjadi referensi komunikasi dengan backend.

### Backend Implementation

Pengembangan backend menggunakan:

- SoT #6 — Validated Data Model    
- SoT #7 — Validated UCIC    

Backend bertanggung jawab untuk mengimplementasikan:

- Business logic    
- Database schema    
- API endpoints    
- Authentication dan authorization    
- Validation rules    
- Data processing    
- Error responses    

Data Model mendefinisikan struktur data yang harus dikelola, sementara UCIC mendefinisikan perilaku API yang harus disediakan.

### Frontend-Backend Integration

Setelah frontend dan backend dikembangkan, keduanya diintegrasikan menggunakan kontrak yang telah ditetapkan dalam UCIC.

Karena frontend dan backend menggunakan referensi yang sama, risiko masalah seperti:

- Endpoint tidak ditemukan    
- Payload tidak sesuai    
- Format response berbeda    
- Status code tidak konsisten    
- Error handling tidak sinkron    

dapat dikurangi secara signifikan.

### Peran AI pada Fase Implementasi

AI dapat digunakan untuk membantu:

- Generate frontend code    
- Generate backend code    
- Generate database schema    
- Generate API implementation    
- Generate unit tests    
- Code review    
- Refactoring    
- Dokumentasi teknis
    

Namun dalam Chain of Truth, AI tidak menghasilkan kode berdasarkan prompt bebas. AI harus menggunakan Source of Truth yang telah divalidasi sebagai konteks utama. Dengan cara ini, kualitas dan konsistensi hasil implementasi dapat lebih terjaga.

### Output Fase 6

Fase ini menghasilkan:

- Frontend Application    
- Backend Services    
- Database Schema    
- API Implementation    
- Integrated System    

Output tersebut belum dianggap selesai sampai berhasil melewati fase pengujian.

### Prinsip Utama Fase 6

Fokus fase ini bukan menciptakan desain baru atau mengubah requirement, melainkan mengimplementasikan artefak yang telah disepakati sebelumnya.

Jika selama implementasi ditemukan kebutuhan baru atau ketidaksesuaian, perubahan tidak dilakukan langsung pada kode. Tim harus menelusuri artefak sumber yang terkait, memperbaikinya, melakukan validasi ulang, kemudian memperbarui implementasi. Prinsip ini menjaga agar kode tetap selaras dengan Source of Truth dan mencegah munculnya perubahan yang tidak terdokumentasi.