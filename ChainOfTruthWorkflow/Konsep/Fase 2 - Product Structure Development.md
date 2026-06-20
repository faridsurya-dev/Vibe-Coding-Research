Setelah SRS divalidasi, langkah berikutnya adalah menerjemahkan kebutuhan sistem menjadi struktur produk yang lebih operasional. Pada fase ini, SRS dipecah menjadi tiga artefak utama: **Information Architecture (IA)**, **Design System**, dan **User Flows**. Ketiga artefak tersebut dikembangkan secara paralel dan menjadi fondasi bagi desain antarmuka, model data, serta implementasi sistem.

Tujuan utama fase ini adalah menjawab tiga pertanyaan penting:

- **Apa saja yang ada dalam produk?** → Information Architecture    
- **Bagaimana tampilan dan perilaku antarmuka harus konsisten?** → Design System    
- **Bagaimana pengguna mencapai tujuannya di dalam sistem?** → User Flows    

### Information Architecture (IA)

Information Architecture mendefinisikan struktur informasi dan navigasi produk. Artefak ini menjelaskan halaman, modul, menu, hubungan antarhalaman, serta bagaimana informasi diorganisasikan agar mudah digunakan oleh pengguna.

Output:

- Sitemap    
- Struktur menu    
- Hierarki halaman    
- Relasi antarfitur dan modul    

### Design System

Design System mendefinisikan bahasa visual dan pola interaksi yang digunakan di seluruh aplikasi. Tujuannya adalah menjaga konsistensi desain sehingga setiap halaman dan komponen memiliki tampilan dan perilaku yang seragam.

Output:

- Color palette    
- Typography    
- Spacing system    
- Grid system    
- UI Components    
- Interaction patterns    
- Responsive guidelines    

### User Flows

User Flow mendeskripsikan langkah-langkah yang dilakukan pengguna untuk mencapai suatu tujuan bisnis. Setiap use case didokumentasikan secara terstruktur sehingga dapat digunakan sebagai dasar desain, data model, API contract, implementasi, dan pengujian.

Minimal isi User Flow:

- Use Case ID    
- Actor    
- Goal    
- Trigger    
- Preconditions    
- Main Flow    
- Alternative Flow    
- Exception Flow    
- Postconditions    
- Related Pages    
- Acceptance Criteria    

Dalam Chain of Truth, User Flow memiliki peran yang sangat penting karena menjadi sumber utama untuk membangun Data Model dan Use Case Integration Contract pada fase berikutnya.

### Output Fase 2

Fase ini menghasilkan tiga Source of Truth baru:

|Source of Truth|Deskripsi|
|---|---|
|SoT #2|Validated Information Architecture|
|SoT #3|Validated Design System|
|SoT #4|Validated User Flows|

Ketiga artefak tersebut akan digunakan sebagai dasar pembuatan High-Fidelity Prototype pada fase berikutnya, sementara User Flows juga menjadi input utama untuk penyusunan Data Model dan UCIC.

### Prinsip Utama Fase 2

Pada fase ini, fokus tim bukan membuat desain atau kode, melainkan memastikan bahwa struktur produk sudah benar. Jika struktur informasi, pola desain, dan alur pengguna telah tervalidasi, maka proses desain, implementasi, dan pengujian di fase-fase berikutnya dapat dilakukan dengan lebih konsisten dan lebih sedikit revisi.