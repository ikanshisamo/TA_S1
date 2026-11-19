Agregasi antar seed (folder aggregate)
metrics_overall_mean_std.csv      mean, std (sampel), min, max, dan nilai tiap seed untuk metrik keseluruhan
metrics_per_class_mean_std.csv    precision/recall/f1 per kelas: mean, std, min, max, nilai tiap seed, support
confusion_matrix_sum.csv          jumlah confusion matrix semua seed (baris = kelas benar, kolom = prediksi)
confusion_matrix_mean.csv         rata-rata jumlah per sel antar seed
confusion_matrix_rownorm_mean.csv rata-rata proporsi per baris (diagonal = recall per kelas)
predictions_aggregate.csv         per gambar uji: prediksi dan benar/salah tiap seed, n_correct (berapa seed benar),
                                  all_seeds_agree, rata-rata probabilitas dan logit antar seed,
                                  ensemble_pred/ensemble_correct (argmax rata-rata probabilitas)
                                  CATATAN: ensemble_* adalah gabungan seed, BUKAN hasil satu model; jangan dibandingkan
                                  dengan metrik per seed. Uji McNemar dan bootstrap memakai prediksi per seed.
history_mean_std.csv              riwayat per epoch: mean dan std antar seed
