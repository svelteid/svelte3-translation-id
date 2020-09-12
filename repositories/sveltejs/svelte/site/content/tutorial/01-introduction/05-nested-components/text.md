---
judul: Komponen bersarang
---

Tidak praktis untuk menempatkan seluruh aplikasi Kamu dalam satu komponen. Sebagai gantinya, kamu dapat mengimpor komponen dari file lain dan memasukkannya seolah-olah kamu sedang memasukkan elemen.

Tambahkan tag `<script>` yang mengimpor `Nested.svelte` ...

```html
<script>
	import Nested from './Nested.svelte';
</script>
```

... lalu tambahkan ke markup:

```html
<p>This is a paragraph.</p>
<Nested/>
```

Perhatikan bahwa meskipun `Nested.svelte` memiliki elemen` <p> `, gaya dari` App.svelte` tidak bocor.