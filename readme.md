![Frontend](https://img.shields.io/badge/Frontend-Javascript-yellow)
![Praktikum](https://img.shields.io/badge/Praktikum-Pemrograman_Web-green)
![Telkom](https://img.shields.io/badge/Telkom-University-red)

# Praktikum Pengembangan Web dengan JavaScript

## Deskripsi

Praktikum ini bertujuan untuk mempelajari dasar-dasar JavaScript dalam pengembangan web interaktif. Proyek ini mencakup implementasi berbagai konsep JavaScript seperti variabel, konsol, percabangan, array, operasi matematika, manipulasi DOM, dan animasi sederhana. Halaman web yang dibuat berisi fitur interaktif seperti tombol untuk menampilkan variabel, memeriksa nilai, menampilkan array, melakukan operasi matematika, menganimasikan elemen, dan mengelola counter.

## Tujuan

- Memahami penggunaan variabel (`let`, `const`, `var`) dan output ke konsol atau alert.
- Menerapkan logika percabangan (`if-else`) untuk pengambilan keputusan.
- Mengelola dan menampilkan data array menggunakan metode seperti `join()`.
- Melakukan operasi matematika dasar berdasarkan input pengguna.
- Membuat animasi sederhana dengan manipulasi CSS melalui JavaScript.
- Mengimplementasikan interaksi DOM untuk memperbarui konten halaman secara dinamis.
- Membangun halaman web interaktif yang responsif dan user-friendly.

## Isi Projek

- `index.html`: File utama yang berisi struktur halaman web dengan elemen HTML untuk menampilkan fitur variabel, percabangan, array, operasi matematika, animasi lingkaran, dan counter, serta skrip JavaScript untuk logika interaktif.

## Cara Menjalankan

1. **Clone Repositori**:
   ```bash
   git clone https://github.com/nnichaelangello/Tugas-5-JavaScript-Mata-Kuliah-Pemrograman-Website.git
   ```

2. **Buka File**:
   - Buka file `index.html` di browser modern (Chrome, Firefox, atau Edge) untuk melihat halaman web dan menguji fitur interaktif.
   - Tidak diperlukan server lokal karena proyek ini hanya menggunakan HTML dan JavaScript vanilla.

3. **Interaksi**:
   - Klik tombol "Coba Cek" untuk melihat contoh variabel.
   - Klik tombol "Cek Nilai" untuk memeriksa status lulus/tidak lulus berdasarkan input nilai.
   - Klik tombol "Lihat Array" untuk menampilkan daftar buah.
   - Masukkan dua angka dan klik tombol operasi matematika (Tambah, Kurang, Kali, Bagi) untuk melihat hasilnya.
   - Klik tombol "Gerakkan Lingkaran" untuk menganimasikan lingkaran dengan perubahan warna dan posisi.
   - Klik tombol "Tambah" atau "Kurang" untuk mengubah nilai counter.

## Penjelasan JavaScript

Berikut adalah penjelasan detail tentang fungsi-fungsi JavaScript yang digunakan dalam proyek ini, disertai dengan contoh kode untuk setiap fungsi:

### 1. Fungsi `contohVariabel()`
- **Tujuan**: Menunjukkan penggunaan variabel dengan tipe data berbeda.
- **Penjelasan**:
  - Mendeklarasikan tiga variabel: `nama` (string, menggunakan `let`), `umur` (number, menggunakan `const`), dan `aktif` (boolean, menggunakan `var`).
  - Menampilkan nilai variabel dalam sebuah pesan alert menggunakan template literal (`${}`).
  - **Contoh Output**: `Nama: Michael\nUmur: 21\nAktif: true`.
- **Catatan**: Penggunaan `let` dan `const` lebih disarankan daripada `var` karena scoping yang lebih baik dan mencegah re-deklarasi yang tidak disengaja.
- **Contoh Kode**:
  ```javascript
  function contohVariabel() {
    let nama = "Michael";
    const umur = 21;
    var aktif = true;
    alert(`Nama: ${nama}\nUmur: ${umur}\nAktif: ${aktif}`);
  }
  ```

### 2. Fungsi `cekNilai()`
- **Tujuan**: Menerapkan logika percabangan untuk mengevaluasi input pengguna.
- **Penjelasan**:
  - Menggunakan `prompt()` untuk meminta pengguna memasukkan nilai numerik.
  - Menggunakan pernyataan `if-else` untuk memeriksa apakah nilai lebih besar dari 75.
  - Menampilkan pesan alert "Lulus! Power level meningkat!!" jika nilai > 75, atau "Bro is cooked... tapi jangan menyerah!" jika nilai ≤ 75.
- **Catatan**: Input dari `prompt()` adalah string, sehingga tidak perlu konversi ke number karena perbandingan numerik dalam JavaScript akan melakukan konversi implisit.
- **Contoh Kode**:
  ```javascript
  function cekNilai() {
    const nilai = prompt("Masukkan Nilai Kamu:");
    if (nilai > 75) alert("Lulus! Power level meningkat!!");
    else alert("Bro is cooked... tapi jangan menyerah!");
  }
  ```

### 3. Fungsi `tampilArray()`
- **Tujuan**: Menampilkan elemen-elemen array dalam format yang rapi.
- **Penjelasan**:
  - Mendefinisikan array `buah` yang berisi string: `["Apel", "Jeruk", "Mangga", "Pisang"]`.
  - Menggunakan metode `join(", ")` untuk menggabungkan elemen array menjadi string dengan pemisah koma.
  - Menampilkan hasilnya dalam alert.
  - **Contoh Output**: `Daftar buah:\nApel, Jeruk, Mangga, Pisang`.
- **Catatan**: Metode `join()` adalah cara efisien untuk menampilkan array dalam format yang mudah dibaca.
- **Contoh Kode**:
  ```javascript
  function tampilArray() {
    const buah = ["Apel", "Jeruk", "Mangga", "Pisang"];
    alert("Daftar buah:\n" + buah.join(", "));
  }
  ```

### 4. Fungsi `hitung(operasi)`
- **Tujuan**: Melakukan operasi matematika dasar berdasarkan input pengguna.
- **Penjelasan**:
  - Mengambil nilai dari dua input (`angka1` dan `angka2`) menggunakan `document.getElementById()` dan mengonversinya ke number dengan `parseFloat()`.
  - Memeriksa apakah input valid (bukan `NaN`). Jika tidak valid, menampilkan pesan "Masukkan dua angka dulu!".
  - Berdasarkan parameter `operasi` (`tambah`, `kurang`, `kali`, `bagi`), menghitung hasil:
    - Penjumlahan: `a + b`
    - Pengurangan: `a - b`
    - Perkalian: `a * b`
    - Pembagian: `a / b`, dengan pengecekan untuk mencegah pembagian dengan nol.
  - Menampilkan hasil di elemen dengan id `hasil` menggunakan `textContent`.
- **Catatan**: Validasi input penting untuk mencegah error, dan pengecekan pembagian dengan nol mencegah hasil `Infinity`.
- **Contoh Kode**:
  ```javascript
  function hitung(operasi) {
    const a = parseFloat(document.getElementById("angka1").value);
    const b = parseFloat(document.getElementById("angka2").value);
    const hasil = document.getElementById("hasil");
    let teks = "";
    if (isNaN(a) || isNaN(b)) teks = "Masukkan dua angka dulu!";
    else {
      if (operasi === "tambah") teks = `Hasil: ${a + b}`;
      else if (operasi === "kurang") teks = `Hasil: ${a - b}`;
      else if (operasi === "kali") teks = `Hasil: ${a * b}`;
      else if (operasi === "bagi") teks = b !== 0 ? `Hasil: ${a / b}` : "Tidak bisa bagi 0!";
    }
    hasil.textContent = teks;
  }
  ```

### 5. Fungsi `animateCircle()`
- **Tujuan**: Membuat animasi sederhana dengan mengubah posisi dan warna elemen lingkaran.
- **Penjelasan**:
  - Mengambil elemen lingkaran (`id="circle"`) menggunakan `document.getElementById()`.
  - Memilih warna acak dari array `colors` (`blue`, `red`, `cyan`, `yellow`) menggunakan `Math.random()` dan `Math.floor()`.
  - Menghitung jarak translasi acak (`randomDistance`) berdasarkan lebar jendela (`window.innerWidth`) untuk memastikan lingkaran tetap dalam batas layar.
  - Mengubah properti CSS `transform` untuk memindahkan lingkaran secara horizontal dan `background` untuk mengubah warna.
- **Catatan**: Animasi ini sederhana dan tidak menggunakan CSS transition. Untuk efek yang lebih halus, dapat ditambahkan properti `transition` di CSS.
- **Contoh Kode**:
  ```javascript
  function animateCircle() {
    const circle = document.getElementById("circle");
    const colors = ["blue", "red", "cyan", "yellow"];
    const randomColor = colors[Math.floor(Math.random() * colors.length)];
    const maxTranslate = (window.innerWidth - 100) / 2;
    const randomDistance = Math.random() * maxTranslate * (Math.random() < 0.5 ? 1 : -1);
    circle.style.transform = `translateX(${randomDistance}px)`;
    circle.style.background = randomColor;
  }
  ```

### 6. Fungsi `updateCounter(operation)`
- **Tujuan**: Mengelola nilai counter yang ditampilkan di halaman.
- **Penjelasan**:
  - Menggunakan variabel global `counterValue` untuk menyimpan nilai counter (awalnya 0).
  - Berdasarkan parameter `operation` (`tambah` atau `kurang`), menambah atau mengurangi `counterValue`.
  - Memperbarui teks di elemen dengan id `counter` menggunakan `textContent`.
- **Catatan**: Penggunaan variabel global seperti `counterValue` dapat dihindari dengan pendekatan yang lebih modern seperti state management, tetapi untuk proyek sederhana ini sudah cukup.
- **Contoh Kode**:
  ```javascript
  let counterValue = 0;
  function updateCounter(operation) {
    const counter = document.getElementById("counter");
    if (operation === "tambah") counterValue++;
    else if (operation === "kurang") counterValue--;
    counter.textContent = counterValue;
  }
  ```
