---
title: Blok each binding
---

Kamu bahkan bisa mem*bind* properti kedalam sebuah blok `each`.

```html
<input
	type=checkbox
	bind:checked={todo.done}
>

<input
	placeholder="What needs to be done?"
	bind:value={todo.text}
>
```

> Catatan interaksi dengan elemen `<input>` akan mengubah *array*. Jika kamu lebih memilih bekerja dengan data yang *immutable*(kekal), kamu harus menghindari penggunaan *bindings* seperti tadi dan lebih baik gunakan event *handlers*.
