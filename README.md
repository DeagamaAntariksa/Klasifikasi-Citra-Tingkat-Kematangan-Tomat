
# Klasifikasi-Citra-Tingkat-Kematangan-Tomat-CNN

1. TERDAPAT 3 GAMBAR TOMAT YANG TELAH DIBAGI, MATANG, MENTAH DAN SETENGAH MATANG 

![output](https://github.com/DeagamaAntariksa/Klasifikasi-Citra-Tingkat-Kematangan-Tomat/assets/81089892/7c79e1b2-02b1-4bc3-b97c-c487beef9a8d)

2. Selanjutnya melakukan proses preprocessing data yang dimana sebagai berikut
   - Dataset buah tomat dibagi menjadi tiga kategori (Matang, Mentah, Setengah Matang).
   - Gambar-gambar pada setiap kategori diresize menjadi ukuran 100x100 piksel.
   - Fitur gambar (X) dan label kategori (y) disimpan dalam list terpisah.
   - Nilai piksel gambar dinormalisasi ke rentang 0-1.
   - Label kategori diubah menjadi bilangan bulat menggunakan LabelEncoder.
   - Data dibagi menjadi set pelatihan (X_train, y_train) dan pengujian (X_test, y_test).
   - Label kategori diubah menjadi one-hot encoding menggunakan to_categorical.
4. Pembangunan Model CNN
   - Model CNN terdiri dari beberapa layer Conv2D, MaxPooling2D, dan Dense.
   - Model menggunakan fungsi aktivasi 'relu' pada layer Conv2D dan Dense terakhir menggunakan 'softmax'.
   - Model dikompilasi dengan menggunakan categorical_crossentropy sebagai fungsi loss dan optimizer 'adam'.
6. Melatih Model CNN
   - Model dilatih dengan menggunakan data pelatihan (X_train, y_train_encoded).
   - Pelatihan dilakukan selama 4 epoch dengan batch size 32.
   - Evaluasi model dilakukan pada set pengujian (X_test, y_test_encoded).
8. Visualisasi Akurasi dan Loss
   - Visualisasi grafik loss selama pelatihan model.
   
   ![out2put](https://github.com/DeagamaAntariksa/Klasifikasi-Citra-Tingkat-Kematangan-Tomat/assets/81089892/35aba1a7-bfc2-4260-a340-b149ed60c80c)

   Grafik loss menunjukkan perubahan nilai loss pada set pelatihan dan pengujian.


   - Visualisasi grafik akurasi selama pelatihan model.
   ![output3](https://github.com/DeagamaAntariksa/Klasifikasi-Citra-Tingkat-Kematangan-Tomat/assets/81089892/c409228f-ad3c-4b8c-8188-93bec028caa2)
   
   Grafik akurasi menunjukkan perubahan nilai akurasi pada set pelatihan dan pengujian.

10. Evaluasi Model
    Loss pada data uji adalah 0.1185 dan akurasi adalah 0.9756.
13. Testing:
    - Dilakukan pengujian model pada data baru (new_data_path) dengan melakukan prediksi kategori.
    - Gambar baru yang diuji ditampilkan beserta label hasil prediksi.
   



