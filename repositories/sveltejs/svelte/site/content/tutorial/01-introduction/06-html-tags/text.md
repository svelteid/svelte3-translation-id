---
judul: tag HTML
---

Biasanya, string disisipkan sebagai teks biasa, artinya karakter seperti `<` dan `>` tidak memiliki arti khusus.

Namun terkadang Kamu perlu merender HTML langsung menjadi sebuah komponen. Misalnya, kata-kata yang Kamu baca sekarang ada di file penurunan harga yang disertakan di halaman ini sebagai gumpalan HTML.

Di Svelte, Kamu melakukan ini dengan tag `{@html ...}` khusus:

```html
<p>{@html string}</p>
```

> Svelte tidak melakukan pembersihan ekspresi apa pun di dalam `{@html ...}` sebelum dimasukkan ke DOM. Dengan kata lain, jika Kamu menggunakan fitur ini, Kamu harus menghindari HTML yang berasal dari sumber yang tidak Kamu percayai secara manual, jika tidak, Kamu berisiko membuat pengguna Kamu terkena serangan XSS.
