---
layout: post
author: "Rully Pratama"
date: 2025-06-21

title: "Mengapa Foto RAW yang Sama Terlihat Berbeda-beda?"

categories:
- Fotografi

published: true
---

Format RAW pasti bukan hal yang asing lagi bagi kalian yang menggeluti dunia fotografi. RAW memiliki kelebihan, diantaranya *shadow recovery* yang sangat baik, fleksibilitas dalam hal *color grading* maupun detail yang tidak bisa didapat pada format JPG. Beberapa kelebihan tersebut berkat RAW menyimpan data mentah dari foto yang diambil.

Analogi mentah untuk format RAW dan matang untuk format JPG sepertinya sangat cocok. Bayangkan saja makanan, apabila kalian mendapati makanan yang sudah matang, lalu makanan tersebut dibagi ke beberapa orang, maka rasa yang dirasakan masing-masing orang akan relatif sama.

Namun apabila bahan mentah yang dibagikan, maka masing-masing orang akan mengolahnya dengan cara masing-masing. Hasil dan cita rasanya pun bisa berbeda-beda, tergantung dari selera, pengalaman memasak, maupun bumbu-bumbu yang digunakan.

## Sedikit tentang cara kamera menangkap cahaya

![Bayer array filter](bayer_filter.avif)

Sensor adalah bagian kamera yang bertugas untuk menangkap cahaya. Namun sayangnya, sensor hanya bisa membedakan intensitas cahaya (terang/gelap) saja, tidak beserta informasi warna. Maka untuk mengatasi hal tersebut, dipasanglah Bayer filter di depan sensor.

Bayer filter berbentuk grid. Setengah dari jumlah grid berupa filter hijau, sementara setengah yang lain terdiri dari merah dan biru. Filter ini hanya mengizinkan cahaya yang berwarna sama untuk bisa diteruskan ke sensor. Dengan data ini nantinya sensor bisa menangkap informasi warna.

Tapi masalahnya, masing-masing pixel dibelakang filter, hanya memiliki informasi warna untuk 1 warna saja.

![Bayer array filter](raw_bayer_small.avif)

Proses demosaic diperlukan untuk mengubah informasi yang tadinya seperti mozaik (perhatikan spot hitam pada pixel di gambar), menjadi gambar dengan warna dan pencahayaan yang sesuai seperti seharusnya.

Demosaic hanya satu langkah dari beberapa *pipeline* yang harus ditempuh kamera untuk menangkap cahaya dan menjadikannya sebagai informasi digital. Ada white balance, color correction, gamma correction dan denoising. Masing-masing langkah apabila dilakukan dengan cara dan intensitas yang berbeda, maka akan menghasilkan gambar yang berbeda pula.

![Bayer array filter](camera_processing_pipeline_small.avif)

## Beda aplikasi, beda cara untuk memproses data RAW

[![Raw process result comparison](Raw_Comparison_small.avif)](Raw_Comparison.avif)

Ingat, bahwa foto RAW merupakan data hasil pembacaan sensor kamera yang masih benar-benar mentah. Aplikasi perlu mengaplikasikan *processing pipeline*-nya masing-masing untuk mengkonversi data bayer mentah menjadi foto yang berarti.

Di sini saya membandingkan 4 gambar, 1 hasil JPG dari kamera, 3 yang lain dari aplikasi yang berkemampuan untuk memproses RAW. Hasilnya... bisa dibilang cukup bervariasi.

Camera JPG akan memproses sesuai dengan profile yang dipilih pada saat gambar diambil, dalam hal ini Canon Standard. Fitur *enhancement* yang lain seperti *Auto Lighting Optimizer* maupun *noise reduction* akan mempengaruhi JPG yang dihasilkan.

Adobe Lightroom, sebagai aplikasi *de facto* untuk menyunting foto sejuta umat, menggunakan profile Adobe Color ke setiap foto RAW yang diprosesnya. Saya suka dengan profile ini, karena profile ini bertujuan untuk menghasilkan gambar yang relatif seragam meskipun diambil dari brand dan model kamera yang berbeda-beda. Foto yang dihasilkan

Windows Photo yang lebih sering dipakai untuk menampilkan gambar saja tanpa menyunting, terlihat memproses foto RAW dengan tingkat pencahayaan yang kurang daripada yang lain. Menurut saya aplikasi ini hanya sekedarnya saja untuk menampilkan foto RAW.

Terakhir, Apple Aperture menghasilkan gambar yang sangat bagus. Mirip dengan gambar yang dihasilkan oleh Lightroom dengan profile Adobe Color-nya. Namun bagi saya, warna bunga yang dihasilkan oleh Lightroom lebih sesuai dengan kenyataan ketimbang Aperture.

## Fakta unik: file RAW juga menyimpan gambar JPG ukuran kecil sebagai *preview*

Meskipun foto RAW merupakan data mentah yang belum diproses, namun kamera tetap menyematkan sebuah gambar dengan format JPG dengan ukuran kecil didalamnya. Tujuannya mungkin untuk jaga-jaga apabila ada aplikasi yang tidak bisa memproses data RAW, maka bisa menampilkan gambar JPG ini.

Saya mencoba mengamati file RAW Canon menggunakan aplikasi [MediaInfo](https://mediaarea.net/en/MediaInfo), terlihat bahwa disamping menyimpan informasi data mentah (TIFF) dia juga membawa file JPG dengan ukuran dan resolusi yang lebih kecil daripada data mentahnya.

[![Canon RAW MediaInfo](raw_media_info_small.avif)](raw_media_info.avif)

Cara lain untuk membuktikan bahwa gambar JPG ini ada, coba buka foto RAW tersebut menggunakan Windows Photo. Satu atau dua detik pertama ketika gambar tampil, itu adalah gambar JPG. Aplikasi menggunakan JPG ini saat data RAW sedang diproses. Ketika hasil sudah didapat, maka gambar diganti dengan hasil pemrosesan tersebut. Sehingga terkesan gambar berganti.

[![Canon RAW embeded JPG on Windows Photo](raw_photo_small.avif)](raw_photo.avif)

Ini juga berlaku di Lighroom. Di mode Library, secara *default* akan menampilkan *preview* JPG (bisa dilihat di pojok kanan bawah tertulis *Embeded Preview*), sedangkan di mode Develop akan menampilkan gambar hasil pemrosesan data RAW.

[![Canon RAW embeded JPG on Adobe Lightroom](lighroom_embeded_preview_small.avif)](lighroom_embeded_preview.avif)

Terima kasih sudah membaca dan stay curious! ✨