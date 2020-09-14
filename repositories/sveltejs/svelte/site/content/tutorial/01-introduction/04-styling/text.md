---
judul: Styling
---

Sama seperti di HTML, Kamu dapat menambahkan tag `<style>` ke komponen Kamu. Mari tambahkan beberapa gaya ke elemen `<p>`:

```html
<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>

<p>This is a paragraph.</p>
```

Yang penting, aturan ini *dicakup ke komponen*. Kamu tidak akan secara tidak sengaja mengubah gaya elemen `<p>` di tempat lain dalam aplikasi-mu, seperti yang akan kita lihat di langkah berikutnya.