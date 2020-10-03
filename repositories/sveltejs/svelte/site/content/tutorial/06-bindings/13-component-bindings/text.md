---
title: Binding komponen
---

Seperti kamu bisa *bind* ke properti dari elemen DOM, kamu juga bisa *bind* ke properti komponen. Contohnya, kita bisa *bind* ke properti `value` dari komponen `<Keypad>` seperti halnya itu berbentuk elemen:

```html
<Keypad bind:value={pin} on:submit={handleSubmit}/>
```

Sekarang, saat pengguna berinteraksi dengan keypad, nilai dari `pin` dalam komponen induk akan langsung diperbarui.

> Hematnya penggunaan komponen *binding*. Karena akan jadi sulit untuk melacak alur dari data dalam aplikasimu jika kamu memilikinya terlalu banyak, terutama jika tidak ada 'satu sumber kebenaran'.
