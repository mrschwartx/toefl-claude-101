# Step Membuat Course Materials di Claude Chat

Panduan langkah demi langkah untuk membuat materi kursus TOEFL dalam format Markdown (.md), dari silabus sampai paket zip.

---

## Ringkasan Alur

```
Lampirkan skill → Silabus → Materi percobaan → Revisi → Buat berurutan
→ Uji kualitas → Index → Kemas zip → Perbarui dari error log
```

---

## Step 1: Siapkan Chat dan Lampirkan Skill

Buat chat baru, lampirkan `SKILL.md`, lalu kirim:

```
Ikuti skill terlampir. Kamu adalah guru bahasa Inggris untuk persiapan TOEFL.
Kita akan membuat course materials dalam format Markdown (.md), satu file per topik.
Penjelasan dalam Bahasa Indonesia, contoh dan soal dalam bahasa Inggris.
Konfirmasi dulu bahwa kamu paham aturannya, lalu tunggu instruksi saya.
```

---

## Step 2: Susun Silabus (Daftar Topik)

```
Buatkan silabus lengkap untuk level [Basic/Intermediate/Advanced/TOEFL Prep].
Format tabel: nomor, skill, topik, durasi, prasyarat.
Urutkan dari paling dasar ke paling sulit, dan seimbangkan 6 skill
(Grammar, Vocabulary, Listening, Reading, Speaking, Writing).
Jangan buat materinya dulu.
```

Periksa daftarnya. Jika ada yang kurang, minta: "Tambahkan topik X" atau "Hapus topik Y".

---

## Step 3: Buat Satu Materi Percobaan

Jangan langsung membuat semuanya. Buat satu dulu untuk mengecek kualitas:

```
Dari silabus tadi, buatkan materi nomor 1 secara lengkap sesuai struktur di skill.
Simpan sebagai file .md dengan nama 01-[level]-[skill]-[topik].md.
```

---

## Step 4: Review dan Revisi

Baca hasilnya, lalu beri masukan:

```
Revisi materi tadi:
- [contoh: tambah contoh yang lebih sederhana]
- [contoh: soal terlalu mudah, naikkan sedikit]
- [contoh: tambah kesalahan umum siswa Indonesia]
Simpan ulang dengan nama file yang sama.
```

Jika hasilnya sudah sesuai, lanjut ke step berikutnya.

---

## Step 5: Buat Materi Secara Berurutan

```
Gaya materi 1 sudah bagus. Buatkan materi nomor 2 sampai 5 dengan standar yang sama.
Satu file per materi, nama file berurutan.
```

Kerjakan 3-5 materi per permintaan agar kualitas tetap terjaga.

---

## Step 6: Uji Kualitas

```
Periksa semua materi yang sudah dibuat dengan checklist kualitas di skill:
soal orisinal, ada kunci jawaban, tingkat kesulitan konsisten, tidak ada bagian kosong.
Sebutkan masalah yang ditemukan dan perbaiki.
```

---

## Step 7: Buat Daftar Isi

```
Buatkan 00-index.md berisi daftar isi semua materi dengan tautan relatif,
dikelompokkan per level dan skill, plus urutan belajar yang disarankan.
```

---

## Step 8: Kemas dan Simpan

```
Kemas semua file .md ke folder dengan struktur 01-basic, 02-intermediate,
03-advanced, 04-toefl-prep, tambahkan .gitkeep di setiap folder, lalu kirim dalam zip.
```

Ekstrak hasilnya ke folder `03-materials/` di paket `toefl-claude-101`.

---

## Step 9: Perbarui Berkala

Setelah belajar beberapa minggu:

```
Berdasarkan kesalahan saya selama ini: [tempel isi error log],
buatkan materi tambahan untuk memperkuat kelemahan saya.
```

---

## Checklist Progres

- [ ] Step 1: Skill terlampir dan dikonfirmasi
- [ ] Step 2: Silabus disetujui
- [ ] Step 3: Materi percobaan dibuat
- [ ] Step 4: Revisi selesai
- [ ] Step 5: Seluruh materi dibuat
- [ ] Step 6: Uji kualitas lulus
- [ ] Step 7: `00-index.md` dibuat
- [ ] Step 8: Zip dikemas dan disimpan
- [ ] Step 9: Materi tambahan dari error log (berkala)

---

## Tips

- Gunakan satu chat untuk satu level agar gaya tetap konsisten.
- Jika chat sudah sangat panjang, mulai chat baru: lampirkan `SKILL.md` dan `00-index.md`, lalu tulis "Lanjutkan dari materi nomor N".
- Untuk materi Listening, Claude membuat transcript. Kamu bisa membacanya sendiri atau memakai fitur text-to-speech di perangkatmu.
- Format dan skor TOEFL bisa berubah. Cek situs resmi ETS untuk informasi terbaru.
