---
judul: Penugasan
---

Inti dari Svelte adalah sistem *reaktivitas* yang kuat untuk menjaga agar DOM tetap sinkron dengan status aplikasi Kamu - misalnya, sebagai respons terhadap suatu peristiwa.

Untuk mendemonstrasikannya, pertama-tama Kamu perlu memasang pengendali event. Ganti baris 9 dengan ini:

```html
<button on:click={handleClick}>
```

Di dalam fungsi `handleClick`, yang perlu kamu lakukan hanyalah mengubah nilai` count`:

```js
function handleClick() {
	count += 1;
}
```

Svelte 'instrumen' penugasan ini dengan beberapa kode yang memberitahukannya bahwa DOM perlu diperbarui.