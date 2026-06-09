---
template: claudecode-deck
title: "Prompt Engineering untuk Pemula"
subtitle: "Modul 2"
author: "Anggraeni Wisono"
date: auto
version: "v1.0"
---

<!-- _class: cover -->

###### Pelatihan AI · Modul 2

# Prompt Engineering *untuk Pemula*

Belajar berbicara dengan AI agar hasilnya jelas, akurat, dan siap pakai.

Durasi 45–60 menit

---

<!-- _class: agenda -->

###### Tujuan Pembelajaran

# Setelah sesi ini, peserta *mampu*…

- **Memahami prompt** Tahu apa itu prompt dan mengapa penting.
- **Menulis lebih jelas** Menyusun prompt yang efektif.
- **Jawaban akurat** Mendapat hasil AI yang lebih tepat.
- **Kurangi kesalahan** Menghindari jawaban yang terlalu umum.
- **Pakai sehari-hari** Memakai AI untuk pekerjaan nyata.

---

<!-- _class: stack -->

###### Mengapa Prompt Penting?

# Hasil AI = kualitas *prompt* Anda.

![Garbage in, garbage out: prompt yang kabur menghasilkan jawaban generik, sedangkan prompt yang jelas dan lengkap menghasilkan jawaban relevan dan siap pakai.](/Users/harry/project/ai-fundamental/modul-2/diagrams/gigo.svg)

> Dua orang memakai AI yang sama bisa mendapat hasil berbeda — yang membedakan adalah **prompt**-nya. *Garbage in, garbage out.*

---

###### Apa Itu Prompt?

# Prompt adalah *instruksi* untuk AI.

Prompt adalah perintah yang Anda berikan kepada AI. AI menjawab persis sesuai instruksi — jadi semakin jelas perintahnya, semakin baik hasilnya.

> Contoh paling sederhana: "Buat email kepada pelanggan." AI langsung mengerjakannya.

---

<!-- _class: procon -->

###### Buruk vs Baik

# Satu kalimat mengubah *segalanya*.

- **✗ Prompt buruk** "Buat proposal." — Proposal apa? Untuk siapa? Berapa halaman? Apa tujuannya? AI hanya bisa menebak.
- **✓ Prompt lebih baik** "Buat proposal pelatihan AI Fundamental untuk perusahaan retail, durasi 1 hari, bahasa profesional, maksimal 2 halaman."

---

<!-- _class: stack -->

###### Formula Prompt

# Empat bahan, satu *resep*.

![Formula prompt: Role + Task + Context + Output menghasilkan prompt berkualitas.](/Users/harry/project/ai-fundamental/modul-2/diagrams/formula-rtco.svg)

> **Role + Task + Context + Output** — pola sederhana yang bisa Anda pakai untuk hampir semua kebutuhan.

---

<!-- _class: pillars -->

###### Membongkar Formula

# Apa isi tiap *bagian*.

- **Role** Siapa yang AI perankan? Marketing Manager, HR, Customer Service, Trainer.
- **Task** Apa yang dikerjakan? Membuat email, laporan, proposal, SOP.
- **Context** Info tambahan: nama perusahaan, target audiens, produk, situasi.
- **Output** Format hasil: tabel, bullet point, email, presentasi, ringkasan.

---

<!-- _class: stack -->

###### Contoh Lengkap

# Satu prompt, *empat* bagian.

![Anatomi prompt: 'Anda adalah HR Manager' (Role), 'buatkan pengumuman internal' (Task), 'kebijakan WFO 3 hari per minggu' (Context), 'bahasa formal maksimal 300 kata' (Output).](/Users/harry/project/ai-fundamental/modul-2/diagrams/prompt-anatomy.svg)

---

<!-- _class: iconcards -->

###### Teknik Prompting

# Cara membuat prompt *lebih tajam*.

- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-context.svg) **Konteks** Beri info yang cukup — AI bukan pembaca pikiran.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-audience.svg) **Audiens** Untuk siswa SMA? Untuk direktur? Sebutkan.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-format.svg) **Format** Tabel, 5 poin, atau 5 slide.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-style.svg) **Gaya bahasa** Profesional untuk LinkedIn, santai untuk sosmed.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-example.svg) **Contoh (Few-Shot)** Beri contoh gaya yang Anda mau.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-steps.svg) **Bertahap (CoT)** Minta AI berpikir langkah demi langkah.

---

<!-- _class: procon -->

###### Teknik 1 · Konteks

# AI bukan *pembaca pikiran*.

- **✗ Terlalu umum** "Buat email penawaran." — jawaban melebar dan generik.
- **✓ Berkonteks** "Buat email penawaran pelatihan AI Fundamental kepada perusahaan manufaktur dengan sekitar 30 peserta."

---

<!-- _class: cards3 -->

###### Teknik 3 · Format Output

# Sebutkan *bentuk* yang Anda mau.

- **Tabel** "Ringkas dokumen berikut dalam bentuk tabel."
- **5 Poin** "Ringkas dokumen berikut dalam 5 poin utama."
- **Presentasi** "Ringkas dokumen berikut menjadi presentasi 5 slide."

---

<!-- _class: pillars -->

###### Teknik 2 & 4 · Audiens & Gaya

# Sasaran dan *nada* menentukan hasil.

- **Tentukan audiens** "Jelaskan AI kepada siswa SMA" ≠ "kepada direktur yang belum pernah memakai AI." Hasil menyesuaikan.
- **Tentukan gaya** "Artikel AI gaya profesional untuk LinkedIn" vs "gaya santai untuk media sosial."

---

<!-- _class: pillars -->

###### Teknik 5 & 6 · Contoh & Bertahap

# Beri *contoh*, minta *langkah*.

- **Few-Shot Prompting** "Berikut contoh email yang saya sukai — gunakan gaya yang sama." AI sangat menyukai contoh.
- **Chain-of-Thought** "Analisis masalah ini langkah demi langkah sebelum memberi rekomendasi." Hasil jadi lebih terstruktur.

---

###### Teknik 7 · Partner Diskusi

# Jadikan AI *teman berpikir*.

Jangan hanya meminta jawaban jadi — ajak AI berdiskusi agar Anda berpikir lebih tajam.

> "Bertindak sebagai konsultan bisnis. Ajukan **5 pertanyaan** yang perlu saya jawab sebelum membuat strategi pemasaran."

---

<!-- _class: pillars -->

###### Kesalahan Umum

# Yang membuat hasil jadi *generik*.

- **✗ Terlalu singkat** "Buat laporan."
- **✗ Tanpa konteks** "Buat strategi."
- **✗ Tanpa target** "Buat artikel."
- **✗ Tanpa format** "Ringkas ini."

---

<!-- _class: iconcards -->

###### Studi Kasus

# Prompt nyata di *tempat kerja*.

- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-cs.svg) **Customer Service** "Anda CS travel — jawab pertanyaan perubahan jadwal, sopan & profesional." Konsisten, cepat.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-hr.svg) **HR** "Anda HR Manager — buat job description AI Trainer, min. 2 tahun." Hemat waktu menyusun dokumen.
- ![](/Users/harry/project/ai-fundamental/modul-2/diagrams/ic-sales.svg) **Sales** "Anda Sales Consultant — proposal singkat pelatihan AI untuk 50 karyawan." Draft lebih cepat.

---

###### Latihan Bersama

# Perbaiki prompt ini *bersama*.

Mulai dari prompt mentah — lalu tambahkan **Role + Task + Context + Output**.

> Prompt awal: "Buat email kepada pelanggan." → **Hasil perbaikan:** "Anda adalah Customer Service perusahaan travel. Buat email kepada pelanggan yang penerbangannya berubah jadwal. Bahasa sopan & profesional, maksimal 200 kata."

---

<!-- _class: pillars -->

###### Template Siap Pakai

# Tinggal *isi kurung*.

- **Email** Anda adalah [jabatan]. Buat email tentang [topik] untuk [audiens]. Bahasa [formal/santai], maksimal [jumlah] kata.
- **Proposal** Anda konsultan bisnis. Buat proposal [topik] untuk [target] dalam format profesional.
- **Ringkasan** Ringkas dokumen berikut menjadi 5 poin utama dan sertakan rekomendasi tindakan.
- **Presentasi** Buat outline presentasi 10 slide tentang [topik] untuk [audiens].

---

<!-- _class: procon -->

###### Bukan Kata Ajaib

# Bukan mantra, tapi *kejelasan*.

- **✗ Yang dicari orang** Prompt rahasia, prompt viral, prompt "super canggih".
- **✓ Yang sebenarnya penting** Tujuan jelas, konteks lengkap, format jelas, dan iterasi—perbaikan.

---

###### Menuju NotebookLM

# AI belum tahu *dokumen Anda*.

Sampai tahap ini AI hanya mengandalkan pengetahuan umum — ia tidak tahu dokumen, SOP, atau kebijakan perusahaan Anda.

> Solusinya: **NotebookLM** — AI yang bekerja berdasarkan dokumen yang Anda miliki sendiri.

---

<!-- _class: cards3 -->

###### Workshop Praktik · 10–15 Menit

# Buat *tiga* prompt Anda.

- **Pekerjaan harian** Satu tugas rutin yang sering menyita waktu Anda.
- **Email** Satu email yang biasa Anda kirim.
- **Ringkasan** Sebuah laporan atau ringkasan.

---

<!-- _class: stack -->

###### Peta Pelatihan

# Anda di *Modul 2*.

![Peta pelatihan: Modul 1 AI Fundamental selesai, Modul 2 Prompt Engineering sedang berjalan, dilanjutkan Modul 3 NotebookLM dan Modul 4 Workshop.](/Users/harry/project/ai-fundamental/modul-2/diagrams/roadmap-m2.svg)

---

<!-- _class: closing -->

###### Terima Kasih

# Prompt yang jelas, hasil yang *tajam*.

Selanjutnya — Modul 3: NotebookLM Fundamental & Knowledge Management.
