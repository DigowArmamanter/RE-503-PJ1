# Praktik Terpadu YOLO: Joel Mark Rodrigo Purba (4222401008)

## Dataset
- Sumber: Roboflow Universe, image-detection-qixfs v9 (deteksi huruf/angka dan panah)
- 2 kelas: `huruf_angka`, `panah`. Dibagi per sesi foto (anti kebocoran) dengan proporsi sekitar 70/20/10.
- Model dasar: `yolo26n`, epoch 30, imgsz 416. Perubahan E3: `imgsz=640`.

## Hasil eksperimen (data VAL)
| eksperimen    | perubahan   | pretrained   |   mAP50 |   mAP50-95 |   precision |   recall |   inferensi_ms |   waktu_latih_menit |   imgsz |
|:--------------|:------------|:-------------|--------:|-----------:|------------:|---------:|---------------:|--------------------:|--------:|
| E1_pretrained | -           | True         |  0.995  |     0.9485 |      0.9851 |   0.9979 |           2.58 |                5.76 |     416 |
| E2_scratch    | -           | False        |  0.9945 |     0.9212 |      0.9919 |   0.9817 |           2.36 |                5.63 |     416 |
| E3_tuning     | imgsz=640   | True         |  0.995  |     0.9447 |      0.9959 |   0.9992 |           5.29 |                7.93 |     640 |

## Hasil uji (data TEST, sekali saja)
- Model terpilih (mAP50-95 val tertinggi): E1_pretrained
- Hasil di data TEST (sekali saja)       : mAP50 0.995 | mAP50-95 0.944

## Analisis
> Tulis dengan kata-katamu sendiri. Pertanyaan pemandu (hapus setelah selesai):
> 1. E1 (pretrained) vs E2 (scratch): mana lebih baik, selisihnya berapa, dan mengapa transfer learning membantu?
> 2. E3: perubahan apa yang dilakukan, dan apakah mAP naik/turun? Apa harganya (waktu latih, kecepatan inferensi)?
> 3. Model mana yang terpilih berdasarkan VAL, dan apakah hasil TEST-nya sejalan?
> 4. Kelas mana yang lebih sulit (lihat confusion matrix)? Dugaan penyebab: jumlah data panah jauh lebih sedikit, objek kecil, cahaya redup/gelap.
> 5. Keterbatasan dan saran perbaikan.

TULIS ANALISISMU DI SINI.
