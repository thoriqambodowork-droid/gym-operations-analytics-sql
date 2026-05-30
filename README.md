-- ====================================================================
-- PROJECT: GYM MEMBER EXERCISE ANALYSIS (SUMMITS FITNESS CENTER)
-- ROLE: DATA ANALYST
-- TOOLS: MySQL WORKBENCH
-- ====================================================================

USE gym_db;

-- 1. Analisis Rata-Rata Kalori Terbakar Berdasarkan Gender
SELECT 
    Gender, 
    ROUND(AVG(CAST(`Calories_Burned` AS UNSIGNED)), 2) AS rata_rata_kalori
FROM gym_members_exercise_tracking
GROUP BY Gender;


-- 2. Analisis Jenis Latihan Terpopuler Berdasarkan Jumlah Member
SELECT 
    `Workout_Type`, 
    COUNT(*) AS jumlah_member
FROM gym_members_exercise_tracking
GROUP BY `Workout_Type`
ORDER BY jumlah_member DESC;


-- 3. Analisis Rata-Rata BPM dan Durasi Latihan untuk Member Aktif (> 3 hari/minggu)
SELECT 
    ROUND(AVG(CAST(`Avg_BPM` AS UNSIGNED)), 2) AS rata_rata_BPM,
    ROUND(AVG(CAST(`Session_Duration (hours)` AS DOUBLE)), 2) AS rata_rata_durasi_jam
FROM gym_members_exercise_tracking
WHERE CAST(`Workout_Frequency (days/week)` AS UNSIGNED) > 3;


-- 4. Analisis Rata-Rata Persentase Lemak Berdasarkan Gender untuk Member Berat > 70 kg
SELECT 
    Gender, 
    ROUND(AVG(CAST(`Fat_Percentage` AS DOUBLE)), 2) AS rata_rata_lemak
FROM gym_members_exercise_tracking
WHERE CAST(`Weight (kg)` AS DOUBLE) > 70
GROUP BY Gender;


-- 5. Analisis Tren Jenis Latihan dan Rata-Rata Resting BPM untuk Member Muda (< 25 Tahun)
SELECT 
    `Workout_Type`,
    COUNT(*) AS jumlah_member_muda,
    ROUND(AVG(CAST(`Resting_BPM` AS UNSIGNED)), 2) AS rata_rata_resting_BPM
FROM gym_members_exercise_tracking
WHERE CAST(`Age` AS UNSIGNED) < 25
GROUP BY `Workout_Type`
ORDER BY jumlah_member_muda DESC;
