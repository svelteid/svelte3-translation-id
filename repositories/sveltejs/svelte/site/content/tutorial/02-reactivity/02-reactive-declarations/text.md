---
judul: Deklarasi
---

Svelte secara otomatis memperbarui DOM ketika status komponen kamu berubah. Seringkali, beberapa bagian dari status komponen perlu dihitung dari bagian *lain* (seperti `nama lengkap` yang diturunkan dari` nama depan` dan `nama belakang`), dan dihitung ulang setiap kali mereka berubah.

Untuk ini, kami memiliki *deklarasi reaktif*. terlihat seperti ini:

```js
let count = 0;
$: doubled = count * 2;
```

> Don't worry if this looks a little alien. It's [valid](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label) (if unconventional) JavaScript, which Svelte interprets to mean 're-run this code whenever any of the referenced values change'. Once you get used to it, there's no going back.

Mari gunakan `doubled` di markup kita:

```html
<p>{count} doubled is {doubled}</p>
```

Tentu saja, kamu bisa menulis `{count * 2}` di markup - kamu tidak perlu menggunakan nilai reaktif. Nilai reaktif menjadi sangat berharga ketika kamu perlu mereferensikannya beberapa kali, atau kamu memiliki nilai yang bergantung pada nilai reaktif *lain*.
