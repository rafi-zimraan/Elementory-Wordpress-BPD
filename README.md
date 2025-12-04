ZAKAT & INFAQ CALCULATOR

🕌 Aplikasi Perhitungan Infaq, Zakat Mal, dan Zakat Fitrah

![Zakat & Donasi Banner](https://github.com/rafi-zimraan/Elementory-Wordpress-BPD/blob/main/assets/backgroundApp.png)


Aplikasi berbasis HTML + CSS + JavaScript yang membantu pengguna menghitung kewajiban zakat serta infaq secara cepat dan akurat.

Aplikasi ini cocok digunakan untuk personal, komunitas, ataupun lembaga seperti masjid, karena seluruh fitur berjalan secara offline tanpa memerlukan backend.

🧰 Tech Stack

HTML5 (struktur halaman)

CSS / TailwindCSS (opsional untuk UI)

JavaScript murni (logika perhitungan)

No Framework, No Backend — berjalan offline dan ringan

🚀 Getting Started
1️⃣ Buka Aplikasi

Karena ini aplikasi HTML murni, tidak ada instalasi rumit.

Cukup buka:

index.html


Atau melalui command:

Windows

start index.html


macOS

open index.html

📦 Fitur Utama
✨ 1. Perhitungan Infaq

Pengguna cukup memasukkan nominal infaq.
Hasil langsung muncul tanpa proses tambahan.

✨ 2. Perhitungan Zakat Mal

Menghitung zakat sebesar 2.5% (1/40) dari total harta.

Komponen perhitungan yang didukung:

Harta tunai

Tabungan

Emas / setara emas

Hutang yang jatuh tempo

Fitur tambahan:

Input nisab dalam rupiah

Indikator apakah harta sudah mencapai nisab

Perhitungan zakat otomatis

✨ 3. Perhitungan Zakat Fitrah

Dapat dihitung dengan dua metode: beras dan uang.

📌 Metode Beras
total kg = jumlah jiwa × 2.5 kg
total rupiah = total kg × harga beras per kg

📌 Metode Uang
total rupiah = jumlah jiwa × nominal per jiwa


Fleksibel mengikuti standar daerah setempat.

📂 Struktur Project
/ (root)
├─ index.html
├─ css/
│  └─ styles.css
├─ js/
│  └─ kalkulator.js
└─ assets/
   └─ banner-zakat.jpg

🧮 Contoh Kode Perhitungan
Zakat Mal
function hitungZakatMal(harta, nisab) {
  const wajib = harta >= nisab;
  const zakat = wajib ? harta * 0.025 : 0;
  return { wajib, zakat: Math.round(zakat) };
}

Zakat Fitrah
function hitungZakatFitrah(jiwa, metode, takaran, harga) {
  if (metode === "beras") {
    const totalKg = jiwa * takaran;
    const totalRupiah = totalKg * harga;
    return { totalKg, totalRupiah };
  }
  return { totalRupiah: jiwa * harga };
}

Infaq
function hitungInfaq(nominal) {
  return Number(nominal);
}

🛠️ Cara Kustomisasi

Ubah nilai nisab sesuai ketentuan daerah

Ubah takaran fitrah (default 2.5 kg)

Pasang format angka rupiah

Tambah UI modern dengan Tailwind

Bisa dibuat PWA untuk digunakan offline

🤝 Kontribusi

Kontribusi sangat terbuka:

Fork repo

Buat branch

Ajukan pull request

📜 Lisensi

MIT License — bebas digunakan untuk keperluan apa pun.


