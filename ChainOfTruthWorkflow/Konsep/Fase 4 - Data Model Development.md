
Setelah alur pengguna tervalidasi melalui User Flows, tahap berikutnya adalah membangun **Data Model**. Fase ini bertujuan menerjemahkan kebutuhan proses bisnis menjadi struktur data yang akan digunakan oleh sistem. Data Model mendefinisikan objek bisnis, atribut, relasi antarentitas, aturan validasi, dan batasan data yang diperlukan untuk mendukung seluruh use case yang telah disepakati.

Dalam Chain of Truth, Data Model tidak diturunkan langsung dari SRS, melainkan dari **Validated User Flows (SoT #4)**. Alasannya sederhana: user flow menunjukkan bagaimana data dibuat, dibaca, diperbarui, divalidasi, dan digunakan dalam proses bisnis nyata. Dengan demikian, struktur data yang dihasilkan lebih selaras dengan kebutuhan operasional sistem.

### Apa yang Dibangun?

Data Model dapat mencakup:

- Domain entities    
- Business objects    
- Attributes dan data types    
- Relationships antarentitas    
- Cardinality    
- Validation rules    
- Business constraints    
- Lifecycle atau state transitions    
- Persistence requirements    

Contoh sederhana:

Jika pada User Flow terdapat proses:

```text
User membuat pesanan
↓
Sistem menyimpan pesanan
↓
User melakukan pembayaran
↓
Pesanan berubah menjadi Paid
```

Maka kemungkinan akan muncul entitas seperti:

- User    
- Order    
- Payment    

Beserta relasi dan aturan bisnis di antaranya.

### Mengapa Data Model Dibangun Setelah User Flow?

Pendekatan tradisional sering memulai desain dari database terlebih dahulu. Dalam praktiknya, hal ini sering menghasilkan struktur data yang tidak benar-benar mencerminkan proses bisnis.

Chain of Truth menggunakan pendekatan sebaliknya:

```text
User Flow
      ↓
Data Model
```

Artinya, data dibentuk berdasarkan kebutuhan proses, bukan proses yang dipaksa mengikuti struktur database.

Pendekatan ini membantu memastikan bahwa setiap entitas dan atribut memiliki alasan keberadaan yang jelas serta dapat ditelusuri kembali ke use case yang membutuhkannya.

### Validasi Data Model

Sebelum menjadi Source of Truth, Data Model perlu ditinjau untuk memastikan:

- Semua User Flow dapat didukung.    
- Tidak ada entitas yang hilang.    
- Relasi antarentitas sudah benar.    
- Aturan bisnis telah terakomodasi.    
- Struktur data cukup fleksibel untuk kebutuhan sistem.    

Jika ditemukan bahwa suatu User Flow tidak dapat diimplementasikan dengan model data yang ada, maka revisi dilakukan pada Data Model sebelum proses dilanjutkan.

### Output Fase 4

Fase ini menghasilkan:

|Source of Truth|Deskripsi|
|---|---|
|SoT #6|Validated Data Model|

Data Model yang telah divalidasi menjadi dasar untuk:

- Desain database    
- Backend implementation    
- API design    
- Validation rules    
- Business logic    
- Integration contracts (UCIC)    

### Prinsip Utama Fase 4

Fokus fase ini bukan membangun database, melainkan membangun **pemahaman bersama tentang data bisnis** yang digunakan oleh sistem.

Dengan menjadikan User Flow sebagai sumber utama, Data Model tidak hanya menjawab _"data apa yang disimpan?"_, tetapi juga _"mengapa data tersebut diperlukan dan bagaimana data tersebut digunakan dalam proses bisnis?"_. Prinsip ini memperkuat traceability dari requirement hingga implementasi, sekaligus memastikan bahwa struktur data selalu memiliki keterkaitan yang jelas dengan kebutuhan pengguna.