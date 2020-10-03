---
title: This
---

*Binding* `this` bersifat *readonly* berlaku untuk setiap elemen (dan komponen) dan memungkinkanmu mendapatkan refrensi ke elemen yang dirender. Contohnya, kita bisa mendapatkan refrensi ke elemen `<canvas>`:

```html
<canvas
	bind:this={canvas}
	width={32}
	height={32}
></canvas>
```

Catatan, nilai dari `canvas` akan `undefined` sampai komponennya dipasang, jadi kita menaruh logikanya didalam [fungsi *lifecycle*](tutorial/onmount) `onMount`.
