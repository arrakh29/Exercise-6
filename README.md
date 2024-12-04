# Exercise-6-
Exercise 6 – Demonstrate a simple way to eliminate resource contention suspending the scheduler

## 📋 Deskripsi

Proyek ini dibuat untuk mempelajari penggunaan multitasking pada mikrokontroler STM32 dengan menggunakan FreeRTOS. Terdapat dua task utama:
1. **GREENLEDTASK**: Menyalakan dan mematikan LED hijau setiap 500 ms.
2. **REDLEDTASK**: Menyalakan dan mematikan LED merah setiap 100 ms.

Kedua task ini mengakses sumber daya bersama menggunakan mekanisme **critical section** untuk memastikan keamanan data.

---

## 🛠️ Komponen yang Digunakan

- **Mikrokontroler**: STM32F103
- **LED**: Merah, Hijau, Biru, dan Kuning
- **FreeRTOS**: Sistem operasi real-time
- **Perangkat Lunak**:
  - STM32CubeMX untuk konfigurasi hardware
  - Keil uVision atau STM32CubeIDE untuk pengembangan kode

---

## ✨ Fitur Utama

- **Multitasking** dengan FreeRTOS
- **Penggunaan Critical Section** untuk mengakses sumber daya bersama
- **Kendali LED Berbasis Waktu** menggunakan delay FreeRTOS
- **Indikasi Konflik**: LED biru akan menyala jika ada konflik saat mengakses sumber daya bersama

---

## ⚙️ Pengaturan

1. **Hardware**:
   - Hubungkan LED ke port GPIO pada STM32 sesuai konfigurasi berikut:
     - **LED Merah**: Pin GPIOB
     - **LED Hijau**: Pin GPIOB
     - **LED Biru**: Pin GPIOB
     - **LED Kuning**: Pin GPIOB

2. **Software**:
   - Gunakan STM32CubeMX untuk menghasilkan kode inisialisasi.
   - Pastikan FreeRTOS diaktifkan dalam konfigurasi STM32CubeMX.

3. **Definisi GPIO**:
   - `#define HIGH GPIO_PIN_RESET`
   - `#define LOW GPIO_PIN_SET`

---

## 🚀 Cara Menggunakan
