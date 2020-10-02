---
title: Handlers baris
---

Kamu juga bisa mendeklarasikan event *handlers* dalam baris:

```html
<div on:mousemove="{e => m = { x: e.clientX, y: e.clientY }}">
	The mouse position is {m.x} x {m.y}
</div>
```

Tanda kutip bersifat opsional, tapi itu sangat membantu untuk menyoroti sintaks di lingkungan tertentu. 

> Pada beberapa kerangka kerja kamu mungkin melihat rekomendasi untuk menghindari penggunaan event *handlers* baris untuk alasan performa, khususnya dalam perulangan. Nasihat itu tidak berlaku untuk Svelte - kompailer selalu melakukan hal yang benar, apapun bentuk yang kamu pilih.
