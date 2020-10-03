---
title: Masukan angka
---

Dalam DOM, segalanya adalah sebuah *string*. Itu tidak membantu saat kamu berurusan dengan masukan angka - `type="number"` dan `type="range"` - itu artinya kamu harus ingat untuk memaksa `input.value` sebelum menggunakannya.

Dengan `bind:value`, Svelte akan mengurusnya untuk kamu:

```html
<input type=number bind:value={a} min=0 max=10>
<input type=range bind:value={a} min=0 max=10>
```
