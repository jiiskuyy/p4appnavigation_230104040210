cat << 'EOF' > README.md
# Praktikum 4: Menggunakan Navigasi Aplikasi (Navio)

Projek ini adalah implementasi modul praktikum pemrograman mobile yang berfokus pada sistem navigasi Android modern menggunakan **Jetpack Compose Navigation**. Aplikasi ini mensimulasikan berbagai skenario navigasi mulai dari Activity klasik hingga arsitektur modern berbasis Fragment dalam satu Activity.

## 🛠️ Persyaratan Sistem
* **Android Studio:** Jellyfish | 2023.3.1 atau lebih baru (Disarankan Narwhal 2025.1.1) [cite: 27]
* **JDK:** version 17 [cite: 28, 145]
* **Minimum SDK:** API 24 (Android 7.0) [cite: 32, 88]
* **Target/Compile SDK:** API 35 [cite: 32, 106]

## 🚀 Fitur Utama
Aplikasi **Navio** mencakup empat pilar utama navigasi Android:

1.  **Explicit Intent Demo:** Simulasi perpindahan dari Activity A ke Activity B menggunakan konsep Intent eksplisit[cite: 12, 501].
2.  **Send Data (Intent Extras):** Implementasi pengiriman data (Nama & NIM) antar layar menggunakan argumen rute pada Navigation Compose[cite: 13, 608].
3.  **Back Stack Management:** Demonstrasi visual bagaimana Android mengelola tumpukan layar (stack) dalam navigasi multi-step (Step 1 -> 2 -> 3)[cite: 15, 879].
4.  **Activity + Fragment Style (Hub):** Struktur aplikasi modular dengan **Bottom Navigation** yang menampung Dashboard, Messages, dan Profile dalam satu Activity[cite: 18, 1087].

## 📂 Struktur Projek
```text
app/src/main/java/id/antasari/p4appnavigation_nimanda/
├── MainActivity.kt      # Titik masuk utama aplikasi [cite: 477]
├── nav/
│   ├── Routes.kt        # Definisi rute untuk 12 layar [cite: 256]
│   └── NavGraph.kt      # Kontroler pusat navigasi & Scaffold [cite: 290]
├── screens/
│   ├── HomeScreen.kt    # Menu utama (Dashboard navigasi) [cite: 402]
│   ├── ActivityA_B.kt   # Layar untuk demo Intent eksplisit [cite: 503]
│   ├── ActivityC_D.kt   # Form input dan penampil data [cite: 610]
│   ├── BackStackScreens.kt # Demo pengelolaan stack [cite: 883]
│   └── HubScreens.kt    # Implementasi Bottom Navigation [cite: 1090]
└── ui/theme/            # Konfigurasi Material Design 3 [cite: 65, 77]
