---
title: Deklarasi properti
---

Sejauh ini, kita hanya berurusan dengan status internal saja - artinya, nilai hanya bisa diakses dalam komponen tertentu.

Dalam aplikasi di dunia nyata, kamu perlu mengoper data dari satu komponen ke anak - anaknya. Untuk melakukan itu, kita perlu mendeklarasikan *properti*, yang pada umumnya disingkat '*props*'. Pada Svelte, kita melakukan itu dengan `export` *keyword*. Ubahlah `Nested.svelte` komponen:

```html
<script>
	export let answer;
</script>
```

> Sama seperti `$:`, ini akan terasa sedikit aneh pada awalnya. Karena `export` tidak bekerja seperti itu pada modul JavaScript! Lakukan saja untuk saat ini - itu akan segera menjadi kebiasaan.
