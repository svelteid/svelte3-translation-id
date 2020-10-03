---
title: Masukan area teks
---

Elemen `<textarea>` berperilaku sama ke sebuah masukan teks dalam Svelte - gunakan `bind:value`:

```html
<textarea bind:value={value}></textarea>
```

Dalam kasus seperti ini, dimana nama yang cocok, kita juga bisa menggunakan bentuk steno(lambang huruf yang dipendekkan dan disepakati pemakaiannya):

```html
<textarea bind:value></textarea>
```

Ini berlaku untuk semua *bindings*, tidak hanya area teks.
