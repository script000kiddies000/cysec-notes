### **Why 

ReFlutter digunakan untuk melakukan rekayasa balik (reverse engineering) pada aplikasi berbasis Flutter. Dengan ReFlutter, pengguna dapat:

1. **Menganalisis Aplikasi Flutter** – Memungkinkan pengembang atau peneliti keamanan untuk mempelajari bagaimana sebuah aplikasi Flutter bekerja, termasuk kode yang dieksekusi melalui DartVM.
2. **Melakukan Intersepsi Lalu Lintas** – Menggunakan ReFlutter bersama Burp Suite memungkinkan pemantauan dan intersepsi lalu lintas aplikasi tanpa perlu akses root pada perangkat Android.
3. **Bypass Certificate Pinning** – Membantu melewati beberapa implementasi certificate pinning yang digunakan dalam aplikasi untuk melindungi komunikasi jaringan.
4. **Modifikasi Library Flutter** – Memungkinkan pengembang untuk menerapkan perubahan khusus pada kode Flutter menggunakan Dockerfile yang sudah disediakan.

---

### **What 

ReFlutter adalah framework untuk melakukan reverse engineering pada aplikasi Flutter dengan menggunakan versi modifikasi dari pustaka Flutter yang telah dikompilasi sebelumnya. Beberapa fitur utama dari ReFlutter meliputi:

- **Patch pada `socket.cc`** untuk memonitor dan mengintersep lalu lintas aplikasi.
- **Modifikasi pada `dart.cc`** untuk mencetak informasi terkait class, fungsi, dan beberapa field dalam aplikasi.
- **Dukungan untuk Android (arm64, arm32) dan iOS (arm64)** serta berbagai rilis Flutter (Stable, Beta).
- **Kemudahan instalasi** melalui `pip3 install reflutter`.
- **Pembuatan ulang APK/IPAp yang telah di-patch** untuk memungkinkan analisis lebih lanjut pada aplikasi Flutter.

---

### **How (Bagaimana Cara Menggunakan ReFlutter?)**

#### **1. Instalasi**

ReFlutter dapat diinstal di berbagai sistem operasi dengan perintah berikut:

```bash
pip3 install reflutter
```

#### **2. Penggunaan Dasar**

Untuk melakukan rekayasa balik pada aplikasi Flutter dalam format APK atau IPA:

```bash
reflutter main.apk
reflutter main.ipa
```

Pengguna perlu memasukkan alamat IP Burp Suite Proxy Server yang akan digunakan untuk intersepsi lalu lintas.

#### **3. Konfigurasi Burp Suite untuk Intersepsi Lalu Lintas**

- **Tambahkan port:** `8083`
- **Bind ke semua interface:** `All interfaces`
- **Aktifkan invisible proxying:** `true`

#### **4. Penyesuaian APK untuk Android**

APK yang telah dihasilkan perlu di-sign sebelum dipasang di perangkat:

```bash
java -jar uber-apk-signer.jar --allowResign -a release.RE.apk
```

Untuk melihat kode yang dimuat melalui DartVM, aplikasi harus dijalankan pada perangkat, dan dump dapat diambil dengan:

```bash
adb -d shell "cat /data/data/<PACKAGE_NAME>/dump.dart" > dump.dart
```


#### **5. Penggunaan pada iOS**

- Jalankan aplikasi hasil `reflutter main.ipa` pada perangkat iOS.
- Informasi analisis akan muncul di log XCode dengan tag `reflutter`.

Dengan mengikuti langkah-langkah ini, pengguna dapat melakukan analisis dinamis aplikasi Flutter dengan lebih mudah dan efektif. 🚀