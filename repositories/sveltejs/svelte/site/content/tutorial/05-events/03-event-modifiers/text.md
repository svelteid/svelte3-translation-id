---
title: Pengubah event
---

DOM event *handlers* bisa memiliki *pengubah* yang mengubah perilaku dari event tersebut. Contohnya, sebuah *handler* dengan pengubah `once` akan dijalankan saat pertama kali saja:

```html
<script>
	function handleClick() {
		alert('no more alerts')
	}
</script>

<button on:click|once={handleClick}>
	Click me
</button>
```

Daftar lengkap dari pengubah:

* `preventDefault` — panggil `event.preventDefault()` sebelum menjalankan *handler*. Berguna untuk menangani *client-side* formulir, contohnya.
* `stopPropagation` — panggil `event.stopPropagation()`, mencegah event untuk mencapai elemen berikutnya 
* `passive` - meningkatkan performa *scrolling* saat event *touch/wheel* (Svelte akan menambahkannya secara otomatis di tempat yang aman untuk melakukannya)
* `capture` — Meluncurkan *handler* selama tahap *capture* daripada tahap *bubbling* ([Dokumen MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#Event_bubbling_and_capture))
* `once` — menghapus *handler* setelah pertama kali dijalankan
* `self` — picu *handler* hanya saat event.target adalah element itu sendiri

Kamu bisa menyatukan pengubah, contoh: `on:click|once|caputre={...}`.
