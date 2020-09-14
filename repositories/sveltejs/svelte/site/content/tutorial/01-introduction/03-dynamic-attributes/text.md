---
judul: atribut dinamis
---

Sama seperti saat Kamu menggunakan tanda kurung kurawal untuk mengontrol teks, Kamu dapat menggunakannya untuk mengontrol atribut elemen.

Gambar Kamu kehilangan `src` - mari tambahkan satu:

```html
<img src={src}>
```

Itu lebih baik. Tapi Svelte memberi kita peringatan:

> A11y: &lt; img &gt; elemen harus memiliki atribut alt

Saat membuat aplikasi web, penting untuk memastikan bahwa aplikasi *dapat diakses* oleh basis pengguna seluas mungkin, termasuk orang-orang dengan (misalnya) gangguan penglihatan atau gerak, atau orang-orang tanpa perangkat keras yang kuat atau koneksi internet yang baik. Aksesibilitas (disingkat a11y) tidak selalu mudah untuk dilakukan dengan benar, tetapi Svelte akan membantu dengan memperingatkan Kamu jika menulis markup yang tidak dapat diakses.

Dalam kasus ini, Kamu kehilangan atribut `alt` yang mendeskripsikan gambar untuk orang yang menggunakan pembaca layar, atau orang dengan koneksi internet yang lambat atau tidak stabil yang tidak dapat mengunduh gambar. Mari tambahkan satu:

```html
<img src={src} alt="A man dances.">
```

Kamu bisa menggunakan tanda kurung kurawal *di dalam* atribut. Coba ubah menjadi `" {name} dances. "` - ingatlah untuk mendeklarasikan variabel `name` di blok` <script> `.


## Atribut singkatan

Tidak jarang memiliki atribut yang nama dan nilainya sama, seperti `src = {src}`. Svelte memberi kita singkatan yang nyaman untuk kasus-kasus ini:

```html
<img {src} alt="A man dances.">
```

