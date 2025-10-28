# 🛡️ Evaluasi Keamanan Sistem ERP Weskonek Menggunakan PTES dan CWE

> **Penelitian ini bertujuan untuk mengevaluasi keamanan sistem ERP berbasis web milik PT Tekno Konek Solusi (ERP Weskonek)** menggunakan pendekatan **Penetration Testing Execution Standard (PTES)** dengan **black-box testing**, serta **mengklasifikasikan kerentanan** menggunakan **Common Weakness Enumeration (CWE)**.

---

## 📖 Latar Belakang

Perkembangan teknologi informasi membawa dampak besar terhadap sistem bisnis modern, termasuk penerapan **Enterprise Resource Planning (ERP)**.  
ERP berfungsi sebagai sistem inti bisnis yang mengintegrasikan berbagai proses seperti keuangan, persediaan, produksi, dan SDM dalam satu platform.

Namun, meningkatnya ketergantungan pada sistem berbasis web juga meningkatkan risiko **keamanan siber**.  
Menurut laporan **Fortinet (2024)**, serangan siber di Indonesia meningkat hingga **43%** dibanding tahun sebelumnya, sementara hanya **12% perusahaan** yang siap menghadapi ancaman tersebut (**Cisco, 2024**).

Banyak kasus kebocoran data dan eksploitasi sistem terjadi akibat lemahnya autentikasi, konfigurasi server, atau input data yang tidak divalidasi.  
Sayangnya, belum ada penelitian yang secara khusus mengevaluasi keamanan **ERP Weskonek** milik **PT Tekno Konek Solusi**.

Penelitian ini dilakukan untuk:
- Mengevaluasi keamanan ERP Weskonek menggunakan **PTES (black-box)**  
- Mengklasifikasikan hasil temuan berdasarkan **CWE (Common Weakness Enumeration)**

---

## 🎯 Rumusan Masalah

ERP Weskonek merupakan sistem terintegrasi yang mencakup berbagai fungsi bisnis seperti keuangan, SDM, inventori, dan operasional.  
Dengan integrasi tersebut, keamanan menjadi aspek kritis untuk menjaga **kerahasiaan, integritas, dan ketersediaan data**.

Masalah utama:
- Ancaman keamanan web seperti **konfigurasi salah, autentikasi lemah, dan input tidak tervalidasi**
- Belum adanya **evaluasi keamanan komprehensif** terhadap ERP Weskonek

Pendekatan yang digunakan:
- **Metodologi PTES** dengan tahapan _intelligence gathering_ hingga _exploitation_
- **Klasifikasi hasil temuan** berdasarkan **CWE** agar hasil lebih terukur dan sesuai standar internasional

---

## 🧩 Tujuan Penelitian

1. **Mengevaluasi tingkat keamanan ERP Weskonek** melalui penetration testing terstruktur.
2. **Mengidentifikasi potensi kerentanan** dari sudut pandang penyerang eksternal (black-box).
3. **Mengklasifikasikan kerentanan** menggunakan standar **CWE**.
4. **Memberikan rekomendasi perbaikan** dan langkah mitigasi keamanan.

---

## 💡 Manfaat Penelitian

### Akademik
- Menambah literatur dan pengetahuan di bidang **cybersecurity**, khususnya **PTES-based penetration testing**.
- Menjadi **referensi penelitian** bagi akademisi dalam evaluasi keamanan aplikasi berbasis web.

### Non-Akademik
- Membantu **PT Tekno Konek Solusi** memahami kondisi keamanan aktual ERP Weskonek.
- Memberikan **rekomendasi peningkatan keamanan sistem** dan membangun kepercayaan pengguna terhadap keamanan data perusahaan.

---

## 📚 Tinjauan Pustaka

### 1. Penelitian Terdahulu
Sebagian besar penelitian keamanan aplikasi web sebelumnya menggunakan **OWASP Top 10** sebagai acuan.  
Meskipun efektif, pendekatan tersebut belum cukup mendalam untuk menjelaskan akar penyebab kelemahan pada tingkat kode atau arsitektur.

Beberapa penelitian lain menggunakan **black-box testing** yang realistis dalam mensimulasikan serangan eksternal.  
Namun, sebagian besar belum melibatkan **klasifikasi kelemahan** menggunakan **CWE**.

Kombinasi antara **PTES (metodologi pengujian)** dan **CWE (standar klasifikasi)** pada penelitian ini menjadi **nilai kebaruan**, terutama dalam konteks **sistem ERP lokal**.

---

## 🧠 Landasan Teori

### 🏢 Enterprise Resource Planning (ERP)
Sistem ERP mengintegrasikan berbagai proses bisnis ke dalam satu platform.  
Namun, karena sering diakses secara daring, sistem ini rawan terhadap serangan seperti:
- SQL Injection (CWE-89)
- Cross-Site Scripting (CWE-79)
- Broken Authentication
- Security Misconfiguration  

Evaluasi keamanan berkala melalui penetration testing sangat penting untuk menjaga keandalan sistem.

---

### 🔐 Keamanan Aplikasi Web
Keamanan web bertujuan melindungi integritas, kerahasiaan, dan ketersediaan data dari serangan seperti:
- Injection Attacks
- Cross-Site Scripting (XSS)
- Broken Access Control
- Security Misconfiguration  

Standar keamanan yang sering digunakan:
- **OWASP Top 10**
- **NIST SP 800-115**
- **ISO/IEC 27001**

Namun, **penetration testing** memberikan pendekatan lebih praktis karena melibatkan simulasi serangan nyata.

---

### 🧪 Penetration Testing
Penetration testing adalah simulasi serangan siber untuk mengidentifikasi celah keamanan yang bisa dieksploitasi.  
Tujuannya:
- Menemukan kerentanan
- Mengukur tingkat risiko
- Memberikan rekomendasi mitigasi  

Dapat dilakukan secara:
- **Manual testing**
- **Automated testing**

---

### ⚙️ Metodologi PTES (Penetration Testing Execution Standard)

Tahapan utama PTES:
1. **Pre-Engagement Interactions** – menentukan ruang lingkup & aturan pengujian  
2. **Intelligence Gathering** – mengumpulkan informasi target (domain, IP, teknologi)  
3. **Threat Modeling** – memetakan potensi ancaman dan vektor serangan  
4. **Vulnerability Analysis** – identifikasi celah keamanan  
5. **Exploitation** – membuktikan dampak eksploitasi  
6. **Post-Exploitation** – menganalisis akses yang didapat setelah eksploitasi  
7. **Reporting** – dokumentasi hasil dan rekomendasi mitigasi  

PTES diakui secara internasional karena sistematis, repeatable, dan fleksibel terhadap jenis sistem yang diuji.

---

### 🕶️ Black-Box Testing
Metode pengujian tanpa pengetahuan struktur internal sistem.  
Penguji hanya berinteraksi melalui antarmuka publik, seperti halaman login atau endpoint API.

Kelebihan:
- Representatif terhadap serangan nyata eksternal  
Kekurangan:
- Terbatas dalam eksplorasi karena tidak mengetahui struktur kode internal  

---

### 🧩 Common Weakness Enumeration (CWE)
CWE adalah daftar global kelemahan perangkat lunak yang dikembangkan oleh **MITRE Corporation**.

Contoh umum:
- **CWE-79**: Cross-Site Scripting (XSS)  
- **CWE-89**: SQL Injection  
- **CWE-200**: Exposure of Sensitive Information  

CWE memungkinkan klasifikasi kelemahan secara spesifik dan mendalam, melampaui cakupan OWASP Top 10.

---

## 📊 Kesimpulan Awal
Penelitian ini mengombinasikan metodologi **PTES** dan klasifikasi **CWE** untuk mengevaluasi keamanan **ERP Weskonek** secara menyeluruh.  
Pendekatan ini diharapkan menghasilkan hasil analisis yang:
- **Terstruktur**
- **Terukur**
- **Sesuai standar internasional**

---

## 🧾 Lisensi
Repositori ini menggunakan lisensi **MIT**.  
Silakan gunakan, modifikasi, dan distribusikan dengan mencantumkan atribusi yang sesuai.

---

## 👨‍💻 Penulis
**Nama:** Ken Narendra Ekamartha
**Peran:** Junior Programmer & Cyber Security Enthusiast  
**Institusi:** PT Tekno Konek Solusi  

> 💬 _“Security isn’t a feature — it’s a foundation.”_
