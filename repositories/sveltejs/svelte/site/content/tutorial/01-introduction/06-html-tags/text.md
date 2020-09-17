---
judul: tag HTML
---

Biasanya, string disisipkan sebagai teks biasa, artinya karakter seperti `<` dan `>` tidak memiliki arti khusus.

Namun terkadang kamu perlu merender HTML langsung menjadi sebuah komponen. Misalnya, kata-kata yang kamu baca sekarang ada di file penurunan harga yang disertakan di halaman ini sebagai gumpalan HTML.

Di Svelte, kamu melakukan ini dengan tag `{@html ...}` khusus:

```html
<p>{@html string}</p>
```

> Svelte tidak melakukan pembersihan ekspresi apa pun di dalam `{@html ...}` sebelum dimasukkan ke DOM. Dengan kata lain, jika kamu menggunakan fitur ini, kamu harus menghindari HTML yang berasal dari sumber yang tidak kamu percayai secara manual, jika tidak, kamu berisiko membuat pengguna kamu terkena serangan XSS.
