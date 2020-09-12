---
judul: Menambahkan data
---

Komponen yang hanya membuat markup statis tidak terlalu menarik. Mari tambahkan beberapa data.

Pertama, tambahkan tag skrip ke komponen Kamu dan nyatakan variabel `nama`:

```html
<script>
	let name = 'world';
</script>

<h1>Hello world!</h1>
```

Kemudian, Kamu bisa merujuk ke `nama` di markup:

```html
<h1>Hello {name}!</h1>
```

Di dalam kurung kurawal, Kamu bisa meletakkan JavaScript apa pun yang Kamu inginkan. Coba ubah `name` menjadi` name.toUpperCase () `untuk sapaan yang lebih seru.