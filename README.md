
# 🧭 Navio: Modul Praktikum Navigasi Aplikasi Android (Week 4)

Aplikasi **Navio** merupakan proyek praktikum *Mobile Programming* tahun 2025 yang berfokus pada implementasi navigasi modern menggunakan **Jetpack Compose Navigation**[cite: 1, 17]. Proyek ini mencakup konsep dasar Intent hingga struktur aplikasi modular berbasis *Fragment-style* dalam satu Activity[cite: 12, 18].

## 👨‍🏫 Informasi Modul
* **Topik:** Menggunakan Navigasi Aplikasi[cite: 3].
* **Dosen Pengampu:** Muhayat, M.IT[cite: 8].
* **Durasi Praktikum:** 1 x 100 menit[cite: 10].
* **Target Pembelajaran:** Memahami Explicit Intent, Activity Lifecycle, Back Stack, dan Material Design 3[cite: 12, 14, 15, 20].

## 🛠️ Spesifikasi Teknis & Alat
* **Android Studio:** Narwhal | 2025.1.1[cite: 27].
* **JDK:** Version 17 (Microsoft OpenJDK)[cite: 28, 145].
* **SDK:** Compile SDK 35, Target SDK 35, Min SDK 24[cite: 32].
* **Library Utama:**
    * Jetpack Compose + Material 3[cite: 37].
    * Navigation Compose 2.8.3[cite: 43].
    * DataStore Preferences 1.1.1 (untuk persistensi tema & profil)[cite: 47, 75].

## 🚀 Fitur Utama (Langkah 1-7)
Aplikasi ini diorganisir ke dalam empat kartu menu utama pada `HomeScreen`[cite: 403, 422]:

1. **Explicit Intent (Activity A → B):** Demonstrasi peluncuran Activity baru menggunakan Intent eksplisit dan pemahaman dasar *Back Stack*[cite: 12, 500].
2. **Send Data (Activity C → D):** Pengiriman data melalui argumen rute (Nama & NIM) dari form input ke layar penampil data[cite: 13, 608].
3. **Back Stack Demo (Step 1-3):** Visualisasi tumpukan layar dengan fitur `LinearProgressIndicator` dan tombol untuk membersihkan stack kembali ke Home[cite: 879, 881].
4. **Hub (Activity + Fragment Style):** Implementasi **Bottom Navigation** yang menampung tab Dashboard, Messages (dengan Message Detail), dan Profile[cite: 1086, 1087].

## 🏆 Track Expert (Langkah 8-9)
Fitur tingkat lanjut untuk optimasi aplikasi:
* **Form "Tahan Badai":** Penggunaan `rememberSaveable` dan `DisposableEffect` agar data form tidak hilang saat rotasi layar atau perubahan konfigurasi[cite: 1464, 1474, 1475].
* **Dynamic Message Detail:** Pengiriman argumen ID dinamis pada tab Messages untuk menampilkan konten pesan yang berbeda[cite: 1500, 1511].
* **Custom Branding:** Penambahan logo kustom `ic_navio` dan judul dinamis pada `TopAppBar`[cite: 1560, 1590].

## 📂 Struktur Proyek Minimal
Proyek ini menggunakan struktur package yang modular[cite: 53, 54]:
```text
id.antasari.p4appnavigation_nimanda/
├── MainActivity.kt      # Entry point dengan NavGraph [cite: 486]
├── nav/
│   ├── Routes.kt        # Definisi sealed class untuk rute [cite: 262]
│   └── NavGraph.kt      # Pengaturan NavHost dan Scaffold [cite: 292]
├── screens/
│   ├── HomeScreen.kt    # Dashboard utama aplikasi [cite: 404]
│   ├── ActivityA_B.kt   # Layar demo Intent eksplisit [cite: 504]
│   ├── ActivityC_D.kt   # Layar input dan penerima data [cite: 612]
│   ├── BackStackScreens.kt # Demo pengelolaan stack [cite: 885]
│   └── HubScreens.kt    # Implementasi Bottom Navigation [cite: 1091]
└── res/
    ├── values/strings.xml     # String default (English) [cite: 68]
    └── values-in/strings.xml  # Lokalisasi Bahasa Indonesia [cite: 69]
