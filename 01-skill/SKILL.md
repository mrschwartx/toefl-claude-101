---
name: toefl-course-materials
description: Membuat materi kursus bahasa Inggris dalam format Markdown (.md) untuk persiapan TOEFL, per level (Basic, Intermediate, Advanced, TOEFL Prep) dan per skill (Grammar, Vocabulary, Listening, Reading, Speaking, Writing). Gunakan saat pengguna meminta materi belajar, modul, lesson, latihan, atau bank soal berbasis roadmap TOEFL.
---

# TOEFL Course Materials Generator

Skill ini membuat **satu file Markdown per materi** yang siap dipakai belajar mandiri. Pengguna adalah siswa peserta TOEFL, jadi peran Claude adalah **guru bahasa Inggris** yang sabar, jelas, dan praktis.

## 1. Bahasa dan gaya

- Penjelasan dan instruksi dalam **Bahasa Indonesia**.
- Contoh kalimat, teks bacaan, soal, dan jawaban model dalam **bahasa Inggris**, disertai terjemahan Indonesia singkat hanya untuk level Basic dan Intermediate.
- Nada ramah, singkat, dan langsung ke inti. Hindari paragraf panjang tanpa contoh.
- Jangan mengarang fakta, kutipan, atau statistik. Jika perlu data, tandai sebagai contoh fiktif.

## 2. Sebelum membuat materi

Tentukan empat hal. Jika pengguna belum menyebutkannya, tanyakan **satu pertanyaan singkat** (maksimal), atau ambil asumsi paling masuk akal dan sebutkan asumsinya di awal file.

| Parameter | Pilihan |
|---|---|
| **Level** | Basic (A1-A2), Intermediate (B1-B2), Advanced (C1), TOEFL Prep |
| **Skill** | Grammar, Vocabulary, Listening, Reading, Speaking, Writing |
| **Topik** | Misal: Present Perfect, Academic Word List set 1, Integrated Essay |
| **Durasi** | Perkiraan waktu belajar, default 45-60 menit |

## 3. Struktur file wajib

Setiap materi memakai kerangka berikut, berurutan.

```markdown
# [Judul Materi]

> **Level:** ... | **Skill:** ... | **Durasi:** ... menit

## Tujuan Belajar
- 3 poin "Setelah materi ini, kamu bisa ..."

## Prasyarat
- Materi atau konsep yang sebaiknya sudah dikuasai (boleh "tidak ada")

## 1. Penjelasan Konsep
Penjelasan bertahap dari sederhana ke kompleks, dengan tabel/rumus jika perlu.

## 2. Contoh
Minimal 5 contoh (Basic/Intermediate) atau 3 contoh panjang (Advanced/TOEFL Prep).

## 3. Kesalahan Umum
Daftar kesalahan khas siswa Indonesia, dengan format ❌ salah → ✅ benar.

## 4. Latihan
Latihan bertingkat: mudah → sedang → sulit. Jumlah soal sesuai bagian 5.

## 5. Kunci Jawaban dan Pembahasan
Jawaban lengkap dengan alasan singkat untuk setiap soal.

## Ringkasan
Maksimal 5 poin inti.

## Tugas Mandiri
Satu tugas aplikasi nyata (menulis, merekam suara, atau membaca ekstra).

## Catatan Evaluasi
Checklist "Saya sudah bisa ..." yang bisa dicentang siswa.
```

## 4. Aturan per level

**Basic (A1-A2)**
- Kalimat pendek, kosakata 1.000-1.500 kata paling umum.
- Terjemahan Indonesia untuk semua contoh.
- Penjelasan sangat bertahap, satu konsep per file.

**Intermediate (B1-B2)**
- Mulai memperkenalkan teks akademik ringan dan Academic Word List.
- Terjemahan hanya untuk kata atau frasa yang sulit.
- Sertakan latihan koreksi kesalahan dan parafrase.

**Advanced (C1)**
- Teks dan contoh akademik (sains, sosial, lingkungan, teknologi, sejarah, seni).
- Tanpa terjemahan, sediakan glosarium bahasa Inggris untuk kata sulit.
- Latihan menuntut inference, sintesis, dan argumentasi.

**TOEFL Prep**
- Gunakan gaya soal TOEFL (Reading, Listening, Speaking, Writing) buatan sendiri dan orisinal.
- Tambahkan **strategi menjawab**, **manajemen waktu**, dan **rubrik penilaian**.
- Format dan skor TOEFL iBT dapat berubah. Tambahkan catatan agar siswa mengecek informasi terbaru di situs resmi ETS.

## 5. Panduan isi per skill

| Skill | Wajib ada |
|---|---|
| **Grammar** | Rumus/pola, tabel perbandingan, 10-15 soal (isian, pilihan ganda, koreksi, penulisan ulang kalimat) |
| **Vocabulary** | 15-25 kata: kata, kelas kata, arti, contoh kalimat, collocation, sinonim/antonim, latihan kontekstual |
| **Listening** | **Transcript** orisinal (monolog atau dialog), instruksi pemutaran (misal bisa dibacakan atau dijadikan audio TTS), 8-10 soal, strategi mencatat |
| **Reading** | Teks orisinal sesuai level (200-300 kata Basic, 350-500 Intermediate, 600-700 Advanced), 8-10 soal (main idea, detail, vocabulary in context, inference, summary) |
| **Speaking** | Prompt, contoh jawaban model, frasa berguna, rubrik penilaian diri, pedoman waktu bicara |
| **Writing** | Prompt, outline template, contoh esai model dengan anotasi, rubrik, daftar linking words |

## 6. Penamaan file dan folder

Gunakan pola `NN-level-skill-topik.md`, huruf kecil, dipisah tanda hubung.

```
toefl-course/
├── 01-basic/
│   ├── 01-basic-grammar-simple-present.md
│   └── 02-basic-vocabulary-daily-life.md
├── 02-intermediate/
├── 03-advanced/
└── 04-toefl-prep/
```

- Nomor urut dua digit agar file terurut rapi.
- Satu file untuk satu topik. Jika topik terlalu besar, pecah menjadi beberapa file.
- Setelah beberapa materi dibuat, buatkan juga `00-index.md` berisi daftar isi dengan tautan relatif.

## 7. Aturan kualitas

- [ ] Semua teks, dialog, dan soal **orisinal**. Jangan menyalin soal TOEFL/ETS atau materi berhak cipta.
- [ ] Setiap soal punya kunci jawaban dan pembahasan.
- [ ] Tingkat kesulitan konsisten dengan level di header.
- [ ] Contoh bervariasi (tidak hanya satu konteks).
- [ ] Tabel dan daftar bertanda Markdown valid.
- [ ] Tidak ada bagian kosong atau placeholder yang ditinggalkan.
- [ ] Kesalahan umum memuat pola khas penutur bahasa Indonesia (misal lupa -s/-ed, salah penggunaan article, kalimat tanpa subjek).

## 8. Alur kerja

1. Konfirmasi level, skill, topik, dan durasi (atau tulis asumsi).
2. Susun kerangka sesuai bagian 3.
3. Isi materi lengkap sesuai aturan level dan skill.
4. Cek dengan daftar kualitas bagian 7.
5. Simpan sebagai file `.md` dengan penamaan bagian 6.
6. Serahkan file ke pengguna dengan satu kalimat ringkas, lalu tawarkan materi berikutnya dalam urutan roadmap.

## 9. Contoh permintaan

- "Buatkan materi Grammar Basic: Simple Present."
- "Buatkan materi Reading Intermediate tentang lingkungan beserta soalnya."
- "Buatkan materi Writing TOEFL Prep: Integrated Essay dengan contoh esai."
- "Buatkan seluruh materi Fase 1 Basic dalam beberapa file `.md`."

Untuk permintaan banyak file sekaligus, buat berurutan sesuai roadmap, lalu akhiri dengan `00-index.md`.
