---
title: Ukuran
---

Setiap blok-level elemen memiliki *binding* `clientWidth`, `clientHeight`, `offsetWidth` dan `offsetHeight`:

```html
<div bind:clientWidth={w} bind:clientHeight={h}>
	<span style="font-size: {size}px">{text}</span>
</div>
```

*Binding* tersebut bersifat *readonly*(hanya bisa dibaca) - mengubah nilai dari `w` dan `h` tidak akan memberi pengaruh apapun.

> Elemen diukur dengan tehnik yang sama dengan [yang satu ini](http://www.backalleycoder.com/2013/03/18/cross-browser-event-based-element-resize-detection/).Ada beberapa overhead yang terlibat, jadi tidak disarankan untuk menggunakan ini untuk elemen dalam jumlah besar. 
>
> elemen `display: inline` tidak bisa diukur dengan pendekatan ini; atau juga dengan elemen yang tidak bisa mengandung elemen lain (seperti `<canvas>`). Dalam kasus ini kamu harus mengukur pembungkus elemen tersebut.
