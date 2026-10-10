# Proyek Hierarki Bangun Datar (Polimorfisme Java)

Proyek ini dibuat untuk mempelajari dan menerapkan konsep pemrograman berorientasi objek (OOP), khususnya **polimorfisme**, **inheritance**, **abstract class**, serta penerapan prinsip *Open-Closed Principle* (OCP) pada bahasa pemrograman Java.

## Struktur Berkas Proyek

Berikut adalah daftar berkas utama yang menyusun proyek ini:

* **`BangunDatar.java`**: Kelas abstrak induk yang mendefinisikan kontrak utama (`luas()`, `keliling()`) serta template method (`toString()`).
* **`Lingkaran.java`**: Kelas turunan yang merepresentasikan bangun datar lingkaran menggunakan `Math.PI` serta validasi jari-jari.
* **`Persegi.java`**: Kelas turunan yang merepresentasikan bangun datar persegi dengan validasi sisi.
* **`Segitiga.java`**: Kelas turunan yang merepresentasikan segitiga menggunakan Rumus Heron serta teorema ketidaksamaan sisi.
* **`Trapesium.java`**: Kelas turunan untuk menghitung luas dan keliling trapesium.
* **`Main.java`**: Program utama (driver) untuk menguji hasil implementasi menggunakan *upcasting*, perulangan polimorfik, total luas, hingga *downcasting* selektif.

## Fitur Utama

1. **Polimorfisme & Dynamic Method Dispatch**: Pemanggilan method `luas()` dan pencetakan objek secara otomatis diselesaikan pada saat *runtime* berdasarkan objek turunannya.
2. **Validasi Ketat (Defensive Programming)**: Seluruh konstruktor kelas turunan dilengkapi validasi untuk menolak nilai parameter yang bernilai nol atau negatif ($\le 0$).
3. **Ekstensibilitas Tinggi**: Menambah bangun datar baru tidak memerlukan perubahan pada logika perulangan atau pemrosesan di kelas utama (`Main.java`), cukup dengan membuat kelas turunan baru dari `BangunDatar`.

## Cara Menjalankan

1. Pastikan semua berkas kode sumber (`.java`) berada di direktori atau paket yang sama.
2. Kompilasi seluruh berkas menggunakan terminal/command prompt:
   ```bash
   javac *.java