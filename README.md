# 🏋️‍♂️ SUMMITS Operations & Member Exercise Analytics (SQL)

## 📌 Project Overview
Project ini berfokus pada analisis data operasional dan perilaku latihan member di **SUMMITS Fitness Center**. Menggunakan database MySQL, analisis ini mengevaluasi tren olahraga terfavorit, pengeluaran kalori berdasarkan gender, performa kardio, serta segmentasi komposisi tubuh member untuk mengoptimalkan strategi bisnis, penempatan fasilitas gym, dan efisiensi program *Personal Trainer (PT)*.

## 🛠️ Tech Stack & Tools
- **Database Server:** MySQL
- **Query Tool:** MySQL Workbench
- **Dataset:** Gym Members Exercise Tracking (Kaggle)

---

## 📝 Business Questions & Insights

### 1. Analisis Pembakaran Kalori Berdasarkan Gender
**Pertanyaan:** Kelompok mana yang membakar kalori lebih banyak per sesi latihan?

| Gender | Rata-Rata Kalori Terbakar |
| :--- | :--- |
| **Male** | 944.46 kcal |
| **Female** | 862.25 kcal |

**Business Insight:** Member pria rata-rata membakar kalori ~9.5% lebih tinggi per sesi. Tim operasional dapat memanfaatkan data ini untuk menyesuaikan asupan hidrasi gratis atau suplemen yang disediakan di bar gym berdasarkan segmentasi demografis harian.

---

### 2. Segmentasi Jenis Latihan Terpopuler
**Pertanyaan:** Apa jenis latihan yang paling banyak diminati oleh member?

| Workout Type | Jumlah Member |
| :--- | :--- |
| **Strength** | 258 |
| **Cardio** | 255 |
| **Yoga** | 239 |
| **HIIT** | 221 |

**Business Insight:** Area *Strength Training* (Angkat Beban) dan *Cardio* menempati urutan teratas. Rekomendasi bisnis: Prioritaskan alokasi anggaran perawatan berkala untuk mesin treadmill dan pastikan variasi dumbbell/plat beban selalu tercukupi agar member tidak mengantre saat *peak hours*.

---

### 3. Analisis Karakteristik Member Aktif (> 3 Hari/Minggu)
**Pertanyaan:** Bagaimana durasi latihan dan performa detak jantung rata-rata dari member yang rajin?

| Rata-Rata BPM | Rata-Rata Durasi Latihan |
| :--- | :--- |
| 143.41 BPM | 1.49 Jam (~90 Menit) |

**Business Insight:** Member aktif menghabiskan waktu rata-rata 1,5 jam dengan intensitas latihan di zona kardio aktif (143 BPM). Ini adalah target pasar potensial bagi *Personal Trainer* untuk menawarkan program lanjut (*advanced program*) karena tingkat komitmen mereka sudah tinggi.

---

### 4. Segmentasi Persentase Lemak untuk Berat Badan > 70 kg
**Pertanyaan:** Berapa rata-rata persentase lemak tubuh berdasarkan gender untuk member berbobot di atas 70 kg?

| Gender | Rata-Rata Persentase Lemak |
| :--- | :--- |
| **Male** | 21.75% |
| **Female** | 30.07% |

**Business Insight:** Data ini memberikan basis bagi klub untuk merancang *Fat Loss Challenge* yang spesifik dan terukur, disesuaikan dengan profil komposisi tubuh rata-rata member berbobot besar.

---

### 5. Tren Latihan Anak Muda (< 25 Tahun) & Kesehatan Jantung
**Pertanyaan:** Apa jenis latihan yang disukai anak muda dan bagaimana kondisi kesehatan jantung mereka saat istirahat (*Resting BPM*)?

| Workout Type | Jumlah Member Muda | Rata-Rata Resting BPM |
| :--- | :--- | :--- |
| **Cardio** | 47 | 63.57 BPM |
| **HIIT** | 43 | 62.77 BPM |
| **Strength** | 38 | 62.08 BPM |
| **Yoga** | 37 | 59.08 BPM |

**Business Insight:** Mayoritas anak muda di bawah 25 tahun lebih menyukai latihan dinamis (*Cardio* & *HIIT*). Indikator *Resting BPM* mereka yang berkisar di angka 59-63 BPM menandakan bahwa fungsi kardiovaskular kelompok usia ini di gym SUMMITS dalam kondisi sangat atletis dan prima.

---

## 📂 File Structure
- `gym_analytics_queries.sql` : File mentah berisi seluruh query SQL yang digunakan untuk analisis.
- `README.md` : Dokumentasi analisis proyek dan kesimpulan bisnis.
