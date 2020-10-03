---
title: Masukan teks
---

Sebagai peraturan umum, alur data dalam Svelte adalah *atas bawah* - sebuah komponen induk dapat mengatur properti dari komponen anak, dan sebuah komponen bisa mengatur atribut dalam sebuah elemen, tapi tidak sebaliknya.

Terkadang melanggar aturan itu baik. Ambil contoh kasus `<input>` elemen dalam komponen ini - kita *bisa* menambahkan `on:input` event *handler* yang mengatur nilai dari `name` ke `event.target.value`, tapi ini sedikit... *boilerplatey*(boilerplate => kode yang harus disertakan di banyak tempat dengan sedikit atau tanpa perubahan). Ini akan menjadi lebih buruk dengan bentuk elemen lainnya, seperti yang akan kita lihat.  

Sebagai gantinya, kita bisa menggunakan `bind:value` direktif:

```html
<input bind:value={name}>
```

Ini berarti tidak hanya akan merubah nilai dari `name` akan memperbarui nilai masukan, tapi perubahan ke nilai masukan juga akan memperbarui `name`.
