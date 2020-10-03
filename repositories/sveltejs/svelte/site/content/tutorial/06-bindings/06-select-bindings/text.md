---
title: Binding pilihan
---

Kita juga bisa menggunakan `bind:value` dengan elemen `<select>`. Perbarui baris 24:

```html
<select bind:value={selected} on:change="{() => answer = ''}">
```

Catatan nilai `<option>` adalah sebuah objek daripada *strings*. Svelte tidak keberatan.

> Karena kita belum mengatur nilai awal dari `selected`, *binding* akan mengaturnya ke nilai default (baris pertama dari daftar) secara otomatis. Berhati-hatilah - sampai *binding* dimulai, `selected` akan tetap *undefined*, jadi kita tidak bisa merefrensikan begitu saja contoh: `selected.id` dalam template. 
