Isi folder eksperimen
config.json            hyperparameter, seed, md5 file split, versi library, GPU
complexity.json        jumlah parameter, MACs per gambar 224x224, operasi elemen ECA
summary_seeds.csv      metrik utama per seed (ditulis di akhir)
seedN/predictions.csv  rel_path, y_true, y_pred, correct, logit_0..6, prob_0..6 (urutan = baris 'test' di CSV split)
seedN/metrics_overall.json   accuracy, macro-P/R/F1, loss(NLL), Brier, AUC, rata-rata epoch 91-100, waktu
seedN/metrics_per_class.csv  precision, recall, f1, support per kelas
seedN/confusion_matrix.csv   baris = kelas benar, kolom = kelas prediksi
seedN/history.csv      per epoch: train/test loss dan metrik, waktu epoch, memori GPU puncak (training)
seedN/model_final.pt   state_dict epoch 100 (jika SAVE_WEIGHTS)
seedN/gates_test.npz   nilai gerbang ECA tiap gambar uji per modul (float16), hanya varian ECA
seedN/gates_summary.json   statistik gerbang per modul (rata-rata, std, eta^2 antar kelas)
aggregate/summary_mean_std.csv        rata-rata, std (sampel, ddof=1), min, max antar seed untuk metrik keseluruhan
aggregate/per_class_mean_std.csv      precision, recall, F1 per kelas: rata-rata, std, min, max, dan nilai tiap seed
aggregate/confusion_matrix_sum.csv    confusion matrix dijumlahkan antar seed (juga _mean dan _row_normalized)
aggregate/seed_agreement.csv          tiap gambar uji: prediksi dan benar/salah per seed, proporsi seed yang benar
Catatan: uji statistik tingkat run memakai data per seed (seedN/), bukan agregat.
aggregate/             agregasi antar seed: mean/std metrik keseluruhan dan per kelas, confusion matrix (jumlah, rata-rata,
                       dinormalisasi), prediksi per gambar digabung, riwayat mean/std (lihat README_aggregate.txt di dalamnya)
