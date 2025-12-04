ZAKAT & INFAQ CALCULATOR

🕌 Aplikasi Perhitungan Infaq, Zakat Mal, dan Zakat Fitrah

![Zakat & Donasi Banner](https://github.com/rafi-zimraan/Elementory-Wordpress-BPD/blob/main/assets/backgroundApp.png)


Aplikasi berbasis HTML + CSS + JavaScript yang membantu pengguna menghitung kewajiban zakat serta infaq secara cepat dan akurat.

Aplikasi ini cocok digunakan untuk personal, komunitas, ataupun lembaga seperti masjid, karena seluruh fitur berjalan secara offline tanpa memerlukan backend.

🎯 Tentang Aplikasi

Aplikasi ini menyediakan fitur:

1. Perhitungan Infaq

Pengguna cukup memasukkan nominal yang ingin di-infaqkan.

Hasil ditampilkan secara instan.

2. Perhitungan Zakat Mal

Menghitung zakat 2.5% (1/40) dari total harta.

Mendukung perhitungan:

Harta tunai

Tabungan

Emas / setara emas

Hutang yang jatuh tempo

Memungkinkan input nisab dalam rupiah sesuai standar setempat.

Memberikan hasil: apakah harta sudah mencapai nisab dan berapa zakat wajibnya.

3. Perhitungan Zakat Fitrah

Bisa dihitung dengan metode:

Beras (kg) → total jiwa × 2.5 kg (default)

Uang → total jiwa × nominal per jiwa

Fleksibel untuk standar harga beras atau nominal zakat per jiwa.

🌐 Teknologi yang Digunakan

HTML5 (struktur aplikasi)

CSS / Tailwind (opsional) untuk tampilan

JavaScript murni untuk logika perhitungan

Tidak membutuhkan backend atau build tool — cukup buka index.html.

📂 Struktur Project
/ (root)
├─ index.html
├─ css/
│  └─ styles.css
├─ js/
│  └─ kalkulator.js
└─ assets/
   └─ banner-zakat.jpg

⚙️ Fitur Utama

✔ Kalkulator Infaq
✔ Kalkulator Zakat Mal (otomatis cek nisab)
✔ Kalkulator Zakat Fitrah (beras / rupiah)
✔ Tombol reset & validasi input
✔ Output siap salin atau dicetak

📐 Rumus Perhitungan
Zakat Mal
Jika harta bersih ≥ nisab :
    zakat = 2.5% × harta bersih


2.5% = 1/40

Zakat Fitrah — Metode Beras
total_kg = jumlah_jiwa × 2.5 kg
total_rupiah = total_kg × harga_beras_per_kg

Zakat Fitrah — Metode Uang
total_rupiah = jumlah_jiwa × nominal_per_jiwa

Infaq
nominal = sesuai input pengguna

🚀 Cara Menjalankan Project

Karena aplikasi ini berbasis HTML murni, cara menjalankannya sangat mudah.

1. Clone Repository
git clone https://github.com/rafi-zimraan/portofolio.git zakat-infaq

2. Masuk Folder
cd zakat-infaq

3. Jalankan Aplikasi

Cukup buka file berikut di browser:

index.html


Atau lewat terminal:

Windows

start index.html


macOS/Linux

open index.html


Tidak perlu npm install, npm run dev, atau server apapun.

🧩 Contoh Fungsi Perhitungan (JavaScript)
// Zakat Mal
function hitungZakatMal(harta, nisab) {
  const wajib = harta >= nisab;
  const zakat = wajib ? harta * 0.025 : 0;
  return { wajib, zakat: Math.round(zakat) };
}

// Zakat Fitrah
function hitungZakatFitrah(jiwa, metode, takaran, harga) {
  if (metode === "beras") {
    const totalKg = jiwa * takaran;
    const totalRupiah = totalKg * harga;
    return { totalKg, totalRupiah };
  }
  return { totalRupiah: jiwa * harga };
}

// Infaq
function hitungInfaq(nominal) {
  return Number(nominal);
}

🔧 Pengembangan & Customisasi

Ubah takaran fitrah (default 2.5 kg) sesuai aturan setempat.

Ubah nilai nisab pada input atau tetapkan nilai default di JavaScript.

Tambahkan lokalisasi rupiah, format angka, atau animasi UI.

Dapat dikembangkan menjadi PWA agar bisa offline sepenuhnya.

🤝 Kontribusi

Kontribusi terbuka!

Fork repository ini

Tambahkan fitur pada branch baru

Buat pull request

📜 License

Lisensi bebas (MIT / Open Source) — sesuaikan dengan kebutuhan Anda.
