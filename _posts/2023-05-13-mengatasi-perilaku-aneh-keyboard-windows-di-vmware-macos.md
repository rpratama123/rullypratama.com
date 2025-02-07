---
layout: post
author: "Rully Pratama"
date: 2023-05-13

title: "Mengatasi Perilaku Aneh Keyboard Windows di VMWare Fusion macOS"
permalink: "/mengatasi-perilaku-aneh-keyboard-windows-di-vmware-macos/"

description: "Virtualisasi Windows di macOS menyisakan beberapa pertanyaan aneh soal perilaku keyboard dan mouse"
image: "assets/images/2023/hackintosh-tricks/hackintosh-keyboard-tricks.jpeg"

keywords:
- hackintosh
- macos
- vmware fusion
- keyboard shortcut
- windows on vmware fusion
- windows virtualization

categories:
- Tutorial
- Random
---

Baru-baru ini, saya [memasang macOS di PC yang saya pakai sehari-hari](/my-2023-hackintosh-build/), alias Hackintosh. Namun beberapa aplikasi yang berkaitan dengan pekerjaan hanya berjalan di Microsoft Windows. Salah satu contohnya adalah Microsoft Power BI. Sehingga mau tidak mau saya memasang *virtual machine* menggunakan VMWare Fusion untuk menjalankan aplikasi tersebut. Namun ada beberapa keanehan yang berkaitan dengan keyboard yang saya alami.

## Ctrl + Arah Menyebabkan macOS Berpindah Desktop

![Ubah pengaturan kombinasi tombol Ctrl + arah di macOS](/assets/images/2023/hackintosh-tricks/ubah-pengaturan-move-space-macos.webp)

Kombinasi tombol `Ctrl` plus arah, `Ctrl + →` misalnya, sangat sering saya gunakan untuk navigasi antar *cell* di Microsoft Excel. Sayangnya, ketika saya gunakan kombinasi tombol ini, bukannya kursor saya yang berpindah, namun sistem operasi *host* saya yang merespon dengan cara berpindah ke satu desktop ke desktop lainnya.

Hal ini disebabkan oleh kombinasi tombol `Ctrl + ←` atau `Ctrl + →` digunakan oleh macOS untuk fungsi yang saya sebutkan di atas tadi. Solusinya adalah, saya ganti kombinasi tombolnya menjadi `Control + Command + →` agar tidak bertabrakan dengan Windows. Pengaturan ini bisa dicari di **Setting → Keyboard → Shortcuts → Mission Control → Move left a space / Move right a space**.

## Ctrl + Klik Kiri Menjadi Klik Kanan

![Ubah pengaturan secondary click di VMWare di macOS](/assets/images/2023/hackintosh-tricks/ubah-pengaturan-secondary-button-mouse-vmware-macos.webp)

Salah satu kombinasi tombol di macOS yang menurut saya 'aneh' adalah `Ctrl + Left Click` diterjemahkan sebagai `Right Click`. Perilaku ini juga ikut dibawa ke Windows melalui VMWare. Tapi kabar baiknya fungsi ini bisa dinonaktifkan dengan cara sebagai berikut.

Melalui menu bar VMWare, pergi ke **Virtual Machine → Settings → Keyboard & Mouse**, pilih profile yang sedang aktif, lalu klik pada tombol **Edit profile...**. Kemudian pergi ke **Keyboard & Mouse → Mouse Shortcuts**. Di sana matikan opsi **Secondary Button**. Dengan begitu kombinasi `Ctrl + Left Click` akan bekerja seperti seharusnya di Windows.

Semoga bermanfaat! ✨

