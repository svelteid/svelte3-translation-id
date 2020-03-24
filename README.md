# Terjemahan Sumberdaya Svelte

> Saat ini, belum diketahui bagaimana bentuk implementasi penerjemahan sumber daya resmi Svelte akan diimplementasikan, oleh sebab itu nantinya perubahan dalam struktur dan pendekatan repositori ini sangatlah mungkin akan terjadi di kemudian hari.
 

## Hasil Penerjemahan
Situs resmi berbahasa Rusia berikut ini telah diluncurkan:
- [ru.svelte.dev](https://ru.svelte.dev)
- [ru.sapper.svelte.dev](https://ru.sapper.svelte.dev)
- [ru.svelte-native.technology](https://ru.svelte-native.technology)

> Rencananya situs versi Indonesia akan dikumpulkan dan di-_deploy_ secara otomatis setelah semua _commit_ ke dalam repositori ini dinyatakan lengkap.

![](https://github.com/svelteid/svelte3-translation-id/workflows/Deploy%20id.svelte.dev%20site/badge.svg)
![](https://github.com/svelteid/svelte3-translation-id/workflows/Deploy%20id.sapper.svelte.dev%20site/badge.svg)
![](https://github.com/svelteid/svelte3-translation-id/workflows/Deploy%20id.svelte-native.dev%20site/badge.svg)

## Apa yang Diterjemahkan
* [Tutorial](https://svelte.dev/tutorial) Svelte V3 ([GitHub](https://github.com/sveltejs/svelte/tree/master/site/content/tutorial))
* [Dokumentasi](https://svelte.dev/docs) Svelte V3 ([GitHub](https://github.com/sveltejs/svelte/tree/api-reference/site/content/docs))
* [Dokumentasi](https://sapper.svelte.technology/guide) Sapper ([GitHub](https://github.com/sveltejs/sapper.svelte.technology/tree/master/content/guide))
* [Contoh](https://svelte.dev/repl) ([GitHub](https://github.com/sveltejs/svelte/tree/master/site/content/examples))
* [Blog](https://svelte.dev/blog) ([GitHub](https://github.com/sveltejs/svelte/tree/master/site/content/blog))
* Konten situs [svelte.technology](https://svelte.dev) ([GitHub](https://github.com/sveltejs/svelte/tree/master/site/src))
* Konten situs [sapper.svelte.technology](https://sapper.svelte.technology) ([GitHub](https://github.com/sveltejs/sapper.svelte.technology/tree/master/src))
* Konten situs [svelte-native.technology](https://svelte-native.technology) ([GitHub](https://github.com/halfnelson/svelte-native/tree/master/docs_src/content))


## Bagaimana Cara Berkontribusi pada Penerjemahan
* [Terjemahkanlah](https://github.com/svelteid/svelte3-translation-id/issues) bagian dari sumber daya apa saja di atas yang belum diterjemahkan.
* Tingkatkanlah kualitas terjemahan yang sudah ada: perbaikilah kesalahan pengejaan, tanda baca atau semantik, revisilah kalimat yang disusun dengan buruk, hilangkanlah inkonsistensi terjemahan dengan rekomendasi, dll. Cara melakukannya hanya melalui sistem _pull request_ dalam repositori github ini.

## Rekomendasi Terjemahan

* Desain terjemahan harus sesuai dengan desain aslinya. 
* Lebih baik untuk membangun kalimat dalam bentuk anonim (tanpa `kami` dan tanpa ` Anda`), walaupun tidak wajib, agar Dokumentasi jangan menjadi terlalu formal.
* Gunakanlah tanda pisah —— manakala dibutuhkan, dan gunakanlah tanda hubung -— saat dibutuhkan. Contoh: sebagaimana Svelte adalah sebuah framework.
* Di semua contoh kode, komentar dan semua teks yang terkait dengan antarmuka pengguna (_user interface_/ UI) wajib diterjemahkan, yakni apa yang dilihat pengguna saat menjalankan contoh tersebut.
* Daftar urutan prioritas penerjemahan dari yang utama yang harus disepakati:
  * [Glosarium](DICTIONARY.md) Svelte;
  * gunakanlah persamaan atau analogi dengan terjemahan dokumentasi framework ternama lainnya (Vue, React, Angular);
  * gunakanlah dokumentasi berbahasa Indonesia, laporan atau artikel yang menggunakan kosakata yang baik dan benar;
  * yang terakhir gunakanlah terjemahan hasil temuan pribadi.
* Hindarilah kebarat-baratan selama masih ada padanan kata dalam Bahasa Indonesia.
* Tautan yang menuju ke sumber daya eksternal (MDN, Wikipedia) haruslah diarahkan kepada versi yang sudah diterjemahkan ke dalam Bahasa Indonesia jika ada.
*  Terjemahkanlah nama asing dengan nama asli dalam tanda kurung: *(Rich Harris)*.
* Judul artikel referensi yang ditulis dalam bahasa asing haruslah disampaikan dalam bahasa aslinya lalu diikuti dengan terjemahan Bahasa Indonesia dalam tanda kurung.
* Upayakanlah menggunakan bahasa umum yang tidak membedakan gender.
* Judul artikel dan _heading_ ditulis dengan huruf kapital.
* Bahasa asing yang tidak diterjemahkan karena dianggap bahasa umum komputer, ditulis dalam cetak miring misalnya: _file_, _browser_.

Untuk menghindari kebingungan, cobalah mengartikan suatu kalimat dan mengulanginya seolah menjelaskan kepada kolega senior. Apabila kalimatnya terdengar janggal, maka kalimat tersebut harus ditulis kembali dengan cara yang berbeda.

Sedikit ruang kebebasan berekspresi dalam penerjemahan tetap diperkenankan, namun jika dan hanya jika terjemahan itu membantu memperjelas makna. Terjemahan sebaiknya jangan terlalu resmi tapi juga jangan terlalu longgar. Carilah terjemahan yang baik dan benar di antara kedua ekstrim tersebut.

## Luncurkan Situs Versi Lokal

Skrip npm telah ditambahkan ke dalam repositori, yang memperkenankan Anda dari Github untuk mengambil versi terkini situs yang terkait dalam projek ini, aplikasikanlah semua modifikasi dari repositori terjemahan ini dan jalankanlah salinan situs pada komputer Anda untuk melihat secara langsung hasil terjemahannya.


```bash
git clone git@github.com:AlexxNB/svelte3-translation-ru.git svelte-translation
cd svelte-translation

# 1. Instalasi semua paket wajib
npm install

# 2. Unduh versi terkini dari situs yang diinginkan dan aplikasikan terjemahan pada situs itu
npm run update-svelte 
#...atau...
npm run update-sapper 
#...atau...
npm run update-svelte-native 

# 3. Luncurkan situs pada mesin lokal
npm run dev-svelte
#...atau...
npm run dev-sapper
#...atau...
npm run dev-svelte-native
```

Kini kamu bisa buka situsnya _running_ di [http://localhost:3000]() dan lihatlah semua perubahan yang tampak padanya saat ini.

Ketika mengubah _file_ terjemahan, _refresh_ jendela peramban (_browser_) dan kamu akan lihat perubahannya.