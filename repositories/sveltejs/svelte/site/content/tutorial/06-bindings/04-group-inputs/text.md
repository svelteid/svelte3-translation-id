---
title: Masukan kelompok
---

Jika kamu memiliki banyak masukan yang terkait dengan nilai yang sama, kamu bisa menggunakan `bind:group` bersama dengan atribut `value`. Masukan radio dalam kelompok yang sama saling berketerkaitan; masukan kotak centang dalam kelompok yang sama akan membentuk sebuah *array* dari nilai pilihan. 

Tambahkan `bind:group` ke setiap masukan:

```html
<input type=radio bind:group={scoops} value={1}>
```

Dalam kasus ini, kita bisa membuat kodenya jadi lebih sederhana dengan memindahkan masukan kotak centang ke dalam sebuah blok `each`. Pertama, tambahkan sebuah *variable* `menu` ke dalam block `<script>`...

```js
let menu = [
	'Cookies and cream',
	'Mint choc chip',
	'Raspberry ripple'
];
```

...lalu ganti sesi ke dua:

```html
<h2>Flavours</h2>

{#each menu as flavour}
	<label>
		<input type=checkbox bind:group={flavours} value={flavour}>
		{flavour}
	</label>
{/each}
```

Sekarang akan lebih mudah memperluas menu es krim dalam direksi yang baru dan seru.
