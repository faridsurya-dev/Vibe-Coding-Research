
Setelah implementasi selesai, tahap berikutnya adalah memastikan bahwa perangkat lunak yang dibangun benar-benar sesuai dengan kebutuhan yang telah didefinisikan pada seluruh Source of Truth. Fase ini berfokus pada verifikasi dan validasi sistem sebelum perangkat lunak dinyatakan siap dirilis.

Dalam Chain of Truth, pengujian tidak hanya dilakukan terhadap kode. Pengujian dilakukan terhadap kesesuaian implementasi dengan artefak yang telah divalidasi sebelumnya. Dengan demikian, pertanyaan yang ingin dijawab bukan sekadar:

> "Apakah kodenya berjalan?"

Tetapi:

> "Apakah sistem yang dibangun sesuai dengan kebutuhan yang telah disepakati?"

### Tujuan Fase Testing

Tujuan utama fase ini adalah memastikan bahwa:

- Requirement telah terpenuhi.    
- User Flow berjalan sesuai desain.    
- API bekerja sesuai kontrak.    
- Integrasi frontend dan backend berjalan dengan benar.    
- Error handling bekerja sebagaimana mestinya.    
- Acceptance criteria terpenuhi.    

Fase ini menjadi gerbang terakhir sebelum sistem dapat dianggap siap digunakan.

### Dasar Penyusunan Test Case

Dalam Chain of Truth, test case diturunkan dari Source of Truth, bukan dibuat berdasarkan kode semata.

Sumber utama pengujian adalah:

|Source of Truth|Digunakan Untuk|
|---|---|
|User Flows (SoT #4)|Functional Testing, User Journey Testing, Acceptance Testing|
|UCIC (SoT #7)|API Testing, Contract Testing, Integration Testing|
|HiFi Prototype (SoT #5)|UI Validation dan User Acceptance Review|

Pendekatan ini menjaga agar pengujian tetap berfokus pada kebutuhan bisnis dan perilaku sistem yang diharapkan.

### Jenis Pengujian

#### Functional Testing

Memastikan setiap use case berjalan sesuai User Flow.

Contoh:

- Login berhasil.    
- Membuat pesanan berhasil.    
- Membatalkan transaksi berhasil.    

#### API Testing

Memastikan endpoint bekerja sesuai kontrak yang didefinisikan dalam UCIC.

Contoh:

- Request payload valid.    
- Response payload sesuai spesifikasi.    
- Status code benar.    
- Error response sesuai kontrak.    

#### Integration Testing

Memastikan frontend dan backend dapat bekerja bersama tanpa masalah integrasi.

Contoh:

- Form frontend mengirim data yang benar.    
- Backend mengembalikan response yang sesuai.    
- Data tersimpan dengan benar di database.    

#### Acceptance Testing

Memastikan sistem memenuhi acceptance criteria yang telah ditetapkan pada User Flow.

Acceptance Testing biasanya dilakukan oleh stakeholder atau product owner sebelum sistem dinyatakan siap digunakan.

### Ketika Pengujian Gagal

Salah satu prinsip penting dalam Chain of Truth adalah:

> Perbaiki artefak yang menyebabkan masalah, bukan hanya gejalanya.

Ketika ditemukan kegagalan pengujian, tim harus menentukan sumber masalahnya:

#### Jika Implementasi Salah

```text
Requirement benar
↓
User Flow benar
↓
UCIC benar
↓
Implementasi salah
```

Maka yang diperbaiki adalah kode implementasi.

#### Jika Source of Truth Salah

```text
Requirement benar
↓
User Flow tidak lengkap
↓
UCIC menjadi salah
↓
Implementasi mengikuti UCIC
```

Maka yang diperbaiki adalah User Flow, kemudian artefak turunannya diperbarui dan divalidasi ulang.

Pendekatan ini mencegah praktik patching yang tidak terdokumentasi dan menjaga konsistensi seluruh rantai artefak.

### Output Fase 7

Jika seluruh pengujian berhasil dilewati, maka output fase ini adalah:

- Validated System    
- Release Candidate    
- Test Results    
- Validation Records    

Artefak-artefak tersebut menjadi bukti bahwa implementasi telah memenuhi kebutuhan yang didefinisikan dalam Source of Truth.

### Prinsip Utama Fase 7

Testing bukan sekadar aktivitas mencari bug. Dalam Chain of Truth, testing adalah proses memverifikasi bahwa seluruh rantai artefak—mulai dari requirement hingga implementasi—tetap konsisten.

Keberhasilan fase ini tidak hanya diukur dari jumlah bug yang ditemukan, tetapi dari kemampuan tim menjawab pertanyaan:

> Apakah sistem yang dibangun benar-benar merealisasikan kebutuhan pengguna sebagaimana yang didefinisikan dalam Chain of Truth?

Jika jawabannya ya, maka hasil implementasi dapat dipromosikan menjadi **Release Candidate** dan siap memasuki proses deployment atau release.